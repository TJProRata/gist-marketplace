# Gist Marketplace

A Claude Code plugin marketplace containing reusable commands for the Gist GEO project.

## Installation

### 1. Add the Marketplace

```
/plugin marketplace add TJProRata/gist-marketplace
```

### 2. Install the Plugin

```
/plugin install geo-plugin@gist-marketplace
```

### 3. Restart Claude Code

Restart Claude Code to load the new plugin commands.

### 4. Verify Installation

Run `/help` to see the new commands, or use `/plugin` → "Manage Plugins" to review installed plugins.

## Available Plugins

### geo-plugin

Commands for the Gist GEO project workflow.

| Command | Description |
|---------|-------------|
| `/hello` | Greet the user with a personalized message |
| `/geo_prime` | Quick project state check |
| `/geo_prime_askgist` | Context for Ask Gist AI chat |
| `/geo_prime_backend` | Context for Convex backend work |
| `/geo_prime_component` | Context for creating shadcn-style components |
| `/geo_prime_dashboard` | Context for dashboard pages and features |
| `/geo_prime_onboarding` | Context for onboarding flow work |
| `/geo_bug` | Create a bug fix plan in specs/*.md |
| `/geo_chore` | Create a chore plan in specs/*.md |
| `/geo_commit` | Create a commit with conventional commit format |
| `/geo_feature` | Create a feature plan in specs/*.md |
| `/geo_generate_branch_name` | Create a new branch from main |
| `/geo_install` | Install and setup project |
| `/geo_pull_request` | Push branch and create PR to main |
| `/geo_start` | Start dev servers |

## Managing the Plugin

```bash
# Disable without removing
/plugin disable geo-plugin@gist-marketplace

# Re-enable
/plugin enable geo-plugin@gist-marketplace

# Uninstall completely
/plugin uninstall geo-plugin@gist-marketplace

# Remove marketplace
/plugin marketplace remove gist-marketplace
```

## Team Installation

Add to your project's `.claude/settings.json` to auto-install for all team members:

```json
{
  "plugins": {
    "marketplaces": ["TJProRata/gist-marketplace"],
    "installed": ["geo-plugin@gist-marketplace"]
  }
}
```

Team members will have the plugin installed automatically when they trust the repository folder.

## Directory Structure

```
gist-marketplace/
├── .claude-plugin/
│   └── marketplace.json      # Plugin registry
├── geo-plugin/
│   ├── .claude-geo-plugin/
│   │   └── plugin.json       # Plugin metadata
│   └── commands/             # Slash command definitions
└── README.md
```

## License

MIT
