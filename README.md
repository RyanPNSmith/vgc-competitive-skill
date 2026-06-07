# VGC Competitive Pokémon Skill for Claude

A Claude Skill that helps with competitive VGC (Video Game Championships) Pokémon team building, meta analysis, and strategic decision-making. Pulls data from Smogon's competitive database to give you data-driven recommendations.

## What It Does

- 🏆 **Team Building** — Generates optimized VGC team suggestions based on current meta usage statistics
- 🔍 **Team Analysis** — Evaluates your existing team for coverage gaps, weaknesses, and synergy
- ⚔️ **Moveset Optimization** — Recommends competitive movesets, items, abilities, and EV spreads
- 📊 **Meta Analysis** — Explains what's dominating the current meta and how to counter it
- 🎯 **Strategic Advice** — Provides guidance on team composition and battle strategies

## Installation

### Option 1: Install the Pre-Built Skill (Easiest)

1. Download [`vgc-competitive-skill.skill`](./vgc-competitive-skill.skill) from this repo
2. Go to [claude.ai](https://claude.ai) → **Settings** → **Capabilities** → **Skills**
3. Click **Upload Skill** and select the `.skill` file
4. Done! The skill will trigger on VGC-related questions

### Option 2: Build from Source

If you want to customize the skill:

1. Clone this repo:
   ```bash
   git clone https://github.com/YOUR-USERNAME/vgc-competitive-skill.git
   cd vgc-competitive-skill
   ```

2. Edit `SKILL.md` to your liking

3. Package it (requires Python 3):
   ```bash
   # Get the packaging script from Anthropic's skill-creator
   # Then zip the folder:
   zip -r vgc-competitive-skill.skill vgc-competitive-skill/
   ```

4. Upload as in Option 1

## Example Queries

Once installed, just ask Claude things like:

- *"Build me a competitive VGC 2025 team around Calyrex-Shadow"*
- *"Analyze my team: Incineroar, Landorus-T, Calyrex-S, Regieleki, Dirge, Wailord"*
- *"What movesets are top VGC players running on Incineroar right now?"*
- *"What's currently dominating the VGC meta and how do I counter it?"*
- *"Is Urshifu-Rapid-Strike viable in current VGC?"*

## Data Sources

This skill pulls competitive data from:

- **[data.pkmn.cc](https://data.pkmn.cc)** — Smogon's API for analyses, movesets, and usage statistics
- **Tournament results** via web search — Recent top finishes when available
- **Meta trends** — Current dominant strategies and team archetypes

## Repo Structure

```
vgc-competitive-skill/
├── README.md                      # This file
├── LICENSE                        # MIT License
├── vgc-competitive-skill.skill    # Pre-built skill (ready to install)
└── vgc-competitive-skill/         # Source files
    └── SKILL.md                   # The actual skill definition
```

## Contributing

PRs welcome! If you have improvements to the skill — better prompts, additional features, more reliable API queries — please open an issue or pull request.

Ideas for contributions:
- Add specific Smogon API endpoint references
- Add a `references/` folder with VGC mechanics documentation
- Improve the skill description for better triggering
- Add test cases to validate the skill output

## License

MIT — See [LICENSE](./LICENSE)

## Disclaimer

This is an unofficial fan project. Not affiliated with Nintendo, The Pokémon Company, or Smogon.
