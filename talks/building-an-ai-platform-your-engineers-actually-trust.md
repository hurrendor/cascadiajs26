# Building an AI Platform Your Engineers Actually Trust 

## Jeff Otaño
### Onebrief, Denver, CO USA 
- [Speaker's Notes (Placeholder)]()
- [Post-conference YouTube Recording (Placeholder)]()
## Abstract: 

Every engineering org has the same problem: developers use AI tools individually, but the organization can't measure, govern, or scale the impact. We went from scattered copilot usage and zero metrics to governed agent environments, shared tooling, and a measurement pipeline that proves what actually works. This is the story of how we built the infrastructure that turned individual AI adoption into organizational capability, and what the data told us along the way.
## Community talk notes:

Making AI "real" inside an org with a decade of infrastructure. The first
instinct was to build the impressive thing — a skills/repo marketplace,
sandboxes, guardrails, a knowledge graph — but nobody had asked whether anyone
actually needed it. An AI bug-diagnoser landed flat too: nobody has time to do
the AI's homework.

### Undeniable beats impressive
The first attempt — an AI fixer for tiny, annoying issues — hit a **16% merge
rate**, with no comments or feedback. The lesson: don't lead with metrics and
impressive demos; create a feedback loop and ship something undeniably useful.

### The homework was already done
The fix was already in the repo: ~1,000 fixes from the past year of real work.
Replaying the agent against that history (rather than asking people to evaluate
speculative output) improved results to a **36% clean-fix rate**.

### Takeaways
- Sandboxes and curated skills make sense when they ease real pain, by default.
- Try it, measure it, and delete what doesn't work.