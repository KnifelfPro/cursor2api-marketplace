# Cursor2API Marketplace

Cursor2API marketplace and extension files for Claude Code, Codex, Gemini CLI,
Cursor, OpenCode, and Hermes.

Install the MCP server first:

```bash
npm install -g cursor2api-mcp
```

Set `CURSOR_API_KEY` in your shell or in the target client config.

## Claude Code

```bash
claude plugin marketplace add KnifelfPro/cursor2api-marketplace
claude plugin install cursor2api@cursor2api
```

Use:

```text
/cursor2api:cursor Fix the failing tests gpt-5.5
/cursor2api:cursorx Fix the failing tests gpt-5.5
```

## Codex

```bash
codex plugin marketplace add KnifelfPro/cursor2api-marketplace
codex plugin add cursor2api@cursor2api
```

Use:

```text
Use cursor to fix the failing tests gpt-5.5
Use cursorx to call Cursor directly gpt-5.5
```

## Gemini CLI

```bash
gemini extensions install https://github.com/KnifelfPro/cursor2api-marketplace
```

Use:

```text
/cursor Fix the failing tests gpt-5.5
/cursorx Fix the failing tests gpt-5.5
```

## Cursor

Cursor can import remote rules from GitHub. Import this repository as a remote
rule source, then select `cursor/rules/cursor2api.mdc`.

MCP config template:

```text
cursor/mcp.json
```

## OpenCode

Install command templates without cloning:

```bash
mkdir -p ~/.config/opencode/commands
curl -fsSL https://raw.githubusercontent.com/KnifelfPro/cursor2api-marketplace/main/opencode/commands/cursor.md -o ~/.config/opencode/commands/cursor.md
curl -fsSL https://raw.githubusercontent.com/KnifelfPro/cursor2api-marketplace/main/opencode/commands/cursorx.md -o ~/.config/opencode/commands/cursorx.md
```

Configure MCP with `cursor2api-mcp-install` and choose OpenCode.

## Hermes

Install templates without cloning:

```bash
mkdir -p ~/.hermes
curl -fsSL https://raw.githubusercontent.com/KnifelfPro/cursor2api-marketplace/main/hermes/config.yaml -o ~/.hermes/cursor2api.config.yaml
curl -fsSL https://raw.githubusercontent.com/KnifelfPro/cursor2api-marketplace/main/hermes/cursor-command.md -o ~/.hermes/cursor-command.md
curl -fsSL https://raw.githubusercontent.com/KnifelfPro/cursor2api-marketplace/main/hermes/cursorx-command.md -o ~/.hermes/cursorx-command.md
```

Merge `hermes/config.yaml` into your existing `~/.hermes/config.yaml` if one
already exists.
