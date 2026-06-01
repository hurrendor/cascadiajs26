# AI Agent Swarms Are Amazing 

## Joel Hooks
### Badass Courses, Portland, OR USA 
- [Speaker's Notes (Placeholder)]()
- [Speaker's Website](https://cascadia.wzrrd.sh/)
- [Post-conference YouTube Recording (Placeholder)]()
## Abstract: 

Agent swarming is a fascinating pattern to massively parallelize work with AI Agents. Instead of a single agent churning through a todo list, you have a coordinator agent that delegates work to a horde of worker agents to break down a todo list in record time. We will dig into agent memory, optimization, and coordination. 
## Community talk notes: 

Developer superpowers
#37 - Own your harness

Joel references this URL for referenced links throughout the talk: https://cascadia.wzrrd.sh/

### Harness Engineering is now
Previously: context engineering

### What is Harness Engineering?
The model you're using interacts with other products and is wrapped by the context that you give it.
Harness includes: 
- System prompts (CLAUDE.md, AGENTS.md, skill files and subagent prompts)
- Bundled infrastructure
- Orchestration logic
- Hooks & middleware for deterministic execution
- Observability (logs, traces, cost & latency metering)

Every mistake becomes a rule.

### Joel's Agent Swarm Story
To Joel, it's important to own your code. Enter OpenCode.
Using swarmtools.ai to operate swarms.

Used the Socratic Method to align intent until Anthropic banned OpenCode.
Began using OpenClaw, gave his agent a SOUL.md to give a smile.
Reference: grimlock.ai
Takeaway from OpenClaw - using Pi gives total control.
Reference: joelclaw.com
Created with Mac Mini, kubernetes

#### Recommendations
- Use Pi (doesn't provide MCP, sub-agents, and so on..)
- Pi add-ons from nicoballion (on Github)
- Pi-CMUX to modify the harness to work the same way as a preferred tool
- PiNotes - mdx(mdsvx) a flavor of markdown

Reference: agentdungeon.ai
Your agents playing D&D

Takeaway: """Agent swarms are hard af (but really fun)"""