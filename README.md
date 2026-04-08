# biagio-arobba-skills

[![Version](https://img.shields.io/badge/version-0.1.0-blue.svg?style=for-the-badge)](https://github.com/barobba/biagio-arobba-claude-skills)
[![License](https://img.shields.io/badge/license-MIT-green.svg?style=for-the-badge)](https://github.com/barobba/biagio-arobba-claude-skills/blob/main/LICENSE)
[![Claude Code](https://img.shields.io/badge/Claude_Code-Plugin-purple.svg?style=for-the-badge)](https://github.com/barobba/biagio-arobba-claude-skills)

A public marketplace of Claude skills for deep knowledge work and session continuity.

## Install

In Claude Code, run:

```
/plugin marketplace add barobba/biagio-arobba-claude-skills
```

---

## Skills

### `ai-session-handoff`

Distills a conversation into a full-fidelity, AI-readable meaning transfer document — designed to hand off complete session understanding to a new AI session.

**What it does:**
- Reviews the full conversation from the beginning
- Extracts established concepts, working vocabulary, dialectical history, key distinctions, resolved tensions, and open threads
- Produces a `session-handoff.md` file optimized for a cold AI to resume the session at full fidelity

**The output is designed for an AI, not a human.** It prioritizes completeness and precision over brevity.

**Design philosophy:**
This skill is built for purposeful sessions — conversations where understanding was actively constructed, not just exchanged. That might be building up a shared mental model of a concept, developing a vocabulary around a domain, or working through a problem with enough depth that the *how* of the thinking matters as much as the *what*.

The core insight is that a session's meaning is more than its context window. A summary loses the dialectical history — what was proposed, challenged, revised, and why. A transcript is too noisy. This skill produces something in between: a precision artifact that captures the intellectual state of the session so a cold AI can resume at full fidelity, without re-litigating settled ground.

If your session was a task log or a series of one-off questions, this skill isn't for you. If you built something together and want to carry it forward, it is.

**Trigger phrases:** "write up this session", "package this conversation", "export this for a new chat", "hand off this session", `/ai-session-handoff`, `/session-handoff`

---

## License

MIT
