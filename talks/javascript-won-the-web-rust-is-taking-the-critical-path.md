# JavaScript Won the Web. Rust Is Taking the Critical Path. 

## Francesco Ciulla
### Zerops, Rome, Italy 
- [Speaker's Notes (Placeholder)]()
- [Post-conference YouTube Recording (Placeholder)]()
## Abstract: 

JavaScript remains the default choice for frontend applications, product work, and most of the visible web. But more of the modern web now lives in critical paths: backend services, runtimes, proxies, WebAssembly modules, and infrastructure where latency, memory, safety, and predictability matter. I will explore where Rust fits, where it does not, and how it can complement JavaScript in serious production systems.
## Community talk notes: 

### Scribe: Mike Wasserman
- Rust isn't top choice for product heavy ui work
- More sensible for core application logic with heavy infra/memory/auth reqs
- different layers optimize for different things
  - once you move awai from visible frontend, constraints change
- Rust wins when web -> crticial systems programming
- Advantages beyond speed - mem safe w/o GC, safe concurrency, strong types, explicit errors, ownership and allocation control, etc.
- Cloudflare Pingora -HTTP Proxy in Rust,  1T+ reqs/day, 1/3 mem
- Discord rewrote Read States in Rust (tracks what users have already seen)
  - Fixed latency spikes, Rust offered predictable latency in backend hot path
- Shopify functions - Write in Rust, compile in WASM, strong guarantees
- Web frameworks - Axum, Actix Web
- HTTP Foundations - Hyper, Tower
- DB Layer - SQLx, Diesel, SeaORM
  - ...
- Tokio and Futures - async fn creates a Future (deferred computation), Tokio drives it forward
  - executor/scheduler, reactor for IO, timer, async I/O
- DB Access - SQLx check queries against schema at compile time
  - ORM query builder abstraction over SQL
- Rust wins for realtime services, auth, backend, wasm, etc.
- Rust doesn't win - landing pages, blogs, classic CMS, 3-day MVPs, Frontend heavy apps
- Rust costs - adoption, learnign curve, hiring, async complexity
- Use Rust when the cost of failure is higher than the cost of adoption
- 
