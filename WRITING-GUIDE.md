# Writing guide

This guide proposes writing conventions for the DOMUS documentation. The goal is to keep the docs consistent, readable, useful as the project grows.

The guide has two parts. **Principles** describe the habits that shape how a document is structured and how each section reads. **Rules** describe the concrete practices to apply during revision.

This guide does not cover tooling, or file naming.

---

## Principles

The six principles below set the orientation for any DOMUS document. Each one is a habit that pays off across the entire chapter, not just in a single section.

### Every document answers a question

State the question in the first paragraph, even if the title already hints at it. A document with an unclear question wanders. For example, a chapter on transaction verification should make clear in its opening lines that it explains how DOMUS detects tampering by comparing stored hashes against the current data.

### State the scope, in and out

What is covered must be stated. What is *not* covered must also be stated. Section 1.8 of the introduction does this well with its "What DOMUS does NOT do" list. That pattern is worth replicating in any chapter where the boundary matters.

### Open every section with its purpose

The reader must know what they will learn before the content begins, so one sentence at the top of each section is enough.

### The first sentence of every paragraph synthesizes what follows

The first sentence carries the concept. The rest of the paragraph develops it with detail, evidence, or examples. A reader who skims only the first sentence of every paragraph should still come away with a coherent (if compressed) version of the document.

### Calibrate context to your reader

The DOMUS docs are read by developers, stakeholders, evaluators in academic settings, each with different prior knowledge. Explain blockchain primitives the first time they appear in a chapter, but do not redefine them on every mention. When unsure, over-explain on first mention and reference back afterwards.

### Voice

Write the way you would explain the system to a colleague at a whiteboard. If a sentence sounds like a press release, rewrite it. Read it out loud, since a sentence that feels unnatural in conversation will read as unnatural on the page.

Before:

> DOMUS introduces a sophisticated cryptographic verification mechanism that leverages distributed ledger technology to ensure the immutable persistence of transactional state.

After:

> DOMUS stores a hash of each transaction on-chain, so any later change to the off-chain data can be detected.

---

## Rules

Apply these during revision. They are numbered for checklist reference.

### 1. Do not restate the same idea across sections

Pick the right section for an idea, state it once, let the rest of the document reference back. Restating the same concept with rewording dilutes the signal and inflates the document without adding information.

If the hybrid Web2 + Web3 model is the central concept, state it once in the chapter that introduces DOMUS. Later sections can refer to it ("the hybrid model described in section 1.1") instead of explaining it again.

### 2. Connect related ideas with prose, not as flat sentences

When several sentences in a paragraph share a thread (sequence, contrast, elaboration), link them with commas, conjunctions, or subordinate clauses. A paragraph of short sentences that all end in periods reads like a bullet list without bullets.

Before:

> The platform stores hashes. It does not store sensitive data. Hashes are verified later. Original data stays off-chain.

After:

> The platform stores only hashes, not the underlying data, which stays off-chain. Verification later compares the stored hash against the current data.

### 3. Reserve bullets for true enumerations

Use bullets for lists of comparable items, such as prerequisites, supported chains, or file paths. They are not a tool for breaking a paragraph apart to make it look organized. If the items have a logical flow ("first... then... afterwards..."), use prose.

### 4. Match section length to answer complexity

When the answer is simple, one or two sentences are enough. Padding a short section with restated context dilutes its signal. A long section is justified only when the topic complexity demands it.

### 5. Name the tradeoff, not just the benefit

State the cost of every design choice. If you cannot name a tradeoff, the analysis is incomplete and the reader cannot evaluate the choice.

Before:

> Storing only hashes on-chain is efficient and preserves privacy.

After:

> Storing only hashes on-chain keeps gas costs low and avoids exposing transaction details publicly. The tradeoff is that verification requires the off-chain data to still be available. If the off-chain data is lost, the on-chain proof becomes meaningless on its own.

### 6. Defer out-of-scope topics with a pointer

If a topic falls outside the current chapter, name it and point to where it lives. A partial explanation is worse than a clean reference because the reader cannot tell whether the explanation is complete.

Before:

> The hash function is one-way and produces a fixed-length output. It is collision-resistant. We use it because it is fast.

After:

> Transaction proofs use SHA-256. Its cryptographic properties are covered in chapter 3.

### 7. Use sentence case for section headings

Only the first word is capitalized. Proper nouns (DOMUS, Solidity) keep their natural capitalization.

Before:

> ## Real Estate Market Challenges

After:

> ## Real estate market challenges

### 8. Avoid amplifying adjectives

Words like "critical", "fundamental", "extremely", "crucial", "excellent" add weight without adding meaning. Either remove them or replace them with a specific claim.

Before:

> Blockchain is a critical technology that provides fundamental security.

After:

> Blockchain stores each transaction hash on a public ledger. Any later modification is detected by hashing the current off-chain data and checking it against the stored value.

### 9. Avoid em dashes (—)

Em dashes break the visual rhythm of prose and are easy to overuse. Restructure with commas, periods, or parentheses.

Before:

> The system handles failures — including network timeouts — automatically.

After:

> The system handles failures, including network timeouts, automatically.

### 10. Avoid "label: description" patterns in bullet lists

Bullets that follow a `**Bold label:** description` pattern flatten what should be flowing prose. Either rewrite the bullets as a paragraph or, if the list structure helps, drop the bold label and let the content speak.

Before:

> - **Immutable:** Transactions cannot be modified.
> - **Transparent:** Anyone can audit the ledger.

After:

> Transactions become immutable once recorded, while the public ledger remains auditable by anyone.

---

## Engineering documents

The rules above govern prose. The engineering documents under `drafts/`, `design/`, and `fmas/` follow templates that also use tables and labeled entries, because a tech design or failure mode analysis is read by scanning to the relevant part, not from top to bottom. Where a recognized format calls for that structure, prefer it over prose:

- Summary, state-transition, and invariant tables stay as tables.
- Failure mode findings keep their `**Description:** / **Impact:** / **Mitigation:**` lead-ins.
- Function and storage-slot specifications stay as itemized lists.

This is a scoped exception to rules 3 and 10 only. Everything else still applies to these documents: sentence case headings (rule 7), no em dashes (rule 9), no amplifying adjectives (rule 8), and naming the tradeoff of a decision rather than only its benefit (rule 5). The tradeoff of allowing the scannable structure is that a document can drift into all tables and no reasoning, so the prose around each table must still carry the argument.

---

## Checklist before submitting a PR

Before opening a documentation PR, read each affected file once more with the following in mind:

- [ ] The chapter states the question it answers.
- [ ] Each section opens with one sentence of purpose.
- [ ] No idea is restated across more than one section.
- [ ] Section headings use sentence case.
- [ ] Tradeoffs of design choices are named, not only benefits.
- [ ] Topics outside the current chapter's scope are pointed to, not partially explained.
- [ ] No em dashes (—), no mid-sentence semicolons, no amplifying adjectives.
- [ ] Bullet lists hold genuine enumerations, not fragmented prose.

---

## A note on style

These rules are restrictive by design. You may find some of them frustrating at first, but the friction is the point. When a sentence keeps fighting a rule, the problem is usually structural rather than stylistic, so rewriting at a higher level fixes both.
