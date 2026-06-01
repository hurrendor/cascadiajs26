# Practical Refactors With Modern CSS Colors 

## James Steinbach
### Delinea, Denver, CO, USA 
- [Speaker's Notes (Placeholder)]()
- [Post-conference YouTube Recording (Placeholder)]()
## Abstract: 

Practical refactors with modern CSS colors: a hands-on talk on simplifying color tokens, dark mode, and theming using modern CSS. Fewer variables, less duplication, clearer intent—using light-dark(), relative colors, and more.
## Community talk notes: 

### Scribe: Mike Wasserman
- jds.li/css-color
- Theming: current is messy
- New method light-dark(<lightValue>, <darkValue>)
  - User agent builds MQ into this, easy to force theme override
- Color manipulation - CSS relative colors , from keyword, rgb and var colors
- Existing colors don't need commas
  - rgb(25 25 25), optional alpha with either comma or slash in no-comma syntax: rgb(25 25 25 / 0.5)
- new syntax
  - from keyword takes a color splits into channels
  - --surface-primary--warmer: rgb(from var(--surface-primary) r g calc(b - 20));
  - can calc with hsl type for lightness, darkening, calcs include type safe clamping
  - hue is not clamped, loops through 360
- color-mix is a another new CSS function - like mixing paints
- Accessibility is important; still hard sometimes
  - automatic contrast: contrast-color(): returns white or black for the best contrast; new April 2026
  - compose contrast-color() with color-mix or using from
- High Can I Use support for these
