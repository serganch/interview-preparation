# Current Progress

## Status

Baseline assessment started. Session 01 system-design exercise is complete and reviewed.

## Current Decisions

- Use OpenCode as the primary AI-assisted development environment.
- Use Luna as the initial model.
- Do not perform extensive model benchmarking at this stage.
- Create a GitHub repository for the project.
- Establish a clear set of context and instruction files before starting substantial implementation.
- Use the project itself as a practical environment for developing AI-assisted engineering skills.
- Preserve original exercise responses as evidence and keep mentor reviews separate.
- Maintain a compact assessment snapshot so preparation can resume from a clean context.

## Assessment Result

Session 01 showed a reasonable practical architecture baseline and strong requirements clarification. The main current development hypothesis is a prioritization and timeboxed-reasoning gap, with a related technical gap in modelling correctness for external financial operations under timeout, retry, duplicate/out-of-order events, and reconciliation.

Detailed review: `progress/session-01-review.md`.

Current handoff snapshot: `progress/assessment-snapshot.md`.

## Immediate Next Step

Run a focused 20-30 minute lifecycle drill for one transfer operation. Cover client retry, provider timeout with unknown outcome, provider idempotency, duplicate and out-of-order webhooks, and reconciliation. Do not redesign the entire system.

Then run a short 30-40 minute system-design exercise in another domain and finally repeat a strict 60-minute interview to measure progress.

## Important Constraint

Do not prematurely optimize the process.

The initial goal is to get a working feedback loop:

candidate → agent → implementation/exercise → review → feedback → next task.

For each exercise, preserve a concise record containing the prompt, language, format, timebox, actual effort, candidate response, review, observed evidence, current hypothesis, and next step. Keep original responses unchanged and store mentor analysis separately.

The workflow can be refined after real usage reveals its weaknesses.
