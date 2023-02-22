# absorb-proposal
This holds the proposal, and examples of a new C# feature called absorb.

## Intro
C# is great, but composition is wrong way around. Design from top then down means you quickly run into the nightmare of concerns, where should put X. Can I add a field to A without changing performance of derived B. Let's flip that model. Instead let's take what makes interfaces great. Their compositional properties is amazing, but it doesn't tell how data is layed out, something which is extremly critical in performance based applications, like that of games. `absorb` is the concept of exposing the inner type to an outer scope. This repo gives two examples of implementing this contract.
