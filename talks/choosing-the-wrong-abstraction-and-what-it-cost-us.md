# Choosing the Wrong Abstraction (And What It Cost Us) 

## Darius Cepulis
### Mux, Oak Park, IL USA 
- [Speaker's Notes (Placeholder)]()
- [Post-conference YouTube Recording (Placeholder)]()
## Abstract: 

We chose the wrong abstractions and had to throw out our most important component. Oops. This talk unpacks how a well-meaning API collapsed under real-world use, and why composable APIs scale better than configuration-heavy ones, across UI and deeper systems.
## Community talk notes:

A component that starts simple and slowly gets out of control. Material UI is
fantastic when you start, but eventually you hit its limits and migrate toward
composable primitives (Material UI → Base UI).

### Programming interfaces are user interfaces
Referencing Mike Bostock's 2016 essay "What Makes Software Good?":
- Programmers are people, too — form must communicate function.
- Functions that take many arguments are not good functions.
- Contrast `chart.js` vs `D3`: a vending machine vs. a kitchen.

### What is the "right" abstraction?
Configuration-style APIs vs. composable APIs. Composable APIs are:
- **Independent** — each part does one thing well (select, find, extend; read,
  filter, count). Like Lego blocks.
- **Stackable** — the type of the input equals the type of the output, so pieces
  chain together. ("Composition is All You Need" — Fernando Rojo, React Universe
  Conf 2025.)

### Composable APIs aren't free
Configuration cost is linear; composition cost is closer to log(n) — but you pay
it up front, and "isn't this a bit complex?" is a fair question. You can lower
the cost of composition with good docs, good idioms, sensible defaults, errors
that teach, types, consistency, discoverability, and examples — all good stuff.

### But the real answer: provide an abstraction ladder
Lowering the composition cost helps, but the stronger move is to give people a
ladder so they choose their own rung:
- Lowest rung: low-level code for constructing views.
- Higher rung: a visual editor.

You should be able to ascend or descend the ladder without starting over.
Examples: `D3` ↔ `Plot` (`d3(Plot.plot())` descends the ladder), `chart.js` ↔
Observable Plot, shadcn → Base UI → HTML/CSS.

Escape hatches are a config trap. With composition you swap Lego blocks instead
(e.g. Video.js — eject the skin to get the primitives).

### AI angle
Good DX is *usually* good AX. Open code that LLMs can read, understand, and
improve does better — `decepulis/ax-bench` performed better with a composable
API. The right abstraction also leads to smaller bundles (tree-shaking).