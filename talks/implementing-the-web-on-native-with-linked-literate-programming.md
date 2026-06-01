# Implementing the Web on Native with Linked Literate Programming 

## James Ide
### Expo, Palo Alto, CA USA 
- [Speaker's Notes (Placeholder)]()
- [Post-conference YouTube Recording (Placeholder)]()
## Abstract: 

What does it take to make a browser API work outside the browser? This talk walks through implementing the W3C getUserMedia camera and microphone API for native iOS apps in Expo, using linked literate programming to connect the spec, Web Platform Tests, native code, and AI-assisted development.
## Community talk notes: 

### Scribe: Mike Wasserman
- Implementing web spec in a local app
- Agents can generate lots of code, we still need durable intent
- Lots of findings appear in conversations, so they're lost.
- Agent harnesses might be isolated
- Aim is to log chat sessions in plain files
- Link code and specs together - keep them updated in lock step
- Coverage - is each part of spec implemented
- Accuracy - does code implement spec correctly
- Intent - are decisions above the code level?
- web specs are good inputs for LLP; written well and considering lots of factors; written in precise language
- demo: W3C Camera API into iPhone app
- Expo OSS React Native framework for apps (web and native)
  - Web uses built-in browser API
  - Native adds same JS APIs; use platform capabilities
  - now can write once for either
- Camera good example; goal to use W3C Camera spec to implement on iOS, use LLP; run WPTs
- Folks have brought WebGPU to React Native with Dawn
- demo'ed camera as cube texture, edge detection, object identification, depth sensing with WebXR
- Demos running in Chrome on desktop too
- Writing demos took triple time and tokens over implementing specs
- Try LLP with specs github.com/ccheever/llp demo code on gh too: github/com/expo/web-standard-conference??? 

