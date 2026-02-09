# codex-review

A Claude Code plugin that runs [OpenAI Codex CLI](https://github.com/openai/codex) code review on your current changes or reviews plans and designs.

## Prerequisites

- [Codex CLI](https://github.com/openai/codex) installed and authenticated (`codex login`)

## Installation

```bash
claude plugin add /path/to/codex-review-skill
```

Or from a git repository:

```bash
claude plugin add https://github.com/ifokeev/codex-review-skill
```

## Usage

Invoke the skill with:

```
/codex-review
```

Or just ask Claude to "review my code" / "review this plan" — the skill activates automatically.

### Mode A — Code Diff Review

Reviews actual code changes (staged, unstaged, committed).

- "review my changes"
- "review the diff"
- `/codex-review` (defaults to diff review)

### Mode B — Plan / Design Review

Reviews a plan, design, or suggested implementation from conversation context.

- "review the suggested implementation"
- "review this plan"

### Custom Instructions

Pass extra focus areas as arguments:

```
/codex-review focus on security
```

### Verbose Output

For full uncompressed output:

```
/codex-review --verbose
```

## License

MIT
