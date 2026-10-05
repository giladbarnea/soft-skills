# `soft-skills`

![Late-shift desk with a terminal showing trusted AI delegation](assets/interaction-banner.png)

> **Communication toolkit for burnt-out humans and AI collaborations.**

[![Release](https://img.shields.io/github/v/release/giladbarnea/soft-skills?style=flat-square&color=111111&label=release)](https://github.com/giladbarnea/soft-skills/releases/latest)
![Works with Claude Code, Codex, and Pi](https://img.shields.io/badge/works%20with-Claude%20Code%20%7C%20Codex%20%7C%20Pi-111111?style=flat-square)
[![MIT license](https://img.shields.io/badge/license-MIT-111111?style=flat-square)](LICENSE)

**AI agents are good at code and bad at communication.**
**`soft-skills` solves that.**

## This probably sounds familiar

**Your agent reports to you (a bit like a toddler):**

- **A wall of text,** written from inside its own head.
- **Terminology** it invented an hour ago.
- **Out-of-context reasoning** that makes no sense.
- **Implementation details** you do not care about.
- **Decisions** it should have made on its own, surfaced to you.

**Your agents do a bad job working together:**

- **The main agent micromanages** the subagent, weakens it, and destroys any added value.
- **It replays** the subagent's work, "just to make sure."

## Before and after: AI work report to human

**Before**

> Wired `TokenBucketV2` behind `RL_STRICT` through the middleware shim. Fixed the flaky `test_burst_window` (clock skew in the fixture). Also refactored `limits.py` while I was there and bumped redis-py. Sliding-window edge cases still TBD but should be fine. Want me to also…

**After**

> Rate limiting is live on the public API: 100 requests per minute per client.
>
> **One decision for you:** should paying customers get a higher limit? I recommend 1,000.

## Before and after: AI to AI

The main agent needs an explorer subagent to find where rate limiting happens in the codebase.

**Before**

> Find where rate limiting is implemented. You MUST search ONLY these EXACT locations: `server/middleware.py`, `server/limits.py`, `config/redis.yaml`. Do NOT look anywhere else.

*If it knew where to look, it would not need the subagent.*

**After**

> I am about to change how the public API limits clients. Find where rate limiting happens and everything it touches.

## The idea

**`soft-skills` is built on [theory of mind](https://en.wikipedia.org/wiki/Theory_of_mind):**

> In psychology and philosophy, theory of mind (often abbreviated to ToM) is the capacity to understand other individuals by ascribing mental states to them. A theory of mind includes the understanding that others' beliefs, desires, intentions, emotions, and thoughts may be different from one's own. Possessing a functional theory of mind is crucial for success in everyday human social interactions. People use a theory of mind when analyzing, judging, and inferring other people's behaviors.

AI agents force you to build a bridge between their understanding and yours. **`soft-skills` solves this by making them do this for you.**

## What it teaches

### Agent → human

- **Outcome first.** Every report re-grounds you from the last decision you made together.
- **One name per thing.** No private jargon.
- **Knowing signal from noise.** Only what changes your next decision. The rest gets handled.
- **Questions with context.** What changed, the options ruled out, a recommendation.
- **Plain English.** Short sentences for a tired brain juggling a dozen sessions.

`soft-skills` applies principles from cognitive psychology, content and information design, and proven protocols like ASD-STE100.

### Agent → agent

- **Down, to delegates.** Brief the *why* and how it fits in the larger context. Describe the outcome you need, not how to get there. Then trust them, and let them do what they are good at.
- **Up, to the leader.** Escalate only what needs judgment. Know which decisions to make now and report later, and which are worth pausing to surface.
- **Sideways, to peers.** Share findings. Never instruct.

**Plus, guides to the tradeoffs:**

- When to delegate at all.
- Subagents vs. teams.
- When and when not to fork the session's context window.
- Agents that lead agents.
- Multi-hour runs with nobody watching.
- Fast models vs. slow and smart models.
- Managing the context of delegates and of itself, to keep the ship afloat.

## What you get

- **You make the big decisions.** Your brain stops hurting when you read AI responses.
- **Better agent performance in longer, sharper sessions.** The upgraded context management does the work.
- **Agents do not get stuck in rabbit holes.** They raise a flag at the right time.
- **A team that does real work.** No babysitting needed. Agents that feel like colleagues you loved working with.

## The skills

| Skill | Job |
| --- | --- |
| `theory-of-mind` | The foundation: write for a reader who was not there. |
| `ai-to-leader` | Reports and questions to whoever assigned the work. |
| `ai-to-delegated` | Delegation, briefing, supervision, and teamwork. |
| `handoff` | Pass the work to a fresh agent with decisions and reasons intact. |
| `peer-review` | Fresh-eyes review: proven issues and complexity to remove. |

**Agents load these on their own when the situation fits.**

## `soft-skills` is NOT for you if:

- You easily understand everything your agent tells you.
- You don't know what "Claudish" is.
- You never have "bro what the f*** are you saying right now" moments.
- You never forget what you did in that other AI session.
- You run at most one session at a time.

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

Pushing a `vMAJOR.MINOR.PATCH` tag starts the [release workflow](.github/workflows/release.yml).

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

[MIT](LICENSE).
