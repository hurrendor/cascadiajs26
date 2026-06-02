# Choosing TypeScript Matters More Than Ever 

## Filip Sodić
### Wasp, Zagreb, Croatia 
- [Speaker's Notes (Placeholder)]()
- [Post-conference YouTube Recording (Placeholder)]()
## Abstract: 

If "English is the new programming language" and "an agent's output is just machine code," should you still care about picking TypeScript? Yes, you absolutely should! Let's dig into the reasons why.
## Community talk notes: 

### Scribe: Mike Wasserman
- Choose Typescript, good to learn language even with LLM
- Built a tower of abstractions to turn ideas into machine actions
  - base is binary, then assembly, then compilers and high-level languages like C, then TS/Go/Python, Frameworks, then apps
- Things have changed, everything is AI Agents; may sit above frameworks
  - AI making english the new programming language (Jenson Huang) or just fancy autocomplete
- English isn't a good spec language, not precise, etc.
  - We're not commiting prompts, we're commiting code
- Languages are here to stay, Typescript is good at compression
  - Output of engineering: Compress context of ideas -> Types, Code (plus validation, tests, var names), documention, human memory
  - Lots actually stays in human memory
  - We tend to implement first, then document later
  - Code is cheap we can generate new code, right?
- example of coffee serve function (kind, beans, shots, milk)
  - shoot first ask questions later
  - impl looks reasonable, but lack of clarity about the params, lots still in our heads (max shots, etc.)
  - funny example about using claude to document
  - Docs are not the harness, claude answered the qs by guessing, etc.
  - Testing helps: wrong types, nonsensical values, semantic relationships, etc.
  - Need to duplicate checks in implementation
  - Tests don't explain reality, just examples
- Typescript is the better way
  - strong types, don't need to test wrong types
  - offer enums and ranges, then need to specify less
  - still unanswered: how many shots does drip coffee have? (bad question)
  - try to embed knowledge in the type system
- Ask questiosn first, instead of coding first
  - Mythical man month quote
  - AI Prompt is writing an ambiguous specification
  - Feel like we're moving slow if we're not using an agent
  - Better to define clear types; defining clear types of Coffee with Espresso and Drip type composition
  - Can remove so many tests and checks by having robust opinionated types that encode knowledge
- Comparing languages:
  - Rust can do more, but makes you think about stuff some projects don't need (added complexity)
  - Go type system is less powerful, has different goals
- Typescript is great, but getting better
  - Modern safer defaults, better errors, removed legacy baggage, rewrite in Go
  - 
