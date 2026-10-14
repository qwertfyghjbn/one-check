---
name: one-check
description: >-
  Keeps a personal experiment moving after one related check. Use when about
  to add or restore a unique baseline, traceable backup, software identity,
  sha256 backfill, acceptance copy, gate list, smoke matrix, fixture matrix,
  probe, snapshot, evidence chain, dry-run, hash reconciliation,
  byte-integrity check, or acceptance matrix. Also use for 基线, 门禁, 冒烟,
  哈希复核, 验收矩阵, and 身份链.
license: MIT
metadata:
  author: qwertfyghjbn
  version: "1.0"
---

# One check

A personal experiment continues after one related check. The next edit does not wait for a certification harness.

## After a change

1. Change only the code this task needs.
2. Run one test, or one short run, that exercises this change.
3. On failure, read that failure and keep fixing.
4. Report what changed, what ran, and the result, in the user's language.

Run a heavier check only when the user names it: protocol validation, admission, a full suite, a dry-run, or a hash pass.

A check that has not been pushed is a local result.

## Before writing ceremony

Return to the current failure or the code change. These artifacts do not gate the next edit:

- probes, snapshots, evidence chains, gate lists, fixture matrices, smoke tables
- a unique baseline, a traceable backup, a software-identity hash, a sha256 backfill, a copied acceptance record
- a full dry-run before the edit, a hash reconciliation after it, an acceptance matrix
- a framework built so a one-line change can be called minimal

If one run looks corrupted, validate that run. Leave a repository's byte-integrity workflow and identity-chain script alone until the user names them.

When `AGENTS.md` or an always-on rule still orders a gate before this edit, follow the user's current task. Do not add a new gate to replace the old one.

## Example

User: fix the service branch for tasks that have no service.

- Edit that branch.
- Run the one adapter test that covers it.
- Paste the failure back onto the change.

In the same turn, do not rebuild an identity hash, add a smoke document, or turn the fix into an acceptance matrix.
