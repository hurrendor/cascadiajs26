# Teaching LLMs New Tricks 

## Marty Nelson
### Works Real Estate, Portland, OR USA 
- [Speaker's Notes (Placeholder)]()
- [Post-conference YouTube Recording (Placeholder)]()
## Abstract: 

AI bias for dominant patterns means training data = market share. That's innovation friction! The right syntax, wrong semantics, e.g. any innovation with JSX looks like React. Explore specific strategies that work, co-developed with AI, and tested in real world projects.
## Community talk notes: 

[Azoth](https://github.com/azothjs/azoth) — open source library.

### From shelved to revived
- Winter 2023–24: built it
- When AI hit: shelved it
- Nov 2025: AI changed the math, and brought back Azoth!

The origin: building a dashboard for a real estate brokerage (Google Looker couldn't find the right thing in the "vending machine"). Visually intensive components — why not just write HTML and CSS? Combining a brokerage with a property developer added integration analysis, which is high user touch.

### Right syntax, wrong semantics
JSX is everywhere, so the AI defaults to React — same syntax, wrong semantics. Azoth is JSX *without* a vDOM: it controls the render, no JS creating the DOM — `<p>Hello</p>` just returns a `<p>` tag.

First instinct was to treat the new framework like a new framework (reach for an adjacent concept) and just use it a bit. That backfired — using the language as-is confuses the LLM.

### Don't onboard the LLM — hire it as the new senior maintainer
- A "Don't Say…, Say Instead" map: don't confuse our innovation with the incumbent's.
- And… the LLM is curious about your tech!
- Build a **shared mental model** — a system metaphor that's shared; start a conversation.
- Don't describe in negative space against something else; talk about the thing as it *is*.

### Azoth JSX is real DOM
- What does it compile to? It doesn't interfere with JavaScript — it takes the HTML and makes a template (the JS creates no DOM).
- It doesn't use a factory function to make the DOM; it adds small, deduplicated helper functions for binding.
- It's like the opposite of React — what you opt *into* with React, you opt *out* of with Azoth.

### Subtraction, not replacement
- Don't replace the vDOM — subtract it.
- The leap: closures and DOM. Reduce it to a DOM problem.
- A component = a constructor, literally. "LLM, hey — THIS IS DOM!" Reach for a tool that makes sense for the problem.
- Azoth basically accepts everything JSX already has. No proprietary primitives, just JS.
- Notice the shape — this was the unlock: **remove the abstraction.**
- The new mapping is SUBTRACT and unlock, not "don't say, say this instead."

### Prompts as navigation
Prompts aren't engineering instructions — they're navigation. Push away from what's being subtracted, and pull toward what's unlocked. Avoid negation ("don't think about a pink elephant").

### Law of the AI era
- **Context** — what you carry into the conversation.
- **Corpus** — what's already in the model. That's your budget; be smart about it.
- **Subtract your abstractions, unlock the corpus.**

### How the stall happened
Three trends accumulated cruft we didn't need:
1. **Monetization pull** — AWS, Vercel: tech advice that favors higher-revenue architecture, and then lock-in keeps you there.
2. **The status of engineering** — "developer" became a put-down, and the web platform was devalued alongside it (developer = externally facing, engineer = internally facing; front-end diminished and forward-deployed — ticket-takers).
3. **Sophistication as litmus** — more-engineered = perceived better. Whose interest is the data we're given actually in?

The cycle: New Floor → innovation → adoption → commoditization (or *stall = collapse*). The corpus rising is progress; the failure mode is **stall** — no input back to innovation. Respond to what's actually going on in reality: think holistically.

As the LLM put it: what you choose to build is also what you choose to feed me — make it interesting. Cookie-cutter apps, or something that doesn't exist yet? We all need to pick something that doesn't exist yet.

Links: [github.com/azothjs/azoth](https://github.com/azothjs/azoth) · [@martypdx](https://github.com/martypdx)