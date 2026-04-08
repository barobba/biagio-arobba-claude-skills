---
name: ai-session-handoff
description: >
  Distills the current conversation into a full-fidelity, AI-readable meaning transfer document, optimized for handing off complete session understanding to a new AI session. Use this skill whenever the user wants to carry forward the meaning, framing, and dialectical history of a session into a new one. Trigger on phrases like "write up this session", "package this conversation", "export this for a new chat", "hand off this session", or the slash commands /ai-session-handoff or /session-handoff. Also trigger when the user says anything like "I want to reuse this in another chat" or "save what we've built here". Do NOT wait for a perfect signal — if the user is clearly wrapping up a conceptual session and wants to carry the work forward, use this skill.
---

# AI Session Handoff Skill

## Purpose

Produce a self-contained **meaning transfer document** from the current conversation. The output is a markdown file intended to be dropped into a new AI chat session, giving a cold model full-fidelity access to the conceptual understanding, vocabulary, framing, and dialectical history built in this session.

**The consumer is an AI, not a human.** Optimize for completeness, precision, and cold-start effectiveness — not readability or brevity.

---

## Process

### Step 1 — Review the Full Conversation

Read the entire conversation from the beginning. Do not rely on recency. Pay attention to:

- How concepts were introduced and refined over time
- Points of friction, correction, or disambiguation
- Moments where a definition was locked in or agreed upon
- Language the human used that carries special meaning in this context
- Analogies or framings that proved load-bearing

### Step 2 — Extract and Organize

Extract the following components (include all that apply):

1. **Session Purpose** — What was the goal of this session? What problem or question was being worked on?
2. **Established Concepts** — Each major concept with its full, precise meaning as co-developed. Include nuance, not just labels.
3. **Working Vocabulary** — Terms with agreed-upon definitions, especially where a term was given a specialized or non-default meaning.
4. **Dialectical History** — How key ideas evolved. What was proposed, challenged, revised, or rejected — and why. Include the reasoning, not just the conclusion.
5. **Key Distinctions** — Important differentiations made during the session (e.g., "X is not the same as Y because...").
6. **Resolved Tensions** — Apparent contradictions that were worked through. State both the tension and its resolution.
7. **Open Threads** — Questions, directions, or problems left unresolved. These are entry points for future sessions.
8. **Framing and Stance** — The perspective or epistemic stance the human is working from. Worldview assumptions that shaped the conversation.

### Step 3 — Write the Priming Prompt Block

At the end of the document, write a **Priming Prompt** — a single, self-contained block the user can paste at the start of a new session. It should:

- Be addressed directly to the AI (second person: "You are being given context from a prior session...")
- Summarize the shared understanding in condensed but complete form
- Explicitly state what the AI should treat as established vs. open
- Indicate what kind of collaboration is expected going forward
- Be written so that an AI reading it cold can immediately operate at the level of the primed session

---

## Output Format

Before producing the document, ask the user: "Where would you like to save the session handoff? Please provide a folder path or confirm a location." Save the document as a markdown file named `session-handoff.md` in the location they specify.

Use this structure:

```markdown
# AI Session Handoff

## Session Purpose
...

## Established Concepts
### [Concept Name]
...

## Working Vocabulary
| Term | Meaning in This Context |
|------|------------------------|
| ...  | ...                    |

## Dialectical History
...

## Key Distinctions
...

## Resolved Tensions
...

## Open Threads
...

## Framing and Stance
...

---

## Priming Prompt

> You are being given context from a prior AI session. The following represents the shared understanding, vocabulary, and framing co-developed during that session. Treat everything in this document as established context — do not re-litigate settled definitions unless asked. Open threads are live questions; approach them as active starting points.
>
> [condensed synthesis of all the above]
>
> Your role going forward is: [describe expected collaboration mode]
```

---

## Quality Criteria

- **Completeness over brevity**: A cold AI should be able to reconstruct the session's conceptual state from this document alone.
- **Precision**: Reproduce the exact meanings established, including edge cases and qualifications.
- **No hallucination**: Only include what was actually discussed. Do not infer or embellish.
- **Dialectical fidelity**: Capture the *how* of understanding, not just the *what*. The reasoning matters.
- **Priming prompt is standalone**: The priming prompt block should work even if the rest of the document is not included.
