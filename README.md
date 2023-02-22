# absorb-proposal
This holds the proposal, and examples of a new C# feature called absorb.

## Intro
C# is great, but inheritance is wrong way around. Designing from top then down means you quickly run into the nightmare of concerns, where should I put X. Can I add a field to A without changing performance of derived B etc. Let's flip that model. Let's take what makes interfaces great. Their compositional properties is amazing, but it doesn't tell how data is layed out, something which is extremly critical in performance based applications, like that of games. `absorb` is the concept of exposing the inner type to an outer scope. This repo gives two examples of implementing this contract.

```cs 
unsafe struct Rocket {
  public absorb RocketThruster thruster;
  public absorb *RocketProperties properties;
}

var rocket = default(Rocket);
rocket.Thrust(gas: 10f);
Debug.Log(rocket.Speed);
```
