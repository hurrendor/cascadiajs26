# Shared Components Beyond the Design System 

## Jonathan Keslin
### Atlassian, Kirkland, WA USA 
- [Speaker's Notes (Placeholder)]()
- [Post-conference YouTube Recording (Placeholder)]()
## Abstract: 

Lots of companies have design system component libraries these days, but those aren't the only shared components around. This talk will center around higher-level shared components for those more complex common UI elements, including how to architect them for reusability, how to ensure they're flexible enough for novel use, and how to govern contributions.
## Community talk notes: 


### Scribe: Mike Wasserman
- Desgin System: UX foundations
- Go beyond design system for nav and higher level ux, team custom, etc.
- Start deciding who you're building for (first consumer)
  - Keep another customer in mind, to ensure you're not overfitting
- Next decide where to build - separate from app (other repo or folder)
  - Publish artifacts
- Build components with a higher standard than app code, for wider reuse
  - Build up from design system
  - Make APIs consistent with platform - addative from basic 
  - Design with layered extensibility - make the right way the easy way wit hsensible defaults
    - Offer layers of customization 
    - example of Jira's navigation
    - Applies to backend too with GoDaddy reverse proxy + microservices 
- Optimize for higher layers
  - prioritize common cases, educate (spotlight tour)
  - offer customization layers, but don't get carried away
  - GoDaddy dropdown became a homer car (features for each client)
- It's okay to be opinionated: don't let components become dumping grounds
  - Teams build with parts a bit differently from each other
  - Build a holistic shared component for more consistency
- Include batteries to reduce boilerplate, encapsulate complexity, but offer escape hatches
- Make components maintainable, add tests to ensure it's reliable, document liberally
  - Docs even help AI use your component, so they don't need to reverse engineer
  - Keep a change log
  - Make usage self-service
- Foster an ecosystem
  - Shared components are super valuable
  - Build a doc site
- Provide governane
  - Recognize authors and maintainers and incentivize effort
   