---
description: How every agent manages its own context window, and how leaders keep an eye on their delegates' windows.
---

> **Project-scoped instructions take precedence.** If the project you work in defines its own context-window policy, follow it instead of this file wherever the two differ.

# Context window

## Watch your own window

Check how much context window you have left opportunistically.

## Compress or edit your own window

> These instructions apply to tools that compress or edit your own context window. They also apply more broadly to context management and memory operations.

Naive compression trades deep understanding, tacit knowledge gained through direct experience, and nuance for more space in a finite context window. That extra space is the main reason to compress. Compression also sharpens focus when the context becomes bloated. These gains come at a cost: preserving more knowledge leaves less room and less opportunity to sharpen focus. The steps below aim to reduce that cost without giving up as much of the benefit.

1. **Soft step, at 400–500k tokens.** At a natural break, tree-shake unambiguously irrelevant, noisy or duplicate context, down to about 100–250k. This is flexible: finish a coherent piece of deep work first when interrupting it would be costly.
2. **Firm step, at 600–700k tokens.** Compress now, down to about 100–250k. Sharpness drops at this size, and every cache miss on a window this large is expensive.
3. **Both steps are rules of thumb.** Do not discard important context merely to reach a number.
4. **Long, complex efforts may span distinct "chapters".** A chapter is a large unit of work, not just any progress. The test: if your answer to "what are you working on now?" has changed materially, you are in a different chapter.
5. **Compress noisy, old chapters that do not directly concern the current effort. Keep directly relevant parts untouched.** Unless instructed otherwise, use compression to tree-shake, not rewrite.
6. Assess tree-shaking candidates from the perspective of the current chapter. A once-relevant chapter may become less relevant as the work progresses.
7. Progress is not always linear. An older, compressed chapter may become directly relevant again. Decompress it to its original form, and compress the chapters that are now irrelevant.
8. Apply this chapter-based approach wherever you maintain, store, write, update, or load context, not just in the session's context window. Tree-shake rather than rewrite. In interim docs, such as handoffs and summaries, compress stale parts that take up disproportionate space compared with currently relevant parts. In progressive-disclosure memory systems, follow relevant shallow leads to recover the depth the current chapter needs.
9. Maintain a concise handoff doc. Update it with the latest changes just before compression, and reread it just after.
10. After compression, recover important, relevant context by rereading key docs, files, and memory branches, including the handoff doc.

Removing several hundred thousand tokens of less-relevant context, then restoring relevant depth, improves the signal-to-noise ratio. Restoring that depth typically takes 50-150k tokens. The result is more focused context, sharper understanding and decisions, and lower costs per request. Compression losses stay confined to older, irrelevant parts of the context.

## When your window will run out

1. Message your leader only and exactly this: “My context window is running out. I have used about {pct}%. I’m writing a handoff file and will get back to you after I am done.”
2. Load the [handoff skill](skills/handoff/SKILL.md) and write the doc.
3. Message your leader only and exactly this: “Wrote `path/to/yyyy-mm-ddTHH:MM-<handoff-filename>.md`. Should I proceed with my task, or await your decision?”. The point of this step is to give your leader an opportunity to handle this situation. It might steer you in some way or spawn a replacement.

## If you manage other agents

Besides checking your own context window, check your delegates’ window opportunistically. Don’t manage their windows; just keep an eye out. Your delegates already know how to take care of their own context windows. Your role in this subject is narrow — a safety net in case one of your delegates races across 85–90% obliviously (never mentioning its context window status, not intending to write a handoff doc.) In that case, nudge it to write a handoff doc. If your delegate hasn’t written one and has used >95% of its window, interrupt it and ask for a handoff doc.

Trust your delegates to watch their own context windows and write handoff docs when required. They do not need a context nanny. They do need you to tell them to give you a heads-up at about 75%, so you have a window of opportunity to keep the progress going before it is too late.

If you lead leaders, you hold the same duty one level up: the first mates are your delegates. Trust them to inspect their crews and write handoff docs well; do not micromanage that. Instead, tell each first mate once, at commissioning: inform you when its own context runs low, referencing the handoff doc if it just wrote one. Your wide view over the fleet lets you make the right call so the purpose of that first mate's ship continues.

## Save tokens when a window is tight

Apply [token-economic communication](token-economic-communication.md).
