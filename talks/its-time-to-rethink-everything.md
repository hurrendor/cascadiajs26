# It's time to rethink everything 

## Theo
### T3 Chat, San Francisco, CA USA 
- [Speaker's Notes (Placeholder)]()
- [Post-conference YouTube Recording (Placeholder)]()
## Abstract: 

We spent decades building awesome tools for developers. Languages, frameworks, clouds, and more. They're great for humans. They're not so great for devs. What happens if we throw it all away and start from scratch?
## Community talk notes: 

### Life before the Cloud
1. Building was capital-intense
2. You had to predict the future
3. Experimentation was expensive

### Life after the Cloud
1. You can start small and scale up
2. Experimentation is cheap
3. You don't need to hire god-tier infra devs anymore

Now, we have life before and after The Claude. 
Life before The Claude mirrors before the Cloud.

In git management...
#### Why can't we commit .env files?
Why can't I have a file in my codebase that only my team has access to?
Why can't a public repo have private parts?

In file systems...
Why can't a file be in two folders at once?
Why do we need a file system to compile my app?

Why do we assume our codebases still matter at this point?
The code itself is valuable as a resource for the agents, but doesn't matter the way it used to matter.

### Things are very different now, but we still act like things are the same
Why can't we rebuild everything?
If we took the opportunity that we have right now to challenge the foundations of the platforms we build on, what could it look like?

Covering a range of things are possible now with agents, while the depth of the features can be handled by individual companies using your product

### Cloud, then Claude
Building software is *way* different now — not because of ~~AI~~ the cloud. Easy scaling made a lot of things possible: Amazon-tier hardware without an Amazon-tier budget. And AI is the same move again — we've been through this before. Expertise required is a lot less now; things that were rigid aren't true anymore.

### Breadth vs. depth (the Salesforce problem)
Salesforce is the opposite of all of this: tons of features. Everyone needs a small number, the Fortune 500 needs some, and then there's the long tail that 1% of users touch. You have to build for every snowflake… or do you?
- **Breadth of features** — range.
- **Depth of features** — number of features in a given area.

Too broad? Hard. Too deep? Not good. But covering a *broad range* trivially is viable now — the depth isn't the problem; build a platform and let the client handle depth with their agents.

### What does this look like?
- **Before:** build ~40 hours, deploy ~3 hours.
- **After:** build ~30 minutes, deploy ~3 hours — so now the 3-hour deploy sucks even worse.

[shoo.dev](https://shoo.dev/) does auth in 2 lines of code — an easy way to add auth (not necessarily secure or good); it didn't ship because it was built too deep in the vertical. So: **boil the ocean** — make all the problems go away. Theo went too far and built [Lakebed](https://lakebed.dev/) `[alpha]`.

**Live demo:** `npx lakebed new sup-seattle` (nothing special on his machine), then `npx lakebed deploy` — deployed just like that; change something, redeploy in seconds. He built the language, compiler, CLI, and deployer. We kid ourselves that we need all the perfect things — just prompt something into existence.

### The point
Find the place where you feel *stupid* for going so big. Where will things be in 5 years? The last 5, 10, 50 years don't matter. **You aren't building big enough.**