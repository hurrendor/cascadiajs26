# Practical Refactors With Modern CSS Colors 

## James Steinbach
### Delinea, Denver, CO, USA 
- [Speaker's Notes ](https://jds.li/css-color)
- [Post-conference YouTube Recording (Placeholder)]()
## Abstract: 

Practical refactors with modern CSS colors: a hands-on talk on simplifying color tokens, dark mode, and theming using modern CSS. Fewer variables, less duplication, clearer intent—using light-dark(), relative colors, and more.
## Community talk notes: 

### Theming
Moving from previous user agent themes to allow the user to apply agent themes
From `color-scheme: light dark;`, `[data-theme="dark"]`, and 1K+ variables

Use
```:root
{ color-scheme: light dark; }
```
`light-dark(<lightValue>,<darkValue>)` in variables to define corresponding colors

### Color Manipulation
Using relative colors
`rgb(from var(--var) r, g, b, alpha)`
Ex: 
```
:root {
--red: #FF0;
}
.button.red {
    background-color: --red;
}
.button.red:hover {   
    background-color: rgb(from var(--red) calc(r+150), g, b / 0.8)
}
```
Existing color functions now implicitly handle the alpha channel. No more `rgba` needed. For lightening colors, use `hsl`
``
hsl(from var(--red) h s l)
``

### Relative color syntax
To reduce code needed for mixins, use `@include --varname`

`color-mix()` - manipulate colors in real time

### Automatic Contrast
`contrast-color()` -- returns either black or white as a strong contrast

Ex:
``
button {
    background-color: --button-color;
    color: contrast-color(var(--button-color))
``

### A few more details from the talk
- **Theme overrides** are tiny now — a six-line block (one each for dark/light),
  e.g. `[data-theme="dark"] { color-scheme: dark; }`.
- **Relative-color syntax** drops the commas in color functions, but alpha needs
  a slash: `hsl(120 50 20 / 0.2)`. Alpha is implicit whether you write `rgb` or
  `rgba`.
- **Tints / normalized lightness** — pull channels off a variable and tweak one,
  e.g. `rgb(from var(--surface-primary) r g 255)`; no clamping needed.
- **Color math** — start from a named color and rotate the hue to derive a
  palette (rotate secondary 120°, tertiary 240°).
- **`contrast-color()`** picks black or white regardless of color scheme, and it
  stacks: use `color-mix()` and relative colors *inside* it to mix a tint in.
- **Browser support** (verify on caniuse): `light-dark()` ~87% (Electron already
  supports it), relative colors ~89%, `color-mix()` ~91%, `contrast-color()`
  ~67%. Tailwind exposes this via `@theme`.