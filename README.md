# LearnMD

**LearnMD** is an open, Markdown-based format for writing learning content — lessons, examples, summaries, and inline knowledge checkpoints.

A `.learn.md` file is valid Markdown — readable by humans, versionable in Git, and renderable by any compatible learning player.

## Quick example

````markdown
---
lang: en
tags: [python, variables]
estimated_time: 15min
---

# Python Variables

A variable is a named reference to a value in memory.

## Assignment

```python
age = 25
name = "Alice"
```

> [!tip]
> Use descriptive names: `student_count` is clearer than `n`.

```quiz
? What operator assigns a value in Python?
- [x] =
- [ ] ==
- [ ] :=
```

## Summary

- Variable = name + value
- Python infers types dynamically
- Names are case-sensitive: `Age` ≠ `age`
````

## Key features

- **Instruction-first** — explain concepts, walk through examples, guide learners step by step
- **Inline checkpoints** — embed knowledge checks directly via ` ```quiz ` blocks (delegated to [QuizMD](https://github.com/neuroneo-md/quizmd))
- **Progressive levels** — plain `.learn.md` works anywhere; frontmatter adds metadata; special blocks add rich UI
- **Math support** — LaTeX via KaTeX, auto-detected
- **AI-native** — designed to be generated and validated by AI assistants via MCP
- **Git-native** — plain text, diff-friendly, works in any repository

## The teach → test stack

LearnMD and QuizMD are complementary:

| | LearnMD | QuizMD |
|---|---|---|
| Purpose | Teach | Assess |
| File | `.learn.md` | `.quiz.md` |
| Standalone | ✓ | ✓ |
| Together | Embeds QuizMD checkpoints | Provides scored checkpoints |

## Specification

See [SPEC.md](./SPEC.md) for the full format specification.

## Implementations

| Project | Type | Link |
|---------|------|------|
| neuroneo.md | Web player + API + MCP server | [neuroneo.md](https://www.neuroneo.md) |

> Built an implementation? Open a PR to add it here.

## Repository structure

```
learnmd/
├── SPEC.md              # Full format specification
├── CHANGELOG.md         # Version history
├── samples/             # Example .learn.md files
├── schema/
│   └── learnmd.schema.json  # JSON Schema for frontmatter validation
├── tests/
│   ├── valid/           # Files that must parse successfully
│   └── invalid/         # Files that must fail validation
└── CONTRIBUTING.md
```

## Related formats

| Format | Repo |
|---|---|
| LearnMD: instructional content | [learnspec/learnmd](https://github.com/learnspec/learnmd) |
| QuizMD: assessments | [learnspec/quizmd](https://github.com/learnspec/quizmd) |
| FlashMD: flashcards | [learnspec/flashmd](https://github.com/learnspec/flashmd) |
| NuggetMD: micro-learning | [learnspec/nuggetmd](https://github.com/learnspec/nuggetmd) |
| ExerciseMD: exercises with solutions | [learnspec/exercisemd](https://github.com/learnspec/exercisemd) |
| TrackMD: learning paths | [learnspec/trackmd](https://github.com/learnspec/trackmd) |
| CurriculumMD: reference frameworks | [learnspec/curriculummd](https://github.com/learnspec/curriculummd) |
| MediaMD: media catalogue | [learnspec/mediamd](https://github.com/learnspec/mediamd) |
| DiagramMD: diagram syntax | [learnspec/diagrammd](https://github.com/learnspec/diagrammd) |
| AnimMD: step-reveal animations | [learnspec/animmd](https://github.com/learnspec/animmd) |
| GlossaryMD: glossaries | [learnspec/glossarymd](https://github.com/learnspec/glossarymd) |
| BadgeMD: micro-credentials | [learnspec/badgemd](https://github.com/learnspec/badgemd) |
| CertMD: macro-credentials | [learnspec/certmd](https://github.com/learnspec/certmd) |
| ListenMD: speech-only episode scripts | [learnspec/listenmd](https://github.com/learnspec/listenmd) |

## License

MIT — see [LICENSE](./LICENSE)
