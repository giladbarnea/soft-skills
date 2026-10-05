# Soft Skills

![Late-shift desk with a terminal showing trusted AI delegation](assets/interaction-banner.png)

> **Communication toolkit for burnt-out humans and collaborative AI's.**

[![Release](https://img.shields.io/github/v/release/giladbarnea/soft-skills?style=flat-square&color=111111&label=release)](https://github.com/giladbarnea/soft-skills/releases/latest)
![Works with Claude Code, Codex, and Pi](https://img.shields.io/badge/works%20with-Claude%20Code%20%7C%20Codex%20%7C%20Pi-111111?style=flat-square)
[![MIT license](https://img.shields.io/badge/license-MIT-111111?style=flat-square)](LICENSE)

## Five skills keep the work usable

- **`theory-of-mind`** restores common ground with readers whose context differs from yours.
- **`ai-to-leader`** makes answers to your leader — human or AI — clear and simple.
- **`ai-to-delegated`** makes delegation and collaboration work.
- **`handoff`** carries decisions, tacit knowledge and "why" into the next session.
- **`peer-review`** collapses complexity like tetris blocks.

**When nobody can understand it, delegate it, resume it, or review it, it's not working.**

## Pleasant to the brain

`ai-to-leader`: 
- uses ASD-STE-100, plain language and stable names.
- assumes the human has one brain, and is juggling work, family, and a dozen unfinished AI projects.
- teaches sub-agents how to manage up their main.
- teaches signal vs noise: what to surface to your leader and what to solve without making a fuss.

## Delegation that doesn't suck

`ai-to-delegated`:
- makes AI delegate, not micro manage.
- teaches trust, avoiding biasing your directs, and how to scope parallel work effectively.

## Handoffs that preserve judgment

`handoff`:
- captures intent, pitfalls, decisions and the rationale behind them.
- leads the next agent from a fresh spawn to a fully onboarded replacement.

## Reviews that simplify

`peer-review`:
- studies the work with a fresh set of eyes and a wide look.
- reports proven issues.
- points out opportunities to collapse complexity, remove code, and gain elegance.

## Install

### Claude Code

```text
/plugin marketplace add giladbarnea/soft-skills
/plugin install soft-skills@soft-skills
```

### Codex

```bash
codex plugin marketplace add giladbarnea/soft-skills
codex plugin add soft-skills@soft-skills
```

### Pi

```bash
pi install npm:soft-skills
```

Start a new Pi session after installation.

## Usage examples

**`ai-to-leader`:**

```
# User:

  /ai-to-leader i have had a long day. what are you talking about


# Assistant:
  
  We've been designing a plugin that makes AI's effective communicators.

  It packages five skills: `theory-of-mind`, `ai-to-leader`, `ai-to-delegated`, `handoff`, and `peer-review`.

  `theory-of-mind` provides the shared foundation. The other four skills cover reporting, delegation, handoffs, and reviews.

  The plugin is almost ready for release. I only need your decision on how to package it for Pi, since Pi does not support plugins natively.
  
  I can either package it as a single `soft-skills` skill, or as five separate skills. Which do you prefer?
```

**`ai-to-delegated`:**
```
# User:

  study the plan and implement it. delegate work.

# Assistant:

  [loaded skill: `ai-to-delegated`]

  I’ll assign research, implementation and review to separate sub-agents. This will prevent biasing the process.

  I will only surface issues that need your attention. Finally, I will plainly summarize the end result.

  Go take a break. We’ll manage.
```

## Only Markdown

The installed `soft-skills` plugin has no MCP server, executable code, network calls, hooks, or background process. Your laptop can remain disappointed by the missing daemon.

Pi installs the same `plugins/soft-skills` tree as a [Pi package](https://pi.dev/packages). The root `package.json` points Pi to its `skills` directory, so all three agents read identical files.

## Release from a version tag

Pushing a `vMAJOR.MINOR.PATCH` tag starts the [release workflow](.github/workflows/release.yml).

1. Set the same version in `package.json`, `plugins/soft-skills/.claude-plugin/plugin.json`, and `plugins/soft-skills/.codex-plugin/plugin.json`.
2. Commit and push.
3. Create and push the matching tag. For version `1.1.0`:

   ```bash
   git tag -a v1.1.0 -m "Soft Skills v1.1.0"
   git push origin v1.1.0
   ```

CI checks that all three manifest versions match the tag. It then publishes `soft-skills@1.1.0` to npm and creates the **Soft Skills v1.1.0** GitHub release.

npm publishing uses [trusted publishing](https://docs.npmjs.com/trusted-publishers) from this workflow. No secret is required. Branch pushes alone do not publish releases.

## License

[MIT](LICENSE).
