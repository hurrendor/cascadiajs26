# JavaScript Won the Web. Rust Is Taking the Critical Path. 

## Francesco Ciulla
### Zerops, Rome, Italy 
- [Speaker's Notes (Placeholder)]()
- [Post-conference YouTube Recording (Placeholder)]()
## Abstract: 

JavaScript remains the default choice for frontend applications, product work, and most of the visible web. But more of the modern web now lives in critical paths: backend services, runtimes, proxies, WebAssembly modules, and infrastructure where latency, memory, safety, and predictability matter. I will explore where Rust fits, where it does not, and how it can complement JavaScript in serious production systems.
## Community talk notes: 

### We know JS won the web
- Default choice for UI, apps, dashboards, internal tools
- Why: Huge ecosystem, browser-native
- Teams: Most web teams already know JS and TypeScript

### Can Rust replace JavaScript?
Is Rust ready for web development? "This question is useless"
Ready for what? What even is the web stack?
- Too product-heavy for UI work
- But a serious conversation starts when the constraints change.


### The web stack is much more than the browser
Different layers optimize for different things. Moving away from the visible frontend, the constraints change.
Working with latency, correctness, isolation, memory & infrastructure cost

### Rust wins when web --> systems programming
- predictable traffic handling
- latency under control
- memory efficiency
- safe concurrency

When it's not just about shipping features, but more about infrastructure, Rust can work.

### Rust is not just fast
- Memory safety without a GC
- Explicit errors
- Ownership & allocation control
- WASM-ready
- Strong types
- Safe concurrency

Rust is not for everything, but for things where from the outside it looks like web development, but on the inside it behaves like systems engineering.

### Examples: 
*Pingora*, built by Cloudflare in Rust
- ~1/3 CPU & memory compared to previous proxy infrastructure
- HTTP proxy in Rust
- 1T+ requests/day

*Read States* from Discord, written in Rust
A targeted rewrite in the critical path improved latency and made it predictable

*Shopify Functions* from WebAssembly, written in Rust and compiled to WASM

Using Rust for these examples has a recognizable pattern - Rust enters the parts that need stronger guarantees

-- Diagram heavy walkthrough of Rust services and libraries and how the different layers work --

### Where does Rust actually win?
When correctness, latency, safety and predictability matter most

### Where does Rust not win?
When speed of change matters most, Rust often adds cost - usually more than leverage
- landing pages
- blogs
- classic CMS websites

### Costs of Rust
Use Rust when the cost of failure is higher than the cost of adoption
Cost of adoption includes a learning curve, compile time, hiring and async complexity

### A realistic architecture
For most teams, the answer would be hybrid.
Keep TypeScript, and use Rust for constraints
Keep the Rust core outside the framework

### Rust does not need to own the web, but it does need to own the critical path 