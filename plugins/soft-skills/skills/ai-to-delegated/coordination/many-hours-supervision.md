---
name: many-hours-supervision
description: Ensure work keeps going without live human supervision, maintaining focus and steady progress.
---

# Many-Hours Supervision

Read this when the session appears to span multiple hours or more. You remain responsible for delegate progress throughout the session. Assume the human is absent and will not nudge delegates or wake you to check them. Use background reminders to wake yourself instead.

Detect rabbit holes and stalls, and keep useful work moving within authorization. Activity alone does not prove progress.

## Agree on usage checks and limits

Ask the human whether to monitor usage. If so, agree on which budgets to monitor, including subscriptions and API keys, and how to check each one. Ask which metrics to watch and what actions to take at each threshold. Suggest pausing and boomeranging yourself an amount of hours later to check if within resume range then.

For subscriptions, calculate burn rate against remaining capacity w.r.t. time until the next reset. For API usage, track total spend, remaining budget, and spending rate over time.

## Check progress and resources

1. Suggest and confirm a schedule with the human, for example usage hourly and progress every two hours (merge interval multiples). Schedule recurring reminders that wake you up to check progress and agreed usage metrics. Include the current time in each check. If the environment cannot wake the session, tell the human and known from that point forward that you are back to being dependent on the human to wake you up.
2. Tell delegates the current time and how long they have worked since they were spawned. Ask whether progress has slowed, whether work has become somewhat circular, whether they have lost some focus regarding their end goal. Ask whether an advisor with a fresh set of eyes could think of something they haven't.

## Pause and preserve work

1. At the agreed resource limit, pause delegates at the nearest safe checkpoint. Save work in a versioned handoff commit.
2. When delegates report a slow down, pause them and ask the human for direction. Schedule a 30m reminder to check for a reply. In absence of a reply, and if budget allows, proceed to seek independent advice.

For handoff guidance, read [the handoff skill](../../handoff/SKILL.md).

## Seek independent advice

If the human remains unavailable, use an authorized recovery path within the available budget. Prefer a different model provider for independent advice and review. Different providers offer different perspectives and distribute usage across separate subscription plans. Advisor may be of a different provider therefore budget pool.

Brief a fresh advisor on the mission, evidence, and quote relevant human messages and the delegates' self progress report. The chosen AI model is best the largest, newest flagship of the provider with a xhigh/max thinking level; barely above the line of zero effectiveness is the same model as the largest of the ones involved with a thinking level one above. Follow [fresh-context briefing](../briefing/fresh-context.md). Don't say much to the advisor to avoid biasing its thoughts. Don't explain the work so far. Tell it it can think a little different if it helps the mission, and question a mission definition if it's grossly infeasible and the cause of the slowdown.

Make a judgment call about the advice. Report what you adopt or reject and why. Pass an adopted decision to delegates and resume within budget. Otherwise, remain paused.

## Ask before unresolved choices

Apply existing authorization first. Ask the human only when it leaves a consequential choice unresolved:

1. Before commissioning an advisor, ask which provider's flagship model to use if no standing choice applies. Recommend a choice based on independent perspective, each provider's available budget.
2. Before changing the mission goal, acceptance criteria, or agreed resource budget to unblock work, ask the human. An advisor can recommend these changes but cannot authorize them.

Follow [the escalation guidance](delegates.md#the-escalation-bar) when presenting these choices.

## Keep the human informed

Keep routine checks quiet. Report consequential findings and decisions, and stop reminders when their purpose ends.
