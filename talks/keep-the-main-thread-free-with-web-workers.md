# Keep the Main Thread Free With Web Workers 

## Courtney Yatteau
### esri, Alexandria, VA USA 
- [Speaker's Notes](https://github.com/cyatteau/cascadiajs-2026-web-workers)
- [Post-conference YouTube Recording (Placeholder)]()
## Abstract: 

When heavy compute runs on the main thread, the UI stutters. I'll show how to spot main-thread blocking, then move filtering/aggregation work into Web Workers with a clean message protocol, debouncing, progress updates, and cancellation so the UI stays smooth.
## Community talk notes: 
Focusing on the user responsiveness, steps to improving UX
1. Feel the freeze
Indicators include delayed clicks, frozen motion, laggy interactions, one big JS task in DevTools
2. Prove the blocker
Prove that the CPU is waiting on an intensive task.
Use the performance tab to record interaction and view where the blocker is.

3. Move the work
When the main thread freezes, move the work to the worker.
Make worker messages boring. Boring is good when two threads are talking.

4. Add guardrails for the user
   - Debounce - wait until the user is done with their work
   - Progress - inform the user that the work is still happening
   - Cancel - allow the user to stop the work

5. Use the pattern

### "Should I use a web-worker for this?" Check THREAD
- T - trigger the stutter
- H - hunt for the blocker
- R - relocate the worker
- E - establish the protocol
- A - add guardrails
- D - decide where this process belongs


### Main Thread vs Web Worker
The main thread is like the front desk - it handles the experience.
A web worker isn't a second UI. Worker threads can do plain data calculations and sends back the result to the main thread.
A good fit can include plain data that can be data intensive.

### Examples of things to consider on what to render first in GIS
- Size
- Complexity of the data
- Data confidence