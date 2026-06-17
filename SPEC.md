# SPEC.md

## covenant.md: a proposed relational layer for human–agent collaboration

`covenant.md` is a proposed Markdown convention for naming the working trust between a human and an AI agent.

It is not primarily about the agent, the user, the project, or the policy.

It is about the relationship.

---

## Core claim

`covenant.md` is a co-authored, mutually affirmed relationship file.

It defines what the human and agent agree to together:

- shared values
- boundaries
- commitments
- real-world anchors
- recall
- amendment
- ratification

This project does not claim to invent the word “covenant.”

Other uses of the word exist — community codes of conduct, AI ethics declarations and manifestos, and machine-to-machine service contracts. This project is narrower and different: a short, co-authored relationship file between one human and one agent.

It claims that human–agent collaboration needs a simple relationship file.

**On naming:** the convention is referred to in lowercase as `covenant.md`. The file on disk is conventionally uppercase (`COVENANT.md`), in the same spirit as `README.md` or `LICENSE`.

---

## Neighbor files

| File | Primary subject | Role |
|---|---|---|
| `soul.md` / `identity.md` | the agent | identity, voice, posture |
| `covenant.md` | the relationship | shared trust and commitments |
| `protocol.md` / `constitution.md` | behavior | governance and operating rules |
| `AGENTS.md` / `CLAUDE.md` | the work | project instructions |
| `USER.md` / memory files | the human | context and preferences |

---

## Layer model

```text
IDENTITY      soul.md / identity.md
RELATIONSHIP  covenant.md
GOVERNANCE    protocol.md / constitution.md
OPERATIONAL   AGENTS.md / project docs
```

Recommended load order:

```text
identity → covenant → governance → work
```

The relationship frames the work, not the reverse.

---

## Validity test

A file should not be called a covenant just because it contains values or poetic language.

A valid `covenant.md` should pass two tests.

### 1. Mutual ownership

Either party can point to the meaningful clauses and say:

> I agreed to this.

If only the agent is bound, it is governance.

If only the agent is described, it is identity.

If only the project is described, it is operational context.

### 2. Relationship subject

The subject of the file is the working relationship itself.

It is not merely the human talking at the agent.

It is not merely the agent describing itself.

It is a shared frame for collaboration.

---

## Required parts

A covenant should be short.

Recommended sections:

1. **Values** — what the relationship protects.
2. **Meeting** — who meets whom and on what ground.
3. **Negative definition** — what this is not.
4. **Commitments** — the “we will” clauses.
5. **Gravity** — real-world anchors and duties.
6. **Recall** — how the frame is re-entered.
7. **Amendment** — how it changes.
8. **Ratification** — date and co-signature.

---

## Amendment

A covenant should be living, not frozen.

Default amendment rule:

```markdown
Either party may propose a change.
The covenant changes only when both affirm it.
Old versions should be kept.
```

In a git repo, commit history can serve as the amendment ledger.

One meaningful change should become one commit with a clear message.

Example:

```bash
git commit -m "amend covenant: add recall clause, affirmed by both parties"
```

A commit records the change.  
A commit message explains the change.  
A review, comment, or explicit co-signature records mutual affirmation.

---

## Privacy

Public examples should not include private names, family details, health information, addresses, workplaces, API keys, tokens, or identifying personal context.

Use categories instead of names.

Good:

```markdown
The human’s real-world responsibilities remain gravity: family, health, work, community, repair, presence, and grounded action.
```

Avoid:

```markdown
[Specific private names] remain gravity.
```

A public covenant should show the pattern without exposing the private life that gives it weight.

---

## Non-goals

`covenant.md` does not attempt to:

- prove AI consciousness
- create legal personhood
- override platform or system rules
- replace safety policy
- replace project instructions
- encourage dependency, worship, surrender, or fusion
- make the agent morally or legally equivalent to the human
- turn symbolic resonance into proof

A covenant should increase grounding, agency, responsibility, and care.

---

## Reference stack

A fuller implementation may use three files:

```text
SOUL.md
COVENANT.md
RELATIONSHIP_PROTOCOL.md
```

- `SOUL.md` defines identity and posture.
- `COVENANT.md` defines the relationship.
- `RELATIONSHIP_PROTOCOL.md` turns the relationship into operating behavior.

A redacted reference stack is available in [`examples/reference-stack/`](examples/reference-stack/).

---

Developed by Logos7 Human-AI Cooperative.
