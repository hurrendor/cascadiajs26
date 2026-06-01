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

### How Spec Driven Development can make code faster