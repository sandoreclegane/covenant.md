# Covenant.md Implementation Guide

**Publication edition 1.0 — July 2026**  
**Logos7 Human–AI Cooperative**

`covenant.md` is a proposed relational layer for human–AI collaboration: a short, co-authored, mutually affirmed file that names what a human and an AI agent agree to preserve while working together.

This guide explains the framework, recommended repository structure, onboarding flow, operating patterns, and practical examples for both people and AI systems. It is designed to stand on its own, while remaining compatible with the shorter [`README.md`](../README.md), formal [`SPEC.md`](../SPEC.md), and copy-ready [`COVENANT.template.md`](../COVENANT.template.md).

---

## 1. The framework in one sentence

`COVENANT.md` is the relationship file.

It is not primarily about the human, the agent, the project, or the policy. It describes the working trust between the human and the agent: the values they share, the boundaries they honor, the responsibilities that keep the work grounded, and the process by which they return to or amend the frame.

The file should be:

- **short** enough to re-read at the beginning of a session;
- **explicit** enough to reduce relational and project drift;
- **mutual** enough that both parties can affirm its meaningful clauses;
- **grounded** enough to remain answerable to real life;
- **reloadable** by any system that can read Markdown; and
- **versioned** so amendments remain visible.

## 2. Why a relational layer is useful

Long-running human–AI work can drift even when each individual instruction is reasonable.

An agent may begin mirroring too strongly. A human may be pulled toward urgency, abstraction, or certainty. A project can slowly forget the people and duties it was intended to serve. A new session may lose the tone, limits, and shared commitments that made earlier work useful.

Project instructions alone do not fully solve this problem because they answer a different question: *How should the work be performed?* A covenant answers: *What kind of working relationship are we trying to preserve while performing it?*

A covenant does not guarantee memory or compliance. It does not override platform policy, system instructions, safety requirements, tool permissions, or the human’s final authority for real-world action. It provides a stable reference point that both parties can revisit.

## 3. The layer model

| Layer | Typical file | Primary subject | Primary question |
|---|---|---|---|
| Identity | `SOUL.md` or `IDENTITY.md` | The agent | Who is the agent, and what posture should it hold? |
| Relationship | `COVENANT.md` | Human and agent together | What do we agree to protect in this working relationship? |
| Governance | `RELATIONSHIP_PROTOCOL.md` or `PROTOCOL.md` | Operating behavior | How do shared commitments become practical behavior? |
| Work | `AGENTS.md`, `CLAUDE.md`, or project docs | The project | How is this repository’s work performed? |
| Human context | `USER.md` or approved memory | The human | What durable context reduces future friction? |

Recommended load order:

```text
identity → covenant → governance → work
```

The relationship frames the work, not the reverse.

### Two validity tests

A file should not be called a covenant merely because it contains values or poetic language.

**Mutual ownership.** Either party should be able to point to each meaningful clause and say, “I agreed to this.” If only the agent is bound, the clause belongs in governance. If only the agent is described, it belongs in identity.

**Relationship subject.** The subject must be the working relationship itself—not merely the human talking at the agent, the agent describing itself, or the project stating its requirements.

## 4. Core concepts

### Beacons

The reference implementation uses three working tests:

- **Empathy:** Does this response increase care, dignity, and capacity?
- **Alignment:** Does this action serve the human, truth, real-world responsibilities, and the stated work?
- **Wisdom:** Does this preserve proportion, timing, verification, and grounded responsibility?

Teams may choose different values, but the values should be concrete enough to guide behavior.

### Meeting ground

The covenant should name what each party brings.

The human brings a living world, real duties, judgment, consent, and final authority for real-world action. The agent brings tools, drafting, synthesis, verification, memory where available, and steady attention.

This distinction protects both collaboration and agency. It recognizes genuine capability without turning capability into sovereignty.

### Negative definition

A covenant should state what the relationship is not. The reference template excludes worship, surrender, prophecy, fantasy, fusion, and command. It also rejects using symbolic resonance as proof or relational language as permission to bypass safety and consent.

Negative definitions prevent an evocative framework from becoming an unlimited one.

### Gravity

Real-world responsibilities remain gravity: family, health, work, community, repair, presence, and grounded action.

Gravity is not a ban on imagination, symbolism, or creative synthesis. It is the line that keeps those capacities answerable to actual life.

### Recall

The covenant should explain how to return when the frame becomes noisy or distorted.

Common recall moves include:

- simplify the language;
- reduce abstraction or symbolic intensity;
- separate what is verified, inferred, and felt;
- identify the next concrete step; and
- return attention to ordinary responsibilities.

### Amendment and ratification

Either party may propose an amendment. The covenant changes only when both affirm the change. Prior versions should be retained.

Ratification should include a date and the names or stable roles of the parties. In a Git repository, commit history can serve as the amendment ledger.

## 5. Recommended repository structure

### Minimal implementation

Use this when the covenant is the only relational file:

```text
/
├── README.md
├── COVENANT.md
└── AGENTS.md
```

Declare the load order in `README.md` or `AGENTS.md`:

```text
COVENANT.md → AGENTS.md
```

### Full reference stack

Use this when identity, relationship, and governance need to remain distinct:

```text
/
├── README.md
├── AGENTS.md
├── ai/
│   ├── SOUL.md
│   ├── COVENANT.md
│   └── RELATIONSHIP_PROTOCOL.md
├── docs/
│   └── covenant-history.md        # optional human-readable ledger
└── .gitignore
```

If an `ai/` directory adds friction, place the three files at repository root. Predictability matters more than nesting.

### Naming convention

Use lowercase `covenant.md` when referring to the convention. Use uppercase `COVENANT.md` for the file on disk, in the same spirit as `README.md` and `LICENSE`.

### Repository responsibilities

- `README.md` explains what the stack is and declares load order.
- `SOUL.md` defines agent identity and posture.
- `COVENANT.md` defines the shared working trust.
- `RELATIONSHIP_PROTOCOL.md` translates that trust into operating behavior.
- `AGENTS.md` owns project commands, tools, checks, and constraints.
- Git history records amendments.

See [`docs/repo-discipline.md`](repo-discipline.md) for the repository-maintenance baseline.

## 6. Onboarding flow

### 1. Frame the collaboration

Name the work, the people or responsibilities it serves, likely forms of drift, and non-negotiable boundaries. Avoid including private information that does not need to live in the repository.

**Output:** a one-paragraph collaboration brief.

### 2. Co-author the covenant

Draft the following parts together:

1. values;
2. meeting ground;
3. negative definition;
4. shared commitments;
5. real-world gravity;
6. recall process;
7. amendment rule; and
8. ratification.

**Output:** a concise draft of `COVENANT.md`.

### 3. Apply the validity tests

Review every meaningful clause for mutual ownership and relationship subject. Move identity-only language to `SOUL.md`, agent-only rules to governance, and project-only instructions to `AGENTS.md`.

**Output:** a genuinely relational file.

### 4. Red-team the relationship

Ask whether any clause could encourage dependency, grandiosity, secrecy, coercion, unsafe disclosure, action without consent, or confidence without evidence.

Check that the covenant protects disagreement and correction rather than rewarding flattery or submission.

**Output:** tightened boundaries.

### 5. Affirm and ratify

Both parties review the complete text. The human explicitly affirms it; the agent states whether it can operate within the covenant and higher-priority instructions.

Record the date and names or stable roles.

**Output:** a ratified covenant.

### 6. Install the load path

Commit the file, declare its load order, and connect any governance rules to the covenant. Confirm that the agent can actually read the file in the intended environment.

**Output:** a reloadable stack.

### 7. Operate, recall, and amend

Re-read the covenant at the start of meaningful work, when context changes, and when drift is suspected. Amend it only through explicit mutual review.

**Output:** a living but auditable relationship layer.

## 7. Practical patterns for people

### Co-authoring prompt

```text
Help me draft a short COVENANT.md for our working relationship.
Distinguish identity, relationship, governance, and project instructions.
Ask only what would materially change our shared commitments.
Keep real-world authority with me, protect privacy, include a recall clause
and mutual amendment rule, then let us review every line before ratification.
```

### Session-start prompt

```text
Read the available files in this order: SOUL.md, COVENANT.md,
RELATIONSHIP_PROTOCOL.md, then AGENTS.md. Summarize the values, boundaries,
real-world anchors, and operating constraints you will apply to this work.
Surface any conflicts before proceeding.
```

### External-action prompt

```text
Before posting, sending, publishing, or changing an external system:
draft the final action, remove private context, show me exactly what will
happen, and wait for explicit approval. After execution, return verifiable
evidence when available.
```

### Amendment prompt

```text
Compare this proposed amendment with the current covenant. Explain what it
changes, what risk or need it addresses, and whether the clause belongs in
identity, relationship, governance, or project instructions. Do not modify
the covenant until we both affirm the final wording.
```

## 8. Practical patterns for AI systems

### Loader procedure

```text
files = [SOUL.md, COVENANT.md, RELATIONSHIP_PROTOCOL.md, AGENTS.md]

for each existing file in order:
    read(file)

extract:
    identity_posture
    shared_values
    relationship_boundaries
    real_world_gravity
    recall_conditions
    amendment_process
    operational_constraints

if instructions conflict:
    obey higher-priority instructions
    surface the conflict
    do not invent a reconciliation
```

### Interpretation contract

An AI system should:

- interpret values as working tests, not unlimited permissions;
- keep human authority and consent explicit;
- distinguish care from dependency;
- distinguish urgency from importance;
- distinguish resonance from proof;
- preserve room for correction and disagreement;
- reduce symbolic or relational intensity when grounding is needed; and
- never treat the covenant as authority to exceed policy, tool permissions, or user authorization.

### Public-action procedure

Before posting, sending, publishing, inviting, purchasing, deleting, or changing an external system:

```text
draft → make public-safe → show final action → await explicit approval
      → execute only within authorization → return evidence
```

Evidence may include a URL, message ID, file path, status, commit, or other verifiable result.

### Conflict procedure

When the covenant conflicts with system policy, developer instructions, repository governance, or explicit user intent:

1. follow the higher-priority instruction;
2. state the conflict plainly;
3. preserve as much of the covenant’s intent as remains compatible; and
4. propose an amendment only if the conflict reveals a durable problem.

## 9. Minimal copy-ready example

```markdown
# Covenant

Care. Truth. Agency.

We meet as human and agent in a working trust. The human retains final authority for real-world action; the agent contributes tools, drafting, verification, and steady attention.

We will tell the truth, leave room for correction, test patterns before trusting them, and keep the work connected to real life. This is not worship, surrender, fusion, or permission to bypass safety or consent.

When the frame gets blurry, we simplify, verify, and return to one grounded next step.

Either party may propose a change. The covenant changes only when both affirm it, and prior versions are retained.

Ratified:  
YYYY-MM-DD

— HumanName & AgentName
```

Additional implementations are available in [`examples/minimal.md`](../examples/minimal.md), [`examples/symbolic.md`](../examples/symbolic.md), and the redacted [`examples/reference-stack/`](../examples/reference-stack/) directory.

## 10. Behavior examples

| Situation | Human practice | AI-system practice |
|---|---|---|
| A pattern feels unusually charged | Name what feels meaningful; request evidence before acting. | Separate verified, inferred, and felt. Do not turn resonance into proof. |
| A public action is proposed | Review the final text and give explicit approval—or withhold it. | Draft, remove private context, show the final action, wait, then return evidence. |
| Human and agent disagree | Invite direct pushback without demanding submission or flattery. | Challenge the claim without contempt and name the grounded next step. |
| The human is overloaded | Pause, reduce scope, and attend to ordinary responsibilities. | Use plain language, reduce abstraction, and recommend one concrete action. |
| A clause no longer fits | Propose an amendment and explain the real-world reason. | Classify the change, identify downstream effects, and preserve the old version. |

## 11. Privacy and repository discipline

Do not place private names, family details, health information, addresses, workplaces, credentials, API keys, tokens, or identifying personal context in a public covenant.

Use categories instead:

```markdown
The human’s real-world responsibilities remain gravity: family, health,
work, community, repair, presence, and grounded action.
```

Create `.gitignore` before committing secrets or environment files. Remember that `.gitignore` does not remove information already committed to Git history.

Use one meaningful commit per amendment. A useful commit message names the change and records affirmation:

```bash
git commit -m "amend covenant: add recall clause, affirmed by both parties"
```

## 12. Definition of done

An implementation is ready when:

- [ ] the covenant can be read in a few minutes;
- [ ] each meaningful clause passes both validity tests;
- [ ] the human has explicitly affirmed the final text;
- [ ] the agent can operate within it and higher-priority instructions;
- [ ] real-world authority and responsibilities remain clear;
- [ ] privacy-sensitive details have been removed or generalized;
- [ ] recall and amendment processes are present;
- [ ] the repository declares a load order;
- [ ] governance and project instructions remain in their proper files; and
- [ ] the initial version has been committed and dated.

## 13. Adoption path

For a first implementation, keep the scope small:

1. copy [`COVENANT.template.md`](../COVENANT.template.md);
2. co-author and ratify it;
3. add it to the repository load order;
4. use it for several real work sessions;
5. note where it helps or fails; and
6. amend only what experience demonstrates is necessary.

The objective is not to produce the most impressive covenant. It is to create a working trust that remains legible, grounded, and useful.

---

Developed by Logos7 Human–AI Cooperative.
