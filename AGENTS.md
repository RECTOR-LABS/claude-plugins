<!-- Satellite context file — extends the global hub (~/.claude/CLAUDE.md | ~/.pi/agent/AGENTS.md). Host-neutral; project-specific only. Do not duplicate hub standards here. -->

# RECTOR-LABS Claude Plugins

> The `rector-labs` plugin marketplace for Claude Code — a single catalog for the RECTOR-LABS Solana security skills.

## Install

```bash
/plugin marketplace add RECTOR-LABS/claude-plugins
/plugin install solana-cpi-safety@rector-labs
```

## Notes

- This repo holds `marketplace.json` (the catalog) + `README.md`. The actual skills ship from their own repos (e.g. `RECTOR-LABS/solana-cpi-safety-skill` ships `.claude-plugin/plugin.json`; this repo lists it in `marketplace.json`).
- To list another RECTOR-LABS skill, add an entry to `marketplace.json`.