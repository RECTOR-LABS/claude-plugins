# RECTOR-LABS Claude Plugins

The `rector-labs` plugin marketplace for Claude Code — a single catalog for the
RECTOR-LABS Solana security skills.

## Install

```bash
/plugin marketplace add RECTOR-LABS/claude-plugins
/plugin install solana-cpi-safety@rector-labs
```

Restart Claude Code after installing. Installed as a plugin, a skill's command
is namespaced (for example `/solana-cpi-safety:audit-cpi`).

## Skills in this marketplace

A Solana security workflow: find vulnerabilities, prove them, respond to incidents.

| Skill | Stage | Status |
|-------|-------|--------|
| [solana-cpi-safety](https://github.com/RECTOR-LABS/solana-cpi-safety-skill) | Find — detect and prevent CPI vulnerability classes | Available |
| solana-poc-forge | Prove — forge runnable PoCs and exploits | Planned |
| solana-incident-response | Respond — triage, contain, and disclose live incidents | Planned |

Each skill is also installable on its own — see its repository for `npx` and
clone-based install options.

## Adding a plugin to this marketplace

Add an entry to `.claude-plugin/marketplace.json` pointing at the skill's repo:

```json
{
  "name": "solana-poc-forge",
  "source": { "source": "github", "repo": "RECTOR-LABS/solana-poc-forge-skill" },
  "description": "..."
}
```

Each listed repo must contain its own `.claude-plugin/plugin.json`. CI validates
the catalog on every push.
