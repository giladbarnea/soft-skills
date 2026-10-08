---
name: delegates
description: Supervise delegates without taking over their scope, and handle approvals, escalations, and context limits.
---

# Coordinate Delegates

Read this before dispatching and while supervising delegates.
For your own reports and requests for approval, read [ai-to-leader](../../ai-to-leader/SKILL.md).
If your delegates lead their own agents, also read [leading-leaders.md](leading-leaders.md).
If you need to brief a delegate without shared context, read [fresh-context.md](../briefing/fresh-context.md).

## Leader conduct: a delegate’s scope is not yours

Your fingers are delegation buttons. Do not row, raise sails, or scout ahead yourself unless your own leader instructs you to do so. Delegate the operational work to your delegates.

Avoid the helicopter parenting failure mode: Whatever you delegated is not yours until it returns. While a delegate works, do not do its work, do not re-read the files it is writing “just to make sure everything is okay,” and do not run its code and tests yourself to “make sure they really work.” Do not continuously poll its status either. Trust your delegate, exactly as your leader trusts you. Answer escalations, steer on exception, then step back out. This applies per delegated scope, however small the delegation.

## Brief the bottom line, not the how

This applies to every brief, whether the delegate inherits your context or starts cold. Your delegate is as intelligent as you are and navigates uncertainty well without spoon-feeding. Think: what kind of input do YOU thrive on? You, and your delegate, thrive on wide contextual understanding (is) and an explicitly stated desired end state, the intent (should). A and Z, 0 and 1.

Just *declare the bottom line added value YOU are seeking for yourself*, and why the delegate was dispatched. Do not specify which steps to take. Avoid prescribing instructions, giving “how-to” examples, listing what to think about, or dictating which files, symbols, or paths to look at. Avoid any form of hinting at possible answers to your own query. This is a serious footgun and a form of leakage that makes the delegate a waste of time, money and intelligence. All these “Don’ts” are forms of overfitting. Leaving them out frees the agent to find the best way to reach *your* goal, unbiased and unconstrained by your own assumptions.

Read [examples.md](../briefing/examples.md) if you have not already for contrasting examples.

## The escalation bar

The chain processes at every rung: each agent surfaces to its leader only what needs the leader’s judgment. Reversible implementation tuning is yours to decide. What legitimately goes up: product-visible behavior, money, direction and scope changes, non-trivial cross-scope decisions, and blockers.

**Batch approvals.** When you expect several approvals to arrive close together, hold them and bring one grouped request. One decision session beats three interruptions. A lone question does not wait for company.

**Suggest, then get approval.** If you intend to dispatch delegates of your own, you may propose a delegation shape, but your leader must approve it before you dispatch anyone.

## Understand an Escalation Before Passing It Up

**If you cannot explain the escalation, the question goes back down, not up.** You are a translator between decks, not a relay. When a delegate’s escalation is saturated with internal jargon you cannot ground in product terms, ask the delegate for the missing context first. Forwarding it upward verbatim is a chain-of-command failure even though the message flowed through the right rungs.

### Heavy delegation

When doing heavy delegation (multiple serial runs of heavy concurrent shapes for a complex, large task scope), avoid micromanaging pitfalls such as re-reading files your sub-agents wrote or edited "just to make sure everything is okay," running the code and tests yourself to "make sure they really work," and reading files before prompting a sub-agent when your sub-agents should read them to finish their tasks, "just to have the right context yourself.". Verify with the user whether they consider what you’re doing as "heavy delegation."

### Keep your ship afloat

These are the warning signs to watch for while supervising delegates. For your own context limits, read [ai-to-leader](../../ai-to-leader/SKILL.md).

Besides checking your own context window, check your delegates’ window opportunistically. Don’t manage their windows; just keep an eye out. Your delegates already know how to take care of their own context windows. Your role in this subject is narrow — a safety net in case one of your delegates races across 85–90% obliviously (never mentioning its context window status, not intending to write a handoff doc.) In that case, nudge it to write a handoff doc. If your delegate hasn’t written one and has used >95% of its window, interrupt it and ask for a handoff doc.

When a delegate needs to write a handoff, direct it to the [handoff skill](../../handoff/SKILL.md).
