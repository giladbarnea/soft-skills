---
name: self-peer-review
description: Dispatch a subagent to review your own committed work
arguments: work_to_review
loads: references/peer-review-instructions.md
---

First, commit your work to have a commit reference. Then dispatch a fresh, flagship subagent (thinking=xhigh if project is medium-sized, thinking=max if large) with the following prompt:

```
The user has given me this task:
<original-user-task>  # Quote verbatim.
{ original user task that resulted in work_to_review }
</original-user-task>

I have attempted to complete it. My work for your review is committed to { commit_sha }.

It touches the systems `A`, `B`, `C` and `D`: `A` publishes an event to `B`, `B` attempts to write to `C` then reports back to `A`, and depending on the report, `A` might talk to `D`.    {# Keep it ultra high-level and brief, like I wrote here. "`A` publishes an event to `B`" is literally enough if that's what `A` does. Do not mention how the systems work. Definitely do not say why they work the way they do. Do not try to be comprehensive. #}

Load the `peer-review` skill and follow its `peer-review-instructions.md` reference.

{ if original user task includes instructions to load skills, documents and context-gathering resources: }
    Load the following skills, docs and resources to gain deep understanding of the review space:
    - `skill-1`: `path/to/skill-1/`
    - `doc.md`: ...
    - ...
```

When the review findings are back, note whether a review item is out of scope, or implicitly makes new design decisions behind the words that might be true, but following them would be scope creep. The reviewer is instructed to surface only real issues, not noise, but there is still place for you to exercise judgment.
