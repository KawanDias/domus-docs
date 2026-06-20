# <Subject> failure mode analysis

**Last updated:** <YYYY-MM-DD>

<!-- Optional changelog block when revising an existing FMA:
> **Changes:**
> - <what changed in this revision>
-->

## Scope

<!-- What this FMA covers and what it explicitly does not. State the threat model
     and assumptions (e.g. "assume an attacker can grab privileged keys or induce a
     reorg"). Reference any parent FMA this builds on. Note where the boundary of
     analysis stops (e.g. "this doc stops at delivery; post-delivery accounting is
     out of scope and lives in its own FMA"). -->

<!-- Optional aside for dismissed classes of failure:
<aside>
⚠️
<which failure class is dismissed and the one-line reason or response>
</aside>
-->

## Summary

<!-- One row per finding, ordered by severity. Columns vary by FMA style — pick one:
     post-incident view → Impact + Response; messaging-layer view → Impact + Mitigation. -->

| **ID** | **Finding** | **Severity** | **Impact** | **Mitigation / Response** |
| --- | --- | --- | --- | --- |
| FM1.a | <short finding> | Critical / High / Medium / Low / Liveness / Informational | <one-line impact> | <one-line mitigation or response> |

## FM1: <failure category>

<!-- Group findings into numbered categories. One-line description of the category. -->

### FM1.a: <specific failure mode>

<!-- A failure mode finding keeps its labeled lead-ins so a reader can scan to the part they
     need. This is the engineering-document exception in WRITING-GUIDE.md, not a violation. -->

- **Description:** <what goes wrong and the precise mechanism or privileged role abused>
- **Impact:** <severity and concrete consequence>
- **Mitigation:** <prevention, detection or monitoring signals, and response>

<!-- Alternative per-entry shape used by post-incident FMAs (no Description field):

### FM-I-1.a. <specific failure mode> (<direction, e.g. root to leaf>)

**Impact:** <consequence, with bounds>

**Recovery path:** <what the protocol can do after detection>
-->

## Possible next steps

<!-- Follow-up design or operational actions surfaced by the analysis. -->

- <action>
