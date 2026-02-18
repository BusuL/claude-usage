# claude-usage

Visualise your Claude Code token usage — with cost estimates and date filtering.

```bash
npx github:BusuL/claude-usage
```

Opens a dashboard at **http://localhost:3456**. All data stays on your machine.

## Features

- **Token usage** across all conversations, projects, and models
- **Estimated API cost** per session and in total (Haiku / Sonnet / Opus pricing)
- **Date range filter** — 7d / 30d / 90d / All time
- **Daily bar chart** and model breakdown donut
- **Most expensive prompts** ranked by token cost
- **Session drill-down** — see every message in a conversation
- **Search & sort** across all sessions

## Usage

```bash
# Run directly (no install needed)
npx github:BusuL/claude-usage

# Custom port
npx github:BusuL/claude-usage --port 8080

# Don't auto-open browser
npx github:BusuL/claude-usage --no-open
```

## How it works

Reads `.jsonl` session files from `~/.claude/projects/` — the same files Claude Code writes locally. No data leaves your machine.

## Cost disclaimer

Cost estimates use published [Claude API pricing](https://www.anthropic.com/pricing). Claude Code Max subscribers pay a flat monthly fee — the cost shown here represents the equivalent API value, not what you actually pay.

| Model  | Input per 1M | Output per 1M |
|--------|-------------|---------------|
| Haiku  | $0.80       | $4.00         |
| Sonnet | $3.00       | $15.00        |
| Opus   | $15.00      | $75.00        |
