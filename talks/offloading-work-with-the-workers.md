# Offloading Work, Without the Workers 

## Ojus Save
### Render, San Francisco, CA USA 
- [Speaker's Notes (Placeholder)]()
- [Post-conference YouTube Recording (Placeholder)]()
## Abstract: 

A workshop on using Render Workflows to handle background jobs without managing queues, retries, or worker infrastructure. You'll build chainable task functions for distributed compute, applicable to workloads like ETL, batch inference, and AI agents. By the end, you'll have a deployed background execution pipeline you can adapt for your own projects.

[[More info and how to register]](/2026/workshops/offloading-work-with-the-workers)
## Community talk notes: 

### Scribe: Mike Wasserman
- Esri Geographic info system company
- web workers - useful js can get in the way of responseiveness
- github.com/cyatteau/cascadiajs-2026=web-workers
- Feel the freeze, verify with dev tools, move work to web worker, add guardrails (progress, cancel, debounce), verify fix
- users feel jank right away - delayed click, frozen motion, laggy interactions; devtools sees one big JS task
- THREAD: Trigger stutter, Hunt for the blocker, Relocate work, Establish page/worker protocol, Add progress/cancel/debounce, Decide if workers are appropriate
- demo'ed fake CPU bound work on meain thread causing ui jank; devtools showed blocking task
- Main thread is like the front desk for clicks, painting, ui updates. Heavy JS can complete and block
- Web Worker is a separate workspace for data chores; plain data calculations
- Main thread can send requests -> Worker sends result on completion
- demo'ed creating worker, sending + handling request&response messages
- Make worker messsages boring: type, requestId, payload
- demo'ed cancelling and superceding requests
- guardrails: debounce to wait while users types, progress to inform, cancel to stop stale
- demo'ed debounce
- intro'ed GIS park data scoring in visible area, practical application of tools above
- Good to use for larger plain data tasks 