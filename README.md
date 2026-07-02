# GetJelly Claude Plugin

Access GetJelly's creator search, profile spy, and content analysis directly from Claude.

## Installation

### Option 1: Via Claude Marketplace (when available)
```bash
/plugin marketplace add getjelly/claude-plugin
/plugin install getjelly
```

### Option 2: Manual Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/getjelly/claude-plugin.git
   ```

2. Copy the plugin to your Claude plugins directory:
   ```bash
   cp -r getjelly-claude-plugin ~/.claude/plugins/getjelly
   ```

3. Restart Claude Code or reload plugins

## Setup

1. Get your API token from [GetJelly AI Integration](https://app.getjelly.ai/ai-integration)
2. When using the plugin, provide your token when prompted

## Available Commands

- **Spy Profile**: Look up any Instagram/TikTok creator
- **Search Creators**: Semantic search by description
- **Analyze Posts**: Content analysis (coming soon)

## Examples

```
spy https://instagram.com/username
find fitness creators under 50K followers with high engagement
```

## Documentation

Full documentation: https://app.getjelly.ai/ai-integration

## Support

- Issues: https://github.com/getjelly/claude-plugin/issues
- Email: support@getjelly.ai
- Website: https://getjelly.ai

## License

MIT
