# Accelerating Musical Live Coding With On-Device AI 

## Alex Hinson
### Fleetio, Chattanooga, TN USA 
- [Speaker's Notes](https://cascadiajs-alex.netlify.app/1)
- [Post-conference YouTube Recording (Placeholder)]()
## Abstract: 

Let's explore a human-centric approach to live coding music. By fusing Strudel REPL with on-device AI via WebGPU and Wasm, we create an "intelligent scaffolder" that handles boilerplate syntax locally, keeping the performer in their flow state without losing agency.
## Community talk notes: 

### The goal: extend creativity, not replace it
[Strudel](https://strudel.cc) is a web-based, live-coding music tool — make music with code. The aim is to use AI as a structural assistant for the technical bits, not to hand the music over to it. A small model under the hood keeps the performer in flow without losing agency.

### Why on-device?
Everything runs in the browser tab — no API, no cloud, all local:
- **Cost** — local inference is free
- **Latency** — no network round-trip
- **Privacy** — input never leaves the browser

### Getting a small model good at a niche domain
- **Pick the model family first.** Is the problem translation? Audio classification? Text generation? Each is a different family. Text generation made the most sense here. [transformers.js](https://github.com/huggingface/transformers.js) runs Hugging Face models in the browser.
- **Shape the I/O.** AI is good at ambiguity, inference, and unstructured input; code is good at precision, rules, and structured output. The right answer lives on a continuum between the two:
  - *Off-the-shelf, ask for code* → looks plausible, won't run.
  - *Intent JSON → deterministic engine* → turns intent into code, but a bigger schema/prompt adds latency and stops feeling fluid.
  - *Fine-tuned for structural context* → keep input context small; sanitize and parse the output. Trade away some deterministic guarantees for a tighter, smaller surface and just the right number of tokens.

### Training data when there isn't any
The base model didn't know Strudel, and there were few examples to train on. Alex used LLMs to generate examples (ask for Strudel, see what comes back) — but some output was confident nonsense referencing things that don't exist.
- **Add a validation step**: run generated code through Strudel and discard anything that doesn't parse — so you scale the good examples, not the hallucinations.
- **Ground the model**: keep it concise about what Strudel actually is; don't let it freestyle.

### The ongoing loop
Identify gap → generate → validate → retrain. The work gets more focused but never really stops; each loop makes the tool more like something Alex wants to perform with.

### Shipping it small
**Quantization** shrinks the model by reducing precision so it fits in a browser tab. Runtime is a few lines: import, `await pipeline(...)`, initialize.

### Questions to ask for your own build
- What's the model's task?
- Where's the AI/code boundary?
- Where does the training data come from?
- Does it actually need to be local?