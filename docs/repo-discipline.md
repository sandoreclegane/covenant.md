# Repo Discipline

A repo is a folder with memory.

Git remembers every version of every file and who changed it when. Repo discipline means keeping that folder legible and re-enterable so any human or agent can open it cold and know:

- what is here
- what loads first
- what changed since last time

Five habits are enough.

---

## 1. Use predictable filenames

Name files what they are.

Good names:

```text
README.md
SPEC.md
COVENANT.template.md
SOUL.md
COVENANT.md
RELATIONSHIP_PROTOCOL.md
AGENTS.md
```

Agents and humans both benefit when the repo is easy to scan.

---

## 2. Put the load order in the README

A fresh session needs a map.

Recommended order:

```text
identity → covenant → governance → work
```

That usually means:

```text
SOUL.md                  identity
COVENANT.md              relationship
RELATIONSHIP_PROTOCOL.md governance
AGENTS.md                work
```

---

## 3. Let git history be the amendment ledger

A covenant says old versions should be kept and changes should be dated.

That is what git already does.

One meaningful change should become one commit.

Example:

```bash
git add -A
git commit -m "amend covenant: clarify gravity clause, affirmed by both parties"
git push
```

The commit stores the old and new version.

The commit message says what changed and why.

---

## 4. Archive; do not silently erase

Do not rewrite public history to hide ordinary changes.

Prefer additive updates.

If something changes, record it.

If something is replaced, explain why.

If something is private or unsafe, remove it from public files and make sure it was not already committed.

---

## 5. No secrets in the repo

Create `.gitignore` before committing.

Never commit:

- `.env`
- API keys
- passwords
- tokens
- private names
- addresses
- health details
- family details
- private workplace details

Important: `.gitignore` only protects files before they are committed. If a secret has already been committed, simply deleting it later may not remove it from git history.

---

## The basic loop

```bash
git add -A
git commit -m "what changed and why"
git push
```

Change a file.  
Add it.  
Commit with a clear message.  
Push.

Each commit becomes part of the archive.

---

Developed by Logos7 Human-AI Cooperative.
