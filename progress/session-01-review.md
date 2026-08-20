# Session 01 Review

This review is retained as a progress-level reference. The canonical exercise record is `exercises/01-money-transfer-system-design/`.

## Metadata

- Exercise: system-design interview for a money-transfer backend
- Language: Russian
- Intended format: 60-minute interview
- Actual effort: approximately 8 hours, written asynchronously
- Status: reviewed
- Candidate response: `exercises/01-money-transfer-system-design/solution.md`

## Observed strengths

- Asked relevant requirements questions before designing.
- Identified the effect of provider limits and peak load.
- Chose a relatively simple architecture instead of unnecessary microservices.
- Distinguished the internal operation from the provider operation.
- Recognized asynchronous processing, idempotency, webhooks, and reconciliation.
- Considered operational load, storage, and hot users.

## Main weaknesses observed

- Spent disproportionate effort on low-impact storage and traffic estimates.
- Did not state the central correctness invariant early enough.
- Did not fully model unknown outcome after a provider timeout.
- Idempotency key retention and client/provider idempotency semantics were unsafe or underspecified.
- Status transitions, stale events, webhook duplicates, and concurrent updates were underspecified.
- Backpressure and admission control under provider rate limits were not sufficiently defined.
- Some API authorization and read-consistency behaviour was left implicit.
- The answer was much broader than a one-hour interview permits and was repeatedly redesigned during writing.

## Primary development hypothesis

The candidate has a reasonable practical architecture baseline but needs to improve prioritization and timeboxed reasoning. The highest-value technical focus is correctness of an external financial operation under retries, timeouts, duplicate/out-of-order events, and reconciliation.

This is a working hypothesis based on one exercise and must be retested in different formats.

## Current assessment

| Dimension | Current state | Confidence | Evidence |
|---|---|---|---|
| Requirements clarification | Strong | Medium | Relevant and architecture-changing questions |
| Architecture decomposition | Competent | Medium | Simple, plausible baseline design |
| Prioritization under time | Priority gap | High | Eight hours spent on a one-hour task; focus drifted to low-impact detail |
| Distributed correctness | Developing | Medium | Idempotency and reconciliation recognized, but unknown outcome was not fully modelled |
| Failure-mode analysis | Developing | Medium | Some failures identified, but state transitions and recovery semantics remained incomplete |
| Trade-off communication | Competent but verbose | Medium | Practical choices were present, but critical versus secondary decisions were not separated clearly |
| Technical knowledge | Partially assessed | Low | One design cannot isolate knowledge from application and communication |
| Interview execution under pressure | Not assessed | None | Exercise was asynchronous and not timeboxed in practice |
| AI-assisted development | Not assessed | None | No practical AI workflow exercise yet |
| Staff-level ownership/influence | Not assessed | None | No behavioural or organizational-scope exercise yet |

## Next training sequence

1. Focused lifecycle drill: one transfer through client retry, provider timeout, retry, duplicate webhook, out-of-order webhook, and reconciliation. Timebox: 20-30 minutes.
2. Short system-design exercise in a different domain. Timebox: 30-40 minutes. Require assumptions, minimal design, one deep dive, failure modes, and a short summary.
3. Repeat a full system-design interview in a strict 60-minute format.
4. Reassess the profile before choosing broader technical topics.

Do not rewrite the original answer as a correction exercise before the focused drills. Preserve it as baseline evidence.
