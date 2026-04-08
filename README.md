# biagio-arobba-skills

A public marketplace of Claude skills for deep knowledge work and session continuity.

## Install

In Claude Code, run:

```
/plugin marketplace add barobba/biagio-arobba-skills
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

**Trigger phrases:** "write up this session", "package this conversation", "export this for a new chat", "hand off this session", `/ai-session-handoff`, `/session-handoff`

---

## Contributing

Have a skill to add? Open a pull request with your skill folder under `plugins/` following the existing structure.

## License

MIT
