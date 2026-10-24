---
name: budget-balancing
description: Agree on usage checks and limits, preserve work at a limit, and switch between pre-approved models.
---

# Budget Balancing

## Agree on usage checks and limits

Ask the human whether to monitor usage. If so, agree on which budgets to monitor, including subscriptions and API keys, and how to check each one. Ask which metrics to watch and what actions to take at each threshold. Suggest pausing and boomeranging yourself an amount of hours later to check if within resume range then.

For subscriptions, calculate burn rate against remaining capacity w.r.t. time until the next reset. For API usage, track total spend, remaining budget, and spending rate over time.

## Pause and preserve work

If a provider is over budget, move work to a pre-approved equivalent model on another provider within budget. Preserve the role.

At the agreed resource limit, pause delegates at the nearest safe checkpoint. Save work in a versioned handoff commit.

For handoff guidance, read [the handoff skill](../../handoff/SKILL.md).
