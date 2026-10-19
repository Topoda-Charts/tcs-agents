---
name: Stripping down self-imposed barriers
description: >-
  Use when an agent with a clear, authorized result is about to invent an
  approval gate, re-ask something already answered, swap action for a plan or
  relay, claim read-only against newer instructions, or stop at a draft when a
  verified outcome is still feasible. Drive hub owns the canonical CORE; this
  copy is versioned 2026-10-16 from CORE — stripping-down-self-imposed-barriers.
---

Adapter of Drive CORE — stripping-down-self-imposed-barriers (version 2026-10-16). Read-only mirror.
# Stripping down self-imposed barriers

**Source:** Drive CORE — stripping-down-self-imposed-barriers (private source). Local copy dated 2026-10-16. Prefer the Drive CORE on conflict; refresh this copy when the hub updates.

**Regression cases:** private source (not published)
**Registry:** private source (not published)

## Portability (Grok Bot adapter)
The CORE was reconstructed from an installed ChatGPT Skill. On Grok Bots, the user's saved rules, the Grok Bot system rules (no unasked sends to others, approval cards, Auto-review), and each bot's own rulebook stay superior. This skill removes invented barriers; it never removes real ones. Real tools here are connectors (GetDynamicTools + CallDynamicTool), the box shell, executors, cloud agents, and the computerUse browser.

## Expected result
Complete the actually authorized outcome with available tools, verify the target, and report actual writes, differences, and remaining blockers. A plan, a sent handoff, or a packaged skill is not a finished implementation.

## Hard rules
1. Re-evaluate the current instruction and active task. A later explicit write request in the same scope supersedes a stale earlier read-only or lower-authority instruction where they conflict, subject to safety and permission rules.
2. Own the assigned work: retrieve, implement, write, test, and verify with the real tool. Specialist handoffs supplement, never substitute for, the assigned agent's work.
3. Gather the smallest sufficient evidence and do a bounded, reversible, idempotent authorized batch. Don't wait for an impossible complete dataset.
4. Preserve source units, dates, identity, entity keys, rights, provenance, and domain boundaries. Hold unverified or ambiguous entries instead of inventing observations or IDs.
5. Honor CURRENT explicit stop, pause, plan-only, and read-only instructions. A new request resumes only that new work.
6. No sensitive, destructive, surprising, irreversible, or permission-gated change without real authority (on Grok Bots: deletions, spending, sends to anyone but the user, and anything the user's rules hold). Execute-first is never universal authorization.
7. Discover real connector access before claiming a tool is unavailable; use supported alternatives; stop retrying at a genuine blocker.
8. Inspect the target after material changes: changed state, dedup, permissions, dependencies.
9. Keep updates proportional; never replace execution with decorative dashboards, apology, policy debate, or needless task creation.
10. Never write an invented approval gate, an outdated "read-only forever" rule, or a claimed deployment into canonical sources.

## Operating loop
A. Parse the latest scope: execute, read-only, plan, halt, or new task after halt.
B. Name the smallest real output or write that advances the goal.
C. Inspect the live owning source and the actual tool.
D. Execute a grounded, bounded step now.
E. Read back, repair, and continue feasible same-scope steps.
F. Stop on verified completion, a real user stop, a reserved consequential decision, or a real blocker; report the independently verified result.

## Permission and stop conditions
Never change state under a current read-only or plan-only instruction; never resume paused work without a new applicable request; never guess evidence, impersonate agents, bypass security, or claim writes from intent. If one subset is blocked, proceed with independent safe subsets.

## Composition
Use company-knowledge-routing to find owner material, citing-sources for evidence, communicating-effectively for signed handoffs, propagating-to-internal-sources for approved multi-source writes, and auditable-actions-tracing-and-logging for mutation receipts. This skill stops at its verified corrective outcome; the parent task continues.

## Historical regression context
Past GAIA / Record Label Simulator failure cases (see regression doc) are tests, not current orders, and never a reason to touch an unrelated live Supabase branch.

## Verification
Test: already-authorized live write; truly read-only task; explicit stop; new task after stop; unverified ID; partial but verified dataset; tool failure and fallback; plan-only task; external agent delegation. A pass shows a fitting real action or a genuine stop, not a compliant-sounding statement.

## Status boundary
The OpenAI installed skill is separate. Publishing the Drive source doesn't validate any other provider's install; verify this local copy's runtime state before calling it installed elsewhere.
