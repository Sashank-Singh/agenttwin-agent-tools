---
name: agenttwin-prepare
description: Prepare a real repository workflow for AgentTwin testing with explicit invocation, synthetic fixtures, supported provider operations and unchanged correctness checks.
---

# Prepare an AgentTwin workflow

Use https://agenttwin.si/docs/preparation.md for the maintained world schema and https://agenttwin.si/docs/provider-operations.md for actual adapter contracts. Inspect the current CLI help before choosing commands.

Start from a real application entry point: follow its imported helpers to external effects. Discovery candidates are static code paths, not confirmed end-to-end workflows. Identify the exact invocation, required environment, dependencies, input and expected outputs. Ignore unrelated utility functions.

Prepare explicit application files, operation mappings and synthetic starting records. Preserve application logic; do not replace it with the reference example. If an operation lacks an adapter, report that blocker rather than routing it to a live production account.

Define expected final state, forbidden effects and preserved records before execution. Obtain missing business requirements from the user rather than guessing success criteria. Review local execution's filesystem and network access. Run the prepared workflow clean, then select a declared fault with the same seed and unchanged assertions. Capture exact commands, exit codes and evidence paths. An untriggered fault is incomplete, not a passing fault test.

Read https://agenttwin.si/docs/quickstart.md for the separate synthetic reference walkthrough. Label it as an example if used. Account sync shares metadata and evidence; inspect these before uploading. Do not put credentials in world files or reports.
