# Day One Opening Keynote 

## Matt Biilmann
### Netlify, San Francisco, CA USA 
- [Speaker's Notes (Placeholder)]()
- [Post-conference YouTube Recording (Placeholder)]()
## Abstract: 
AX, Agent Experience
Building products for agents

## Community talk notes:

### Chapter I
Netlify objective - Turn imagination into reality
Discussion of how JavaScript is one of the languages that help create the magic of the web.

Progression breakdown of AI assistance and agents within driving vehicles, to having AI autonomy.

"""The whole stack changes when the driver is no longer human"""
Timelapse of autocomplete within the IDE to building with an AI agent to describe ideas and supervise the development to using AI assistance. Shifting the "build vs buy" equation.

We will see a lot of shift happening in how things are developed.
Referencing [OpenClaw.ai](https://openclaw.ai/), autonomous coding agents, and making the comparison to self-driving cars.
While autonomous cars make us rethink cities, autonomous agents make us rethink our platforms, virtual cities, products and more.

### Chapter II - Agent Experience
Today - AX is critical for infra and dev tools
Tomorrow: your products wont' succeed without it

Before UX (User Experience) was coined by Don Norman, the interaction with the UI was not seen as an experience.
DX - Developer Experience coined by Jeremiah Lee Cohick
AX - Agent Experience
Covering the experience that agents will have as they work with a product or platform.

[agentexperience.ax](https://agentexperience.ax/) is the canonical community hub for AX — concepts, articles, research, and open collaboration driving the standard forward.

### How to AX?
It's about understanding how agents experience your product. Every product already has an Agent Experience — the question is whether it's good.

### The 4 Pillars of AX
**1. Access**
- Can the agent access your product?
- Does your agent have the correct permissions?
Bots used to get banned for being bots; being a bot is no longer inherently a problem, but auth still needs solving. Emerging standards like WorkOS's AgentAuth add a new identity layer that identifies agents *and* the humans that own them. Netlify's response: [netlify.ai](http://netlify.ai) serves markdown-only to bots instead of the marketing site.

**2. Context** 
- Does the LLM know about your product? Shipping a Markdown variant of every page is cheaper to read and friendlier to context windows. Model Context Protocol (MCP) exposes what your product knows in a universal format — it's the UI for LLMs — but don't move an API straight to MCP (it'll overwhelm the context window). Same product, different surfaces: an API is for humans (~100 endpoints); an MCP is for agents (~5 tools that progressively give access).

**3. Tools** 
- Are you building your product for agents?
- Every product has an Agent Experience, but is it good?
A good developer experience (DX) doesn't necessarily mean a good agent experience (AX). For the Netlify CLI, by adding a response that indicates how to use the product without interaction, AX improves by providing an alternative route — a non-interactive escape hatch so an agent can accomplish the same task without human input.

**4. Orchestration**
Make it trivial to kick off longer-running agents in the background of your product (e.g. Linear's background agents). Netlify Agent Runners let you kick off cloud runners with full context so async agents can work autonomously.

### The Road Ahead
"""As agents become autonomous and our whole team become builders, we need to reshape every part of our developer platforms"""

**Evals** — Measuring AX is its own discipline. A practical starting point: try onboarding an agent into your product daily and see if it succeeds. Netlify provided [Axis](https://axis.dev/), an open-source framework for rating and improving the agent experience.
