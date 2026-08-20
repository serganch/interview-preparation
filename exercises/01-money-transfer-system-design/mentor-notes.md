# Mentor Notes

## Metadata

- Exercise: 01 - Money Transfer System Design
- Format: written baseline system-design exercise
- Language: Russian
- Intended timebox: 60 minutes
- Actual effort: approximately 8 hours
- Status: reviewed
- Candidate response: `solution.md`

## Assessment summary

The candidate demonstrated a reasonable practical architecture baseline and strong requirements clarification. The main issue was not lack of architectural ideas, but prioritization and timeboxed reasoning. The response spent too much effort on low-impact sizing details while leaving the central correctness model for an external financial operation insufficiently explicit.

## Strengths observed

- Relevant requirements questions.
- Awareness of provider limits and peak load.
- Proportionate architecture with no unnecessary microservice decomposition.
- Separation of internal operation identity from provider operation identity.
- Recognition of asynchronous processing, idempotency, webhooks, and reconciliation.
- Awareness of operational load, storage, and hot users.

## Weaknesses observed

- Central correctness invariant was not stated early.
- Unknown provider outcome after timeout was not fully modelled.
- Client and provider idempotency semantics, including key retention, were unsafe or underspecified.
- Status transitions, stale events, duplicate webhooks, and concurrent updates were underspecified.
- Backpressure and admission control under the provider rate limit were not sufficiently defined.
- Some authorization and read-consistency behaviour was implicit.
- The answer was too broad for a one-hour interview and was repeatedly redesigned during writing.

## Current working hypothesis

The candidate needs focused practice in:

1. identifying the central invariant and architecture-driving risks;
2. distinguishing definitive failure from unknown outcome;
3. modelling idempotency across client, internal, and provider boundaries;
4. defining state transitions and handling duplicate, stale, and concurrent events;
5. keeping system-design reasoning within an interview timebox.

This hypothesis is based on one exercise and must be retested.

## Next exercise

Run a 20-30 minute focused lifecycle drill for one transfer. Cover client retry, provider timeout with unknown outcome, provider idempotency, duplicate and out-of-order webhooks, and reconciliation. Do not redesign the entire system.

## Assessment dimensions

| Dimension | State | Confidence | Evidence |
|---|---|---|---|
| Requirements clarification | Strong | Medium | Relevant architecture-changing questions |
| Architecture decomposition | Competent | Medium | Simple, plausible baseline design |
| Prioritization under time | Priority gap | High | Eight hours spent on a one-hour task |
| Distributed correctness | Developing | Medium | Idempotency and reconciliation recognized, unknown outcome incomplete |
| Failure-mode analysis | Developing | Medium | Important failures identified, recovery semantics incomplete |
| Trade-off communication | Competent but verbose | Medium | Practical choices present, priorities insufficiently separated |
| Technical knowledge | Partially assessed | Low | One design cannot isolate knowledge from application and communication |
| Live interview execution | Not assessed | None | Exercise was asynchronous |
| AI-assisted development | Not assessed | None | No practical AI exercise yet |
| Staff-level ownership/influence | Not assessed | None | No behavioural exercise yet |
