# Implementing the Web on Native with Linked Literate Programming 

## James Ide
### Expo, Palo Alto, CA USA 
- [Speaker's Notes (Placeholder)](https://github.com/ccheever/llp)
- [Slides](https://github.com/expo/web-standard-camera-demo/releases/download/v1.0.0/slides.pdf)
- [Post-conference YouTube Recording (Placeholder)]()
## Abstract: 

What does it take to make a browser API work outside the browser? This talk walks through implementing the W3C getUserMedia camera and microphone API for native iOS apps in Expo, using linked literate programming to connect the spec, Web Platform Tests, native code, and AI-assisted development.
## Community talk notes: 

Agents can generate code. We still need durable intent.
Linked Literate Programming (LLP) uses markdown to document our intent
LLP = Markdown specs + references from code.

Why the links matter:
- Coverage
  - Did we implement the relevant spec sections?
- Accuracy
  - Does the code match the referenced spec?
- Intent
  - Are decisions visible above the code level?

Web specs are great inputs for LLP
- edge cases
- carefully designed APIs
- types, methods, lifecycles

An effective pattern: Implement web APIs in native apps
Native apps use the same JS API

### How the links work
Agents import the spec, then leave linking comments back to it from the code,
e.g. `// @ref LLP 0000mediastream-constructor` pointing at a spec heading like
`# Constructors [mediastream-constructor]`. The same spec can drive both web and
native implementations.

Workflow: set up LLP, pull the relevant parts of a spec, then test coverage —
Web Platform Tests (WPT) close the loop, since the edge cases are already
considered in the spec. The result is a more programmatic feedback loop between
spec and code.

[Camera Demo specs referenced](https://github.com/expo/web-standard-camera-demo)