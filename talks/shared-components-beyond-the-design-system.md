# Shared Components Beyond the Design System 

## Jonathan Keslin
### Atlassian, Kirkland, WA USA 
- [Slides](https://jonathankeslin.com/cascadiajs26)
- [Post-conference YouTube Recording (Placeholder)]()
## Abstract: 

Lots of companies have design system component libraries these days, but those aren't the only shared components around. This talk will center around higher-level shared components for those more complex common UI elements, including how to architect them for reusability, how to ensure they're flexible enough for novel use, and how to govern contributions.
## Community talk notes:

Beyond the design system (DS — your UX foundations, atomicity) there's a whole
class of higher-level, navigation/UX or team-specific components that are either
design-system candidates or live one layer up. How should you build them?

### Before you build
- **Who are you building for?** Anchor on a consumer, then add a *second*
  consumer early so the implementation doesn't couple itself to the anchor's use
  case.
- **Where are you building it?** Keep it separate from the app so it can evolve
  independently, and publish artifacts to avoid copy-paste habits.
- **Build it thoughtfully** — hold it to a higher standard than app code and keep
  the API consistent. Common cases should take little to no effort; the most
  custom case can require the most effort (layers 1/2/3 of progressive
  complexity). Prioritize common use cases, but don't forget the complex-but-
  frequent ones — hard mode is allowed to be hard.

### Six principles
1. Build **up** from the design system.
2. Design with **layered extensibility** — make the right way the easy way (e.g. a
   button that takes an icon).
3. Don't build a **Homer car** (don't try to satisfy everyone at once).
4. It's okay to be **opinionated**.
5. Consider **including batteries** — reduce boilerplate, handle data fetching
   where you can (like Relay's fragments), but keep an escape hatch so consumers
   can do something themselves.
6. Make it **maintainable** — thorough tests, liberal docs, and a changelog that
   says what changed and whether consumers need to act.

### Foster an ecosystem & provide governance
Shared components are valuable, so invest in discoverability — a doc site or
marketplace; good docs matter more than ever. Define patterns and practices, and
recognize authors for contributions. A quality-scale model like Home Assistant's
bronze/silver/gold tiers gives contributions a clear bar to clear.