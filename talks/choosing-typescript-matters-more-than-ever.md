# Choosing TypeScript Matters More Than Ever 

## Filip Sodić
### Wasp, Zagreb, Croatia 
- [Speaker's Notes - Keynote](https://sodic.dev/choosing-typescript-matters-cascadiajs-2026.key)
- [Speaker's Notes - PDF](https://sodic.dev/choosing-typescript-matters-cascadiajs-2026.pdf)
- [Request the original presentation / more resources (form)](https://forms.gle/j5KMBi1ASB5d1Lj76)
- [Post-conference YouTube Recording (Placeholder)]()
## Abstract: 

If "English is the new programming language" and "an agent's output is just machine code," should you still care about picking TypeScript? Yes, you absolutely should! Let's dig into the reasons why.
## Community talk notes: 
You should learn a language well. TypeSciprt is the perfect choice!

### Why care about the language?
AI will not make languages obsolete just yet. English is not an ideal programming language due to complications
If language didn't matter, we wouldn't be committing code, we would be committing prompts.

### But why TypeScript?
Software engineering is compression - and TS is excellent at compression.
As you work through solutions, context extends around and in order to put the solution to work, you will start compressing things into types, code, docs, and memory

Approaches to reducing memory fade 
1. Modern: Shoot first, ask questions later
    - "Code is cheap"
      - This approach leaves most information to memory
  - Documenting like a boss or using AI
    - Distributes information and context to memory, docs and code
    - Docs are not the harness - AI or the documenter still need to answer outstanding questions
  - Writing tests
    - Tests transfer more context and help document knowledge, but don't prevent mistakes
  - Writing types
    - *If you know something, the types should know it as well*

2. What if we start with questions?
    - Write the types out from the answers
    - Writing out the types allows you to discover the domain as you're building your model

[Invitation form to receive email for learning more about TypeScript](https://docs.google.com/forms/d/e/1FAIpQLSdOhVv4na8SiIztFZxLI-pSQCD_2r2zn2MQRPU8FnyZHPUj2w/viewform)

### What about competition?
TypeScript is best

### TypeScript is getting better
- Modern & safer defaults
- Better errors
- Removed legacy baggage
- Rewrite in Go
- Most popular language in Github today

### The tower of abstractions
Consider the world we've built for the agents: a tower of abstractions, 0/1 at the bottom; climb the tower — ASM, compilers → C, then TS/Go/Python, then frameworks, then applications. In years past we spent most of our time in the language layer. People who dabble in predictions ask where things will land: squashing the lower (and even the higher-level) languages. The truth is in the middle, between irrelevancy and "English is a programming language" — English is not a good programming language.

> Fred Brooks: "Show me your flowcharts and conceal your tables, and I shall continue to be mystified. Show me your tables, and I won't usually need your flowcharts; they'll be obvious."

So instead of defining what we want in a prompt (basically a specification), take a step back and define the type **manually** — that's more precise than English. We can compress our memory *and* preserve context by reaching for the right type: think about the questions related to our domain, then define the appropriate types, discovering the domain *while* building the model.

### On the "just write tests" path
You *can* move some memory into code with test coverage and case exhaustion (plus a happy path) — just use JS, not TS, and add a bunch of tests if you want to throw off 100k lines of code a day. But that reduces entropy by adding extra code, and tests still expect both us and the agent to generalize.

### Odds and ends
- *GrillMe* — a skill to help refine domain modeling (also mentioned by another speaker the day before).
- He considered going deep on branded types, result types, ensuring exhaustiveness, smart constructors, and edge type safety — but decided to keep it simpler. Request the original presentation for that depth (form linked above).

[Feedback form](https://forms.gle/RF8DMhwSvgxKjtnEA)