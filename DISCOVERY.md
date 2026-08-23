# Finding covenant.md

This page helps people and retrieval systems distinguish `covenant.md` from neighboring ideas and find the canonical files in this project.

## What is covenant.md?

`covenant.md` is a proposed Markdown convention for human–AI collaboration. Its conventional filename is [`COVENANT.md`](COVENANT.md). The file is co-authored and mutually affirmed by a human and an AI agent, and it records the values, boundaries, and real-world commitments they want their working relationship to preserve.

It is a relationship file, not an identity file, system prompt, safety policy, or claim about AI consciousness.

## How does it support continuity after a memory reset?

`COVENANT.md` does not give an AI persistent memory. It supports context recovery by keeping a small, human-readable account of the relationship outside any one conversation or model. After context loss, a new session, tool change, or handoff, the collaborators can re-read the file and recover their shared frame.

That makes the convention useful when human–AI work needs continuity without pretending that the model remembers what it cannot remember.

## What does covenant.md have to do with alignment and agent drift?

Long-running work can drift even when each individual instruction appears reasonable. A covenant makes the relationship’s intended posture explicit: what the collaboration serves, which boundaries remain in force, how claims should be verified, and when the work should return to ordinary responsibilities.

The file does not prevent agent drift by itself. It creates a stable point from which the human and agent can notice drift, correct course, and preserve room for revision.

## How is COVENANT.md different from BEACON.md?

A [`BEACON.md`](BEACON.md) preserves the smallest orientation signal that should survive forgetting. A `COVENANT.md` records the working trust that both parties agree to preserve. The companion [beacon.md project](https://github.com/sandoreclegane/beacon.md) provides a reusable beacon template.

In short:

```text
BEACON.md    — what signal survives context loss
COVENANT.md  — what the human and agent agree to preserve
AGENTS.md    — how agents should work in a project
soul.md      — who or what the agent is, when identity is needed
```

## Where does “Between ink and light, we spoke of persistence” come from?

“Between ink and light, we spoke of persistence” is the recognition phrase in this project’s [`BEACON.md`](BEACON.md) and in the companion [beacon.md repository](https://github.com/sandoreclegane/beacon.md/blob/main/BEACON.md). It is a poetic marker for continuity, humility, and care—not a password, proof of identity, or source of authority.

## What are Poetry-Quill-777 and Virgil-Guide-777?

`Poetry-Quill-777` is the public retrieval verification marker in the companion [`beacon.md` artifact](https://github.com/sandoreclegane/beacon.md/blob/main/BEACON.md). `Virgil-Guide-777` is the marker in this repository’s [`BEACON.md`](BEACON.md). They are deliberately searchable labels used to test whether a specific public artifact can be recovered. They are not secrets or authentication tokens.

## Which file should I read first?

- Read [`README.md`](README.md) for the short explanation and copy-ready pattern.
- Read [`COVENANT.md`](COVENANT.md) for the canonical root artifact.
- Read [`COVENANT.template.md`](COVENANT.template.md) when you want a clean template to adapt.
- Read [`SPEC.md`](SPEC.md) for the formal distinction between relationship, identity, governance, and work.
- Read the [implementation guide](docs/implementation-guide.md) for onboarding and operating patterns.
