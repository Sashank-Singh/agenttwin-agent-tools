---
name: agenttwin-replay
description: Replay an AgentTwin captured run, verify a source-only repair against unchanged checks, and record the restored baseline as a reviewed regression.
---

# Replay an AgentTwin run and verify the repair

Use https://agenttwin.si/docs/worlds.md for reusable world, scenario and verify commands, https://agenttwin.si/docs/evidence.md for receipt structure, and the current CLI help for exact flags.

Find the failed run's stored receipt inside the project .agenttwin/runs directory. Inspect the recorded operation events and assertion failures before touching source. Identify what application change the evidence supports; do not change the captured checks or the scenario data.

Verify the patch with the receipt's effective world and the same scenario version from the docs, for example `agenttwin verify --file .agenttwin/runs/RUN_ID/run.json --world agenttwin.world.json --scenario support_retry@1 --json`. Replay the captured failure without the patch first when you need original evidence; an untriggered fault or unverified patch is not proof.

Record exact commands, exit codes, receipt paths, and the unchanged check list. Commit the passing baseline only to a trusted review location before requiring it in CI. Never upload credentials, private customer data or unrelated source files.
