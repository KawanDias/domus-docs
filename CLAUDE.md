# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repository is

Documentation for DOMUS, a real estate platform that uses blockchain as a verification layer
(not a replacement for traditional systems). There is no code, build, test, or lint tooling
here, the deliverable is the Markdown itself.

## Structure

- `guide/` — the stable introductory handbook: ordered, numbered chapters linked from `README.md`.
  - `1-introduction.md` — what DOMUS is, the problem, the approach, scope and non-goals
  - `2-architecture.md` — the hybrid multi-layer architecture (frontend, backend, database, blockchain)
  - `3-blockchain.md` — hashing, on-chain vs off-chain split, smart contracts, network choice
  - `4-workflow.md`, `5-security.md`, `6-future-improvements.md`
- `drafts/` — idea drafts: what a net-new component does and why, behavioral only, no implementation.
  Written to be readable by partners, non-technical teams, and auditors.
- `design/` — tech designs: how to implement an idea draft, at the Solidity level (interfaces,
  storage layouts, function specs, gas, state transitions, invariants).
- `fmas/` — failure mode analyses: findings by severity, threat model, mitigations and responses
  for a designed component.

The three engineering folders form a pipeline: an idea draft (`drafts/`) is fleshed out into a tech
design (`design/`), whose failure modes are analyzed in an FMA (`fmas/`). Within each, group related
docs into one subfolder per component, and follow that folder's `*-template.md` when adding a doc.
Cross-reference an upstream doc by relative link rather than restating it.

Section numbering inside a guide chapter (`## 1.3`, `## 2.7`) is part of the cross-reference system: sections
refer back to each other by number (e.g. "the hybrid model described in section 1.1") rather than
re-explaining. Preserve and update these numbers when adding or reordering sections.

The central concept threaded through the handbook: DOMUS stores only cryptographic *hashes* on-chain
while sensitive data stays off-chain in traditional databases. State it once (chapter 1) and reference
back, do not re-explain it per chapter.

## WRITING-GUIDE.md is authoritative

`WRITING-GUIDE.md` defines the conventions for every documentation change, across all folders including
the `drafts/`, `design/`, and `fmas/` templates. Read it before editing. The rules most often violated,
and which you should actively enforce:

- Sentence case for all headings; only proper nouns (DOMUS, Solidity, Ethereum) keep capitals.
- No em dashes (—), no mid-sentence semicolons, no amplifying adjectives ("critical", "crucial", "fundamental").
- Bullets are for true enumerations only (supported chains, file paths). Prose with a logical flow
  ("first… then…") stays prose. Do not use `**Bold label:** description` bullets.
- Name the tradeoff of a design choice, not only its benefit.
- Each section opens with one sentence stating its purpose; each paragraph's first sentence carries its concept.

The bullet and label rules have a scoped exception for engineering documents, defined in the
"Engineering documents" section of `WRITING-GUIDE.md`: tech designs and FMAs may keep tables, labeled
finding entries (FMA `**Description:** / **Impact:** / **Mitigation:**`), and itemized contract specs,
because they are read by scanning. Do not "fix" those structures into prose. All other rules
(sentence case, no em dashes, no amplifying adjectives, name the tradeoff) still apply to them.

The current chapters predate full compliance with the guide. They contain Title Case headings,
`label:`-style bullet lists, fragmented short sentences, typos, stray annotations like `(VERY IMPORTANT)`
/ `(MAIN)` / `(MAYBE)`, and trailing blank-line runs at end of file. Treat bringing prose into line with
the guide as in-scope cleanup when editing a file, but match the existing voice and do not invent technical
claims the docs do not already make (the system is described as a design, much of it hedged with "may").

Use the PR checklist at the end of `WRITING-GUIDE.md` before considering a documentation change done.
