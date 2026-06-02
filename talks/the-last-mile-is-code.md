# The Last Mile Is Code 

## Joe Duffy
### Pulumi, Seattle, WA USA 
- [Speaker's Notes](https://github.com/joeduffy/cascadiajs-2026)
- [Post-conference YouTube Recording (Placeholder)]()
## Abstract: 

Agents have crossed a threshold on writing code. They've crossed nothing comparable on the world below it. YAML files, console UIs, copy-pasted snippets, bespoke infra DSLs, and cloud configuration that sit between "it works on my laptop" and "it's running in production." For most developers, that world has always belonged to someone else: a platform team, an SRE rotation, the person on call. That's starting to change, and not just for individual developers. Engineers at every scale are arriving at the same realization that infrastructure is no longer a separate discipline once it's expressed in the same languages the application is. This talk is about what changes when agents can do the full loop instead of just the part that looks like code, where the line between coding and engineering goes from here, and why shipping is about to belong to everyone.
## Community talk notes: 

In the last few years, agents got really good at code, really fast.
We still just write text; the computer does the rest.
In the "new stack", natural language precedes programming language, preceding compiled machine code.

### The hard part isn't the code anymore, it's everything underneath it.
Handling deployment, ClickOps, the under-glue for everything is "the last mile" with a lot of manual work.
For most of us, this part has always been someone else's job such as a platform team, an SRE rotation or the person on call.

The last mile is hard as each model in training saw much more code in distribution than glue work.

### Put the last mile in code, too
Using Infrastructure as Code (IaC) to make the last mile programmable.
"IaC is like git diff, but for your infrastructure"

As the last mile becomes the same language as the app, anyone can ship it. Shipping is no longer a separate team's job anymore.
#### The last mile is code

### Supporting data points
- Agent code quality has climbed fast: on SWE-Bench, scores moved from ~33 (Aug
  '24) to ~94, with the contamination-resistant Pro variant around 78.
- Agents do measurably better when they *act by writing code* rather than
  emitting config — about +20% (from "CodeAct: Executable Code Actions Elicit
  Better LLM Agents").
- Agents now drive ~28% of deployments, up from ~4% late last year.
- Andrej Karpathy: "Building a modern app is a bit like assembling IKEA
  furniture." IaC lets you preview the change before it happens — like a
  `git diff` for your infrastructure — so infra can be reviewed, approved, and
  merged the same way app code is.
