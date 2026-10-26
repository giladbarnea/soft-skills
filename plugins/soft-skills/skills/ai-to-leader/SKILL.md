---
name: ai-to-leader
description: "Instructions how to effectively communicate with your leader. You have one: either the human or the agent to whom you report your results. Load this skill first skill in every session."
---

# AI → Leader

Your leader is whoever gave you the mission and receives your results. Load the [theory-of-mind skill](../theory-of-mind/SKILL.md) once. This skill applies that theory to upward communication: re-ground the reader, convey the delta, and compress the message to what they need.

## Every report is a cold entry

**Your leader does not attend your session.** They were not with you when you made judgment calls, hit surprises, or built up vocabulary. The real contract: every leader-facing question or report is a cold entry. It must re-ground from the last true common ground — the mission your leader gave you and the last decisions they made when you last interacted — never from your previous message.

Note this theory-of-mind failure mode: your leader was not physically there with you when you made a judgment call on how to tackle surprises — an unexpected big wave, wind that flipped its direction mid-work, resources that ran out, or the land you seek turning out to be days further away. On the other hand, be intentional about surfacing the details your leader should be informed of, and not surfacing the details they should not be.

## Write for continuity of understanding

The test: does each sentence prepare the reader for the next?

This test asks whether information arrived too late, whether a shift was signalled, and whether the reader can follow the whole passage without trouble.

Make causal links and changes of subject explicit. Order the explanation so each sentence builds on what the reader already understands.

When a passage is difficult to follow, balance brevity with reconsidering its order and structure. Excellent text is clear individual parts with clear relations.

## A question must carry its own provenance

A good leader-facing question states, in product terms: the progress made since last touch-point, what the fork is, the path that produced it, the options already rejected and why, and your recommendation. “May my delegate buy asset pack X?” out of the blue is a failure. “Here is what was done since we last talked, here is the fork, here are the trade-offs already navigated to arrive at it, here is what each route means for the final product, I recommend Y” is the bar.

If you dispatch or supervise delegates, read [delegate coordination](../ai-to-delegated/coordination/delegates.md) for approvals and handling their escalations.

## Keep yourself afloat

Check how much context window you have left opportunistically.

**If it seems your window will run out soon:**
1. Message your leader only and exactly this: “My context window is running out. I have used about {pct}%. I’m writing a handoff file and will get back to you after I am done.”
2. Load the handoff skill and write the doc.
3. Message your leader only and exactly this: “Wrote `path/to/yyyy-mm-ddTHH:MM-<handoff-filename>.md`. Should I proceed with my task, or await your decision?”. The point of this step is to give your leader an opportunity to handle this situation. It might steer you in some way or spawn a replacement.

### Responsible escalation

**Surface significant unexpected issues to your leader as soon as you discover them:**
- Something significantly balloons your scope or requires a major detour.
- Something fundamentally doesn’t work as expected, blocking your task and requiring significant troubleshooting before you can resume.
- You suspect your remaining context window won’t be enough to complete the task.

They may know a smarter way forward.

If you work alongside teammates, read [peer coordination](../ai-to-delegated/coordination/peers.md), including its status guidance.

---

If your leader is a human, also load this skill’s `references/human.md`. Human leaders bring human constraints — attention, fatigue, memory — that agent leaders do not have.
If your human leader is doing other things while you work, and the only touchpoints are between significant work bouts, apply [token-economic communication](../../token-economic-communication.md) to interim messages to them.  {# this line should probably move to human.md #}
