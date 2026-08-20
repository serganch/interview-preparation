# Assessment Snapshot

This file is a compact handoff for continuing preparation in a fresh context. It records current evidence and hypotheses, not permanent labels.

## Current state

The baseline assessment has started. One system-design exercise is complete and reviewed. The canonical exercise record is `exercises/01-money-transfer-system-design/`; the original candidate response is in its `solution.md`.

## Candidate baseline

Experienced backend engineer with strong practical JVM/backend experience, distributed systems and microservices exposure, and experience with production constraints and legacy systems. The preparation targets senior/staff backend interviews and controlled AI-assisted engineering.

## Main working hypothesis

The main bottleneck is not lack of broad architecture exposure. It is selecting the highest-impact concern quickly and expressing a sufficiently rigorous design under time pressure. The most important technical manifestation is incomplete correctness reasoning for external financial operations, especially unknown outcomes, retries, idempotency, and reconciliation.

## Strengths currently supported by evidence

- Requirements clarification.
- Practical architectural decomposition.
- Preference for proportionate complexity.
- Awareness of asynchronous providers, webhooks, reconciliation, and operational constraints.

## Priority development areas

- Identify the central invariant and architecture-driving risks early.
- Distinguish definitive failure from unknown outcome.
- Model client and provider idempotency across the full operation lifecycle.
- Define state transitions and handling of duplicate, stale, and concurrent events.
- Explain backpressure and admission control when a dependency is rate-limited.
- Keep the response within interview time and explicitly defer secondary details.

## Not yet assessed

- Live verbal system design under interviewer follow-ups.
- Code review and debugging.
- AI-assisted development workflow.
- Behavioural, influence, and staff-level organizational scope.
- Algorithms/coding, if relevant to target interview processes.

## Mentor operating instructions for the next session

- Do not begin a broad curriculum.
- Start with the focused lifecycle drill described in `progress/session-01-review.md`.
- Act as a mentor unless the exercise explicitly says to act as an interviewer.
- Ask the candidate to reason first; do not provide the model answer prematurely.
- Keep the exercise narrow and timeboxed.
- Record a short exercise artifact and review after completion.
- Update this snapshot only when new evidence changes a working hypothesis or next step.
