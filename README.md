# `soft-skills`

![Late-shift desk with a terminal showing trusted AI delegation](https://raw.githubusercontent.com/giladbarnea/soft-skills/main/assets/banner.png)

> **Soft skills are the hard part.**

[![Release](https://img.shields.io/github/v/release/giladbarnea/soft-skills?style=flat-square&color=111111&label=release)](https://github.com/giladbarnea/soft-skills/releases/latest)
[![npm downloads](https://img.shields.io/npm/dm/soft-skills?style=flat-square&color=111111&label=downloads)](https://www.npmjs.com/package/soft-skills)
[![Last commit](https://img.shields.io/github/last-commit/giladbarnea/soft-skills?style=flat-square&color=111111)](https://github.com/giladbarnea/soft-skills/commits/main)
![Works with Claude Code, Codex, and Pi](https://img.shields.io/badge/works%20with-Claude%20Code%20%7C%20Codex%20%7C%20Pi-111111?style=flat-square)
![5 skills](https://img.shields.io/badge/skills-5-111111?style=flat-square)
![Made of 100% Markdown](https://img.shields.io/badge/made%20of-100%25%20Markdown-111111?style=flat-square&logo=markdown)
![Built on theory of mind](https://img.shields.io/badge/built%20on-theory%20of%20mind-111111?style=flat-square)
[![MIT license](https://img.shields.io/badge/license-MIT-111111?style=flat-square)](https://github.com/giladbarnea/soft-skills/blob/main/LICENSE)

**Your agents can already code. `soft-skills` teaches them to work: with you, with each other, and for days without you.**

`soft-skills` reverse-engineers how senior engineers work: how they report, delegate, lead a team, and keep a project moving for days.

## This probably sounds familiar

**Your agent reports to you like a toddler:**

- **A wall of text,** written from inside its own head.
- **Terminology** it invented an hour ago.
- **Implementation details** you do not care about.
- **Decisions** it should have made on its own, surfaced to you.

**Your agents work badly together:**

- **The main agent micromanages** its subagent, then replays the subagent's work "just to make sure."
- **It hands a small task to a single subagent.** The task gets a middleman, details get lost in the handover, and the cost doubles.

**Your long runs go nowhere:**

- **You come back after two days.** The agent spent most of them retrying the same fix.
- **The context window ran out at 2 AM,** and you only found out the next day.

## What it unlocks

### 1. An agent you can actually read

`soft-skills` synthesizes principles from cognitive psychology, information design, aerospace maintenance manuals, and hospital handoff protocols. The result:

- **You understand every report on first read,** even after two days away from the project.
- **You stop decoding jargon.** Every report is in plain English, with one name for each thing.
- **Your attention goes only to the decisions that are yours.** The rest gets handled.
- **You answer questions in seconds,** because each one comes with what changed, what was ruled out, and a recommendation.

### 2. Agents that delegate like a good manager

- **Your main session stays sharp for longer.** The noisy work fills other agents' context windows, not its own.
- **Delegates bring back better answers.** They get the goal and the reason, not your assumptions about where the answer is.
- **You pay less for the same work.** Fast, cheap models search. Strong models make the judgment calls.
- **You get fewer interruptions.** Small questions get answered down the chain. You get one grouped decision.

### 3. Teams that run for days without you

- **Teams that talk.** Teammates share findings live, review each other, and converge before they report.
- **Agents that lead agents.** You approve one plan. A lead agent runs sub-leads, and each sub-lead runs its own team.
- **Self-supervision.** Scheduled check-ins catch loops and stalls. When the work is stuck, a fresh model from another provider gives an outside view.
- **Budget awareness.** Agents track subscription and API usage, move to an approved model on another provider, and pause safely at your limit.
- **Clean handoffs.** Before a context window runs dry, the agent writes a handoff with its decisions and reasons. A fresh agent continues without starting over.

## Before and after

### Agent → you

**Before**

> Wired `TokenBucketV2` behind `RL_STRICT` through the middleware shim. Fixed the flaky `test_burst_window` (clock skew in the fixture). Also refactored `limits.py` while I was there and bumped redis-py. Sliding-window edge cases still TBD but should be fine. Want me to also…

**After**

> Rate limiting is live on the public API: 100 requests per minute per client.
>
> **One decision for you:** should paying customers get a higher limit? I recommend 1,000.

### Agent → agent

The main agent needs an explorer subagent to find where rate limiting happens in the codebase.

**Before**

> Find where rate limiting is implemented. You MUST search ONLY these EXACT locations: `server/middleware.py`, `server/limits.py`, `config/redis.yaml`. Do NOT look anywhere else.

*If it knew where to look, it would not need the subagent.*

**After**

> I am about to change how the public API limits clients. Find where rate limiting happens and everything it touches.

### A weekend run

**Before**

> You open the laptop on Monday. The agent tried 31 variations of the same fix, hit the usage limit on Saturday night, and has been idle since.

**After**

> The checkout tests pass. The fix is on the `checkout-retry` branch.
>
> On Saturday the work went in circles, and you were away. I asked an outside model for a fresh view. Its idea worked. Usage stayed under the limit you set.

## Ready-made team shapes

| Shape | Use it when |
| --- | --- |
| **Research fan-out** | Independent questions need one answer. Fast, cheap agents search in parallel. One strong agent connects the dots. |
| **Colloquium** | Parallel research where each finding changes how the others see their own problem. |
| **Pair programming** | Two peers agree on a plan. One builds, the other reviews once. |
| **Hillclimber + watcher** | A measurable target. One agent iterates. A mostly quiet watcher catches tunnel vision. |
| **External advisor** | Several attempts failed. A fresh flagship model looks for the way around the problem. |
| **Fleet** | The work is too big for one team. A lead agent runs sub-leads, and each sub-lead runs a team. |

These are starting points, not fixed structures. Agents adapt them to the work.

## The idea

**`soft-skills` is built on [theory of mind](https://en.wikipedia.org/wiki/Theory_of_mind):**

> In psychology and philosophy, theory of mind (often abbreviated to ToM) is the capacity to understand other individuals by ascribing mental states to them. A theory of mind includes the understanding that others' beliefs, desires, intentions, emotions, and thoughts may be different from one's own.

Every reader of an agent's message was not there while the agent worked. That is true for you, for a delegate, for a teammate, and for the next agent that reads a handoff. **`soft-skills` teaches agents to write for that reader.** The same idea also tells them what to leave out of a brief, so a delegate is free to think.

## The skills

| Skill | Job |
| --- | --- |
| `theory-of-mind` | The foundation: write for a reader who was not there. |
| `ai-to-leader` | Reports and questions to whoever assigned the work. |
| `ai-to-delegated` | Delegation, briefing, team shapes, supervision, and budgets. |
| `handoff` | Pass the work to a fresh agent with decisions and reasons intact. |
| `peer-review` | Fresh-eyes review: proven issues and complexity to remove. |

**Agents load these on their own when the situation fits.**

## `soft-skills` is NOT for you if:

- You easily understand everything your agent tells you.
- You don't know what "Claudish" is.
- You never have "bro what the f*** are you saying right now" moments.
- You never forget what you did in that other AI session.
- You run at most one session at a time, and never for more than a day.

## Install

**Claude Code**

```text
/plugin marketplace add giladbarnea/soft-skills
/plugin install soft-skills@soft-skills
```

**Codex**

```bash
codex plugin marketplace add giladbarnea/soft-skills
codex plugin add soft-skills@soft-skills
```

**Pi**

```bash
pi install npm:soft-skills
```

Then start a new Pi session.

## Only Markdown

No MCP server, no code, no network calls, no hooks, no background process. Your laptop can remain disappointed by the missing daemon.

<details>
<summary><b>Releasing</b> (maintainers)</summary>

Pushing a `vMAJOR.MINOR.PATCH` tag starts the [release workflow](https://github.com/giladbarnea/soft-skills/blob/main/.github/workflows/release.yml).

1. Set the same version in `package.json`, `plugins/soft-skills/.claude-plugin/plugin.json`, and `plugins/soft-skills/.codex-plugin/plugin.json`.
2. Commit and push.
3. Create and push the matching tag:

   ```bash
   git tag -a v1.1.0 -m "Soft Skills v1.1.0"
   git push origin v1.1.0
   ```

CI checks that the three versions match the tag, publishes to npm with [trusted publishing](https://docs.npmjs.com/trusted-publishers), and creates the GitHub release. Branch pushes alone do not publish.

</details>

## License

[MIT](https://github.com/giladbarnea/soft-skills/blob/main/LICENSE).
