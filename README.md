# avici plugin for Claude Code

Talk to your [avici](https://avici.club) account inside Claude — wallets, cards,
balances, and activity. Read-only; you sign in with avici email + OTP (OAuth).

## Install

```bash
claude plugin marketplace add VaibhavArora19/avici-plugin
claude plugin install avici@avici-official
```

Then run `/mcp` → **avici** → **Authenticate** → log in with your email + the OTP.

You also get slash commands (Claude Code): `/balance`, `/activity`, `/cards`,
`/wallets`, `/refunds`, `/spending`, and `/reveal` (reveal is Claude Code only).

## What's inside

This repo is just the plugin/marketplace wrapper. It registers a connector that
points at the hosted avici MCP server; no server code or secrets live here — the
only thing it carries is the public connector URL (auth is handled by OAuth).

- `.claude-plugin/marketplace.json` — marketplace manifest (`avici-official`)
- `plugin/` — the `avici` plugin: manifest, `.mcp.json` (connector URL), commands
