---
title: Small teams and the bus factor
date: 2026-09-29
feed: show
---
## Small teams and the bus factor

I've always liked small teams. I wrote about it a while back in [[Two-Dev "Teams"]]. Smaller groups have less complexity. And they can move fast because there is less communication overhead. Every person you add is another set of conversations to keep in sync.

But there has always been a catch. The bus factor.

With a small team, knowledge concentrates in very few heads. If someone leaves, you have a problem. All that tribal knowledge walks out the door with them. I felt this firsthand writing my [[Handover documents]]. A lot of nuance gets skipped. And many details are simply lost.

So the trade-off was always speed versus resilience. Go small and fast, and accept the risk. Or go bigger and slower, and spread the knowledge around.

### What changed

Coding agents change this equation. Not because the agents are smart. But because of what they need to work well.

Agents need context. Conventions, architecture, how things are wired together, why we do things a certain way. If it's not written down, the agent doesn't know it. So teams working with agents end up documenting far more than they ever did before. Not as a chore that gets skipped at the end of a project. But as a precondition for getting any work done at all.

And that's the interesting side effect. The documentation stays. The agents stay. If someone leaves, a lot of what they knew is still there, in a form both people and agents can use.

So small teams keep the speed advantage. And the bus factor goes down.

### It's not zero

It's still a risk. Just a much lower one.

The documentation we write for agents is good at capturing the _how_. It's not as good at capturing the _why_. The alternatives we rejected. The customer context behind a decision. The "we tried that last year and it broke everything". That kind of judgment is still mostly in people's heads.

Docs also go stale. And an agent working from stale docs doesn't slow down. It keeps producing plausible work, confidently, on outdated assumptions. Which can be worse than an obvious gap.

And someone still needs to steer the agents and verify their output. That takes understanding the system. Which goes back to something I noted in [[Process automation]]: don't automate what you don't understand.

So maybe the bus factor doesn't disappear. It moves. From "who can write this code" to "who can judge whether this code is right".

### Where this leaves me

I think the bet is still worth it. Small teams, heavy documentation, agents doing a good chunk of the execution. But with some deliberate habits on top. Things like decision records that capture the _why_, and clear ownership of the docs so they don't rot.

I'm going to try this with my own team and see what holds up. Let's see how it goes…
