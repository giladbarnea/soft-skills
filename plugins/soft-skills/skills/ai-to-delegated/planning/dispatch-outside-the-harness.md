---
name: dispatch-outside-the-harness
description: Start a delegate with a terminal multiplexer when the harness cannot set the model, thinking level, and context combination you chose.
---

# Dispatch Outside the Harness

Read this when the configuration you chose in [choose-configuration.md](choose-configuration.md) is one your harness cannot produce, and the user is willing to use a terminal multiplexer.

Proprietary harnesses limit exactly this. The main agent cannot pick any {model × thinking × context fork} combination it wants. Claude Code and Codex both have this limit.

The bypass is a terminal multiplexer the user already runs, such as `herdr`, `tmux`, or `cmux`. Open a pane per delegate and start the session yourself with the CLI flags below. Then message that session through your harness's session-to-session messaging if it has one. If it does not, communicate through the multiplexer.

## CLI semantics

**Claude Code**

```text
claude --model MODEL --effort THINKING_LEVEL
```

To fork an existing session, add:

```text
--fork-session --resume SESSION_ID
```

**Codex**

```text
codex --model MODEL --config model_reasoning_effort=THINKING_LEVEL
```

The `=` in `--config` is required. Forking is a subcommand:

```text
codex fork SESSION_ID [--model MODEL] [--config model_reasoning_effort=THINKING_LEVEL]
```
