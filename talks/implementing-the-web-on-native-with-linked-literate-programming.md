# Implementing the Web on Native with Linked Literate Programming 

## James Ide
### Expo, Palo Alto, CA USA 
- [Speaker's Notes (Placeholder)](https://github.com/ccheever/llp)
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

[Camera Demo specs referenced](https://github.com/expo/web-standard-camera-demo)