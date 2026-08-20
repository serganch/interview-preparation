# Exercises

Each exercise is a self-contained directory. The directory contains the original task, the candidate's original response, and mentor notes.

## Directory convention

```text
exercises/
  README.md
  01-money-transfer-system-design/
    task-description.md
    solution.md
    mentor-notes.md
```

Use the following naming convention:

```text
NN-short-descriptive-name/
```

`NN` is the chronological exercise number. The name should identify the problem or capability without encoding the result.

## File responsibilities

### `task-description.md`

Contains the prompt given to the candidate and relevant interviewer clarifications. It should be sufficient to understand the exercise without relying on conversation history.

### `solution.md`

Contains the candidate's original response. Preserve it as evidence. Do not silently rewrite it after review. If a corrected solution is useful later, create a separate file with an explicit name such as `revised-solution.md`.

### `mentor-notes.md`

Contains concise metadata, review observations, evidence, working hypotheses, and the next exercise. It may include questions and answers that materially affected the exercise. It should not become a complete replacement solution.

## Recording rules

For every exercise, record at least:

- language;
- format;
- intended timebox;
- actual effort;
- status;
- candidate response location;
- observed strengths and weaknesses;
- current hypothesis;
- next step.

The global `progress/` files contain only the current handoff and cross-exercise assessment. Exercise-specific details belong here.
