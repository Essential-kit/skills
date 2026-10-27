# Essential Kit Skills

A public collection of installable agent skills for planning, implementing, reviewing, and maintaining software. The pack works with the [skills](https://skills.sh) CLI and any agent that reads `SKILL.md` files.

## Install

Install the whole pack:

```bash
npx skills add Essential-kit/skills
```

Install selected skills:

```bash
npx skills add Essential-kit/skills --skill code-review --skill tdd
```

List the pack without installing:

```bash
npx skills add Essential-kit/skills --list
```

Install globally:

```bash
npx skills add Essential-kit/skills --global
```

Add `--agent <name>` to target a specific agent. Without `--global`, the CLI installs into the current project.

## Skills

| Skill | What it does |
| --- | --- |
| `code-review` | Four-axis review: standards, spec, simplification, and performance/scaling optimization. |
| `codebase-design` | Deep-module design vocabulary and interface improvement. |
| `diagnosing-bugs` | Diagnosis loop for hard bugs and performance regressions. |
| `domain-modeling` | Build glossaries and ADRs; sharpen the project's domain language. |
| `grill-with-docs` | Stress-test a plan while producing ADRs and glossary entries. |
| `grilling` | Relentless interview to sharpen a plan, decision, or idea. |
| `handoff` | Compact a conversation into a handoff document for another agent. |
| `implement` | Implement a piece of work from a spec or ticket set. |
| `implement-spec` | Implement a spec and tickets, and close the corresponding GitHub issues. |
| `improve-codebase-architecture` | Scan for deepening opportunities and present them as an HTML report. |
| `pr` | Author or revise a PR with scope checks, a summary, added/removed diff, evidence, and merge danger. |
| `research` | Research primary sources and capture the findings as a Markdown report. |
| `tdd` | Test-driven development with behavior-focused tests. |
| `to-spec` | Turn the current conversation into a spec published to GitHub Issues. |
| `to-tickets` | Break a spec into tracer-bullet GitHub tickets and dependencies. |
| `writing-for-agents` | Write skills, `AGENTS.md` files, and other agent-consumed documents. |

## Highlights

- **No per-repo setup step.** Skills read `GLOSSARY.md`, `GLOSSARY-MAP.md`, and ADRs when they exist.
- **GitHub-native delivery.** `to-spec`, `to-tickets`, `implement`, and `implement-spec` use GitHub Issues and the canonical `ready-for-agent` label through the `gh` CLI.
- **Research-backed review.** `code-review` runs Standards, Spec, Simplification, and Optimization reviewers in parallel; `skills/code-review/SCALING.md` is the optimization reference.

## Requirements

- Node.js 22.20 or later for the `skills` CLI.
- An authenticated `gh` CLI for the GitHub Issues workflows (`to-spec`, `to-tickets`, `implement`, `implement-spec`, and `code-review` when it fetches an issue) and for `pr` submission.

## Repository layout

```text
skills/<name>/SKILL.md
skills/code-review/SCALING.md
skills.sh.json
```

## Credits and license

This pack is derived from [Matt Pocock's skills](https://github.com/mattpocock/skills), used under the MIT License. The `code-review` Simplification axis was inspired by [Meltiply's code-review skill](https://github.com/MeltiplyOrg/meltiply/blob/master/.agents/skills/code-review/SKILL.md), with original wording. Its Optimization axis and `SCALING.md` are original research with cited sources. The `pr` skill credits Dex Horthy's `show-me` and adapts Meltiply's `pr` workflow; see `skills/pr/CREDITS.md`.

See [LICENSE](LICENSE).
