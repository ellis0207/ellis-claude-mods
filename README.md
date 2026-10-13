# Ellis's Claude Mods

Reusable [Claude Code](https://claude.com/claude-code) mods, one plugin per folder under `plugins/`. Install only what you need.

| Mod | What it does | Source |
| --- | --- | --- |
| [savvy-progress](plugins/savvy-progress) | A progress bar above the prompt and a live agents panel (`/agents-info`) showing running, finished and planned subagents with model, progress, context, estimated cost and time. | [johnnyvizz/claude-kit](https://github.com/JohnnyVizz/claude-kit/tree/main/plugins/savvy-progress) @ `c871c15`, MIT |

## Install

### From the marketplace

In Claude Code:

```
/plugin marketplace add ellis0207/ellis-claude-mods
/plugin install savvy-progress@ellis-claude-mods
```

Restart the session afterwards. Because this repo is private, Claude Code needs GitHub access to it (your `gh` login or git credentials).

### By hand

```bash
git clone https://github.com/ellis0207/ellis-claude-mods.git ~/ellis-claude-mods
claude --plugin-dir ~/ellis-claude-mods/plugins/savvy-progress
```

To load a mod in every session, add it to `env` in `~/.claude/settings.json` (separate several folders with `:`):

```json
{ "env": { "CLAUDE_CODE_PLUGIN_DIRS": "~/ellis-claude-mods/plugins/savvy-progress" } }
```

## Adding a mod

Put it in `plugins/<name>/` with a `.claude-plugin/plugin.json`, then add an entry to `.claude-plugin/marketplace.json` and the table above. Mods copied from elsewhere keep their original license and note the source commit.
