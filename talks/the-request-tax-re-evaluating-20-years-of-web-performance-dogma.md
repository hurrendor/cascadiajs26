# The Request Tax: Re-evaluating 20+ Years of Web Performance Dogma 

## Alex Moon
### WP Engine, Bellingham, WA USA 
- [Speaker's Notes](https://github.com/moonmeister/request-tax/tree/cascadia-js)
- [Post-conference YouTube Recording (Placeholder)]()
## Abstract: 

For 20 years, we've been told to "Minimize HTTP Requests." But is that still true? I'm investigating how HTTP/3 and QUIC change the "Request Tax" and why I'm seeing patterns where granular fetches beat monolithic queries. Let's look at the data and re-evaluate the rules.
## Community talk notes: 

### How we bundle
- webpack, rollup, etc
- inline CSS/JS
- data URLs in CSS
- ....

Everything to prevent more http requests.
### Why do we bundle?
HTTP/1.1 told us to!

### What about caching?
A single changed line invalidates the entire bundle.

We want to bundle for performance but we want granularity for caching for performance. Code splitting can help us find the balance.
Reference: [HTTP/3 is fast! Blog](https://requestmetrics.com/web-performance/http3-is-fast/)

### What changed under the hood
- **HTTP/2** (SPDY) fixed the HTTP/1.1 problem — but **TCP is still the problem.**
- **HTTP/3 over QUIC** fixed a lot of hard problems… but did we actually *fix* this?
- **Request granularity:** HTTP/1.1 is actually faster when bundling. The more we split and make things smaller, the better HTTP/3 looks; under HTTP/1.1 the overhead of splitting goes up.
- **HTTP/3 is more consistent at delivery**, and HTTP/3 + caching = ❤️.

### Prompts
For the average developer: Optimize for caching, stop stressing about the network
Framework/Bundler maintainers: Is the default app/framework/route still the answer?
Cloudflare: Can you get us more data? Can you follow up on your 2020 article on HTTP/3 performance?
Anyone else: got cool data to share?