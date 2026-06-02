# Trust, But Verify: Human-in-the-Loop for Agents That Actually Matter 

## Michael Liendo
### Auth0, Davenport, IA USA 
- [Speaker's Notes (Placeholder)]()
- [Speaker's Website](https://www.focusotter.com/)
- [Post-conference YouTube Recording (Placeholder)]()
## Abstract: 

We've built an ecosystem of capable agent. Now let's learn how to make them stop. In this talk we'll walk through various human-in-the-loop patterns. From simple inline confirmations, to out-of-band permission gates, to handing your agent a wallet with real money in it and more.
## Community talk notes: 

### How do we secure things?
*Patterns*
    Pattern #1. Interrupt - ask for mid-task pauses to give preference-based decisions
    Pattern #2. Token vault - Authorize when the agent hits a wall. Give a short lived and scoped authorization.

- Live demo combining both patterns -

Pattern #3 - CIBA (Client initiated backchannel auth)
For when the stakes are too high for a chat reply, such as in financial, medical or legal decisions. On separate devices, etc.
The industry is already doing this, such as with Stripe.

### Match the patterns to the stakes
The higher the stakes, the bigger the external triggers