# Design Tokens: Getting Agents to Follow Brand Guidelines 

## Kaelig Deloumeau-Prigent
### Design Tokens W3C CG, Seattle, WA USA 
- [Speaker's Notes - Keynote](https://discord.com/channels/853074440069578772/853074440523087902/1511492364726829228)
- [Speaker's Notes - PDF](https://discord.com/channels/853074440069578772/853074440523087902/1511492364726829228)
- [Post-conference YouTube Recording (Placeholder)]()
## Abstract: 

While AI allows us to ship more UI than ever, it also makes it easier to ship experiences that don't match our design language. Let's see how Design Tokens, the lingua franca of design systems, bridge the gap between design, engineering, and AI.
## Community talk notes: 

Resource
[Join the fight against UI slop and share your design token agentic tooling](https://discord.com/channels/853074440069578772/853074440523087902/1511492364726829228)

### The problem
Design is *not* what ends up getting built. You tell the agent "use the design system, don't make mistakes" — but not everything needs to be in a design system. Bind some complicated one-off as an extreme edge case to every implementation and you end up with too many decisions in each component.

### The bridge: design tokens
All the different targets need a shared language to use the design system:
1. Give them **names**
2. Give them **values**
3. Give them **instructions**

That's a single source of truth for getting branded targets — design tokens. The **Design Tokens Format Module** captures a design decision in the token itself, in JSON files; then you define relationships and swap them when you want. Lots of tooling supports the spec (Figma, Sketch, penpot, and more), stewarded by the **Design Tokens Community Group**.

### Getting agents to follow them
How do we teach agents? Create skills, MCPs, hooks, plugins, CLIs — or train a model on your design system and tokens. The loop:
- **Find tokens** → PLAN
- **Code** → VERIFY (lint)
- **Validate** the suggestion

A lot of teams are investing time here, but there's little-to-no design-token tooling for AIs yet. Join the fight against UI slop — [designtokens.org](https://www.designtokens.org).