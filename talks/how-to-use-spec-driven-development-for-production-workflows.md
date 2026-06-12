# How To Use Spec-Driven Development for Production Workflows 

## Erik Hanchett
### AWS, Reno, NV, USA 
- [Speaker's Notes (Placeholder)]()
- [Post-conference YouTube Recording (Placeholder)]()
- [Website](https://www.programwitherik.com)
## Abstract: 

AI coding assistants are great at completing small tasks or features. But what do you do when you're working with more complex codebases and need to build in-depth features that require upfront planning?

This talk makes the case for spec-driven development. I'll show how AI coding assistants can help break down complex tasks into three phases: requirements gathering, technical design, and task implementation. Using a real-world example, we'll look at the trade-offs of this approach and how you can start using it in your own projects right away.
## Community talk notes: 

### What is Spec Driven Development
Specification are the primary contract for generating code.

Questions asked:
- Can't the latest frontier models do everything? Why do we need spec-driven development?
  - Spec-driven development helps guide the code in the correct direction.

Things and ideas to keep in mind:
- Giving too much context makes models confused (AKA context rot or context pollution)
  - AGENTS.md / Steering comes into play here to provide very targeted information about our project.
  - Use skills to handle specific types of complex requests.
    - Have them in place before putting together the specs.
- Giving too much trust in your agent will still result in you being blamed at the end of the day
  - Review the code produced!
  - Set up AI code reviews as well
- Be careful of speed over maintainability - what patterns are being created?

### What do you need to tell your AI IDE for spec-driven development?
Include the following:
- User requirements
- Design document
- Implementation details
- Spec-kit/Open Spec/BMad

*Quick-tip*: Create a MVP

### How does MCP help?
"MCP is the USB-C port for AI"
MCP
- specs can be pulled from project management services 
- from project managers - use any vibe apps created to create the specs

### The three phases in practice
- **Requirements** — written with EARS (Easy Approach to Requirements Syntax).
- **Design** — review the markdown, approve, then move to implementation.
- **Implementation** — can be done out of order; build an MVP as a pedantic,
  tight vertical slice and keep reviewing as you go.

### Property-based tests as a regression net
Use property-based testing to run regression tests against the requirements:
"take all these steps and create the [tests] I can use to prove this works."
The question to keep asking: conceptually, does it work as I expect?

### A little history
[Kiro](https://kiro.dev/) grew out of AWS's experience (Alexa) and started life as a VS Code fork
before becoming a spec-mode tool you can use even in a brownfield app. You don't
strictly need Kiro — you can tell any AI IDE to follow the same
requirements → design → implementation flow (Spec-kit, Open Spec, [BMad](https://github.com/bmad-code-org/bmad-method)).

### A note on when to use SDD
SDD works best for complex, in-depth features — don't reach for it on every task. For simpler work, the overhead isn't worth it.

### How Spec Driven Development can make code faster