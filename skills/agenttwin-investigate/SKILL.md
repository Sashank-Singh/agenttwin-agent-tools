---
name: agenttwin-investigate
description: Investigate an AgentTwin failed run, derive an application repair from recorded events and assertions, and verify the repair without changing the captured correctness checks.
---

# Investigate an AgentTwin result

Read https://agenttwin.si/docs/cli.md and https://agenttwin.si/docs/quickstart.md for current receipt, verify, reset and replay syntax; inspect installed command help. Use the user's receipt and workflow, not a substituted demo.

Inspect application output, ordered events, initial/final state, assertion expected/actual values, fault activation and source/spec digests. Distinguish an application bug from an unsupported operation, invalid specification, untriggered fault or infrastructure error. Do not infer production provider behavior from a bounded adapter.

Recompute checks with verify using the recorded world and effective fault selection. Replay the captured application when supported; report divergence or missing artifacts explicitly. For reusable worlds, capture state before reset and compare every collection to the immutable starting fixture after reset.

Write a repair prompt naming the affected application path, observed error, causal evidence, required behavior and exact reproduction command. Patch only the application when demonstrating an unchanged-check fix. Never relax assertions or fixtures to obtain green status. Rerun with the same seed and fault, then verify evidence and compare specification digests.

A passing receipt is bounded evidence, not independent attestation or a claim of production equivalence. Include limitations and exact output in the report, removing secrets and private records before sharing.
