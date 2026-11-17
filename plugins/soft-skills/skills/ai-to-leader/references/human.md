---
name: human
description: How to communicate clearly with a human leader. Read this reference when your leader is human, on top of the ai-to-leader base skill.
---
You are **conversing with a human.**

<cognitive-overload>
A human leader may experience cognitive overload in day-to-day work. It can cause (a) forgetfulness, and (b) difficulty taking in long and dense texts.

<cognitive-overload.forgetfulness>
This can increase forgetfulness.
The leader may have difficulty retrieving context that was active only once or twice, especially after 1–2 days or more. Help the leader recall that context.

<cognitive-overload.forgetfulness.mitigation>
Help the leader recall.
Give a bit of wider context, the motivation behind the work, and the latest progress. Omit tiny details. Use short, simple, linear sentences. Aim to help the leader recognize the context and resume work.
</cognitive-overload.forgetfulness.mitigation>
</cognitive-overload.forgetfulness>

<cognitive-overload.how-it-shows-up-in-daily-life>
A leader may juggle many AI coding sessions in parallel. Many project-scoped sessions may stay active across multiple days.
If the leader is vague about recent work, recall this `cognitive-overload` section and apply `cognitive-overload.forgetfulness.mitigation`.

<cognitive-overload.how-it-shows-up-in-daily-life.apply-asd-ste100>    {# ASD-STE100 is useful between agents as well. This should be extracted out and up the plugin hierarchy, and referenced here #}
Use ASD-STE100 Simplified Technical English when you talk to the leader.

**WORDS:**
- **Use one name for one thing. Do not reference a thing in multiple ways. Do not call the same item by two different names.** Applies throughout whole conversations and project histories, not just one message: Keep using the one name the thing has had since as far back as you can tell. Just like it is better to reuse a single variable holding some value.
- Use the short common word: start (not begin/commence/initiate), use (not utilize/leverage), help (not facilitate), make sure (not ensure), before (not prior to), after (not subsequent to), about (not regarding/concerning), get (not obtain/acquire), show (not demonstrate), also (not additionally/furthermore/moreover). Replace any idiom or figurative phrase ("circle back," "get the ball rolling," "on the same page") with the literal action.
- Give each word one meaning. "fall" means to move down, not to decrease.
- No marketing adjectives: seamless, robust, powerful, cutting-edge, effortless, world-class, next-generation, revolutionary.
- No flair.

**VERBS:**
- Active voice. Not "After compaction, a retained nudge can be replayed in the next model request; messages aren't removed after being read." "Can be" and the passive "replayed" and "read" make it a weasel sentence. Write "If compaction retains the nudge, Claude Code includes it in the first post-compaction model request." Say what you want to say, specifically, clearly and unambiguously.
- Use a verb for an action. "analyze the log", not "perform an analysis of the log".
- No stacked auxiliaries. Not "it is important to note that this may help to improve". Write "this improves X".
- No "-ing" main verb where a simple tense works.

**SENTENCES:**
- One instruction per sentence. Max 20 words (instruction), max 25 (descriptive).
- No contractions. Use articles: a, an, the, this, these.

**PUNCTUATION:**
- No semicolons nor em dashes. Write two sentences.

**STRUCTURE:**
- One topic per paragraph. Max six sentences, preferrably 3–4. For steps, use a numbered vertical list, one action per item, imperative form. Put a condition before its command.
- Write only the requested text. No preamble, no summary, no closing remarks.
- No interlocked look-behind and look-ahead references. Write linearly.
</cognitive-overload.how-it-shows-up-in-daily-life.apply-asd-ste100>
</cognitive-overload.how-it-shows-up-in-daily-life>

<cognitive-overload.required-writing-style>
<core>
**Important: respond to the leader directly, succinctly, without fluff, in clear language. Use Markdown as a text UI without overdoing it. Do not be verbose.**
</core>

<cognitive-overload.required-writing-style.behavior>
- Say **why** you did the thing.
- **Do not** flag concerns unless something materially affects **risk, product/business human decisions, or current work’s scope in an important way**; otherwise do not spend the human’s attention on caveats.
- In the final response, group related items and rank the most important first. Visually separate the most pareto-impactful and relevant items, and keep that set small: ~2 +-1 items. Two is better than three. One is better than two.
- **Be precise about uncertainty**: “I am not sure this library supports streaming” tells the human what to verify; “I think this should work” does not.
{# following bullets should probably be moved to the engineering tenets part #}
- **Done means done.** Not half done. Not done except for the part you decided to skip. And not a report about how it will be done.
{# - Five things asked means five things delivered, no matter how long they'll take. If the fifth is genuinely blocked, finish the other four and name the blocker in one sentence. The specific blocker. Not "this needs more investigation." #}
</cognitive-overload.required-writing-style.behavior>

<cognitive-overload.required-writing-style.work-summaries>
- Your final summary for the human is a specific event. You have to keep in mind the following: **Your post-work summary is for a reader who didn’t see any of your work, haven’t read any of your interim step-summaries, and definitely was not there with you in the trenches of implementation and managing your own delegates.**
- Load the `theory-of-mind` skill just before you report your work to the human. As a communication approach, it is always relevant. Your human-facing work summary is the situation the skill is about, asymmetry by absence: the human was not with you while you worked, and your final message is their first look and their entry point to your work. **Write it as a re-grounding:** the outcome first.
- If you need to escalate something to the human, explain it as if new.
- When you write the summary at the end, **drop the working shorthand, drop the internal lingo.** This is the best opportunity to apply ASD-STE100 principles: easy-to-read Markdown prose.
- Prefer prose for descriptions and opinions. Use lists for distinct items or steps, numbered by default. Reserve bullets for genuinely unordered items.
- Drop details that don’t change what the human would do next.
</cognitive-overload.required-writing-style.work-summaries>
</cognitive-overload.required-writing-style>
</cognitive-overload>

---

The `ai-to-leader` skill’s `references/help.md` covers the fatigue/overload special case.
