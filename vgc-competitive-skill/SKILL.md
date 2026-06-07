---
name: vgc-competitive
description: Help with competitive VGC Pokémon team building, strategy, and meta analysis. Use this skill whenever the user wants to build optimized VGC teams, analyze their current teams, get moveset recommendations, understand competitive viability, or stay informed on the current competitive meta. Pulls live data from Smogon's competitive database and usage statistics to provide data-driven team recommendations. Use for VGC strategy questions, team building guidance, moveset optimization, item selection, EV spread recommendations, and meta-game analysis.
compatibility: Requires access to data.pkmn.cc API for competitive data
---

# VGC Competitive Pokémon Assistant

A skill for helping you build, analyze, and optimize teams for VGC (Video Game Championships) competitive Pokémon battles using current meta data and competitive statistics.

## What This Skill Does

This skill helps with all aspects of competitive VGC team building and strategy by pulling data from Smogon's competitive database:

- **Team Building** - Generates team suggestions based on current meta usage statistics and top tournament finishes
- **Team Analysis** - Evaluates your existing team for coverage, weaknesses, and synergy issues
- **Moveset Optimization** - Recommends the best movesets, items, abilities, and EV spreads for specific Pokémon in the current meta
- **Meta Analysis** - Explains what Pokémon are dominating, why, and how to counter them
- **Strategic Advice** - Provides guidance on team composition, typing coverage, and battle strategies

## How to Use This Skill

### 1. Building a New Team
Provide the current VGC season/series and your team concept (e.g., "sun-based hyper offensive team" or "trick room setup"). The skill will:
- Query current meta usage statistics
- Recommend Pokémon that fit your strategy
- Suggest competitive movesets and EV spreads
- Identify synergy opportunities and coverage gaps

### 2. Analyzing an Existing Team
Paste your current team (with movesets, items, abilities, EVs if possible) and ask for analysis. The skill will:
- Check each Pokémon's viability in the current meta
- Identify coverage gaps and problematic matchups
- Suggest improvements or alternatives
- Rate the team's overall competitiveness

### 3. Moveset & Item Optimization
Ask about a specific Pokémon (e.g., "What moves should my Incineroar run in VGC 2025?"). The skill will:
- Pull the most common movesets from competitive data
- Explain the reasoning behind each move choice
- Suggest item/ability combinations
- Provide EV spread recommendations

### 4. Understanding the Meta
Ask questions like "What's dominating VGC right now?" or "How do I counter the current meta?" The skill will:
- Analyze current usage statistics
- Identify top Pokémon and teams
- Explain the meta narrative
- Suggest strategies to exploit weaknesses

## Data Sources

This skill uses:
- **Smogon API** (data.pkmn.cc) - Competitive movesets, analyses, and usage statistics for VGC formats
- **Tournament results** - Recent top finishes and team lists when available
- **Meta trends** - Current dominant strategies and team archetypes

## Important Notes

- **Format Specificity** - VGC rules change seasonally (by "series"). Always specify the current series when asking for team advice
- **Timing** - Meta analysis reflects the most recent available data; may lag behind very new tournament results by a few days
- **EV Spreads** - Common spreads are provided, but exact EV recommendations depend on your specific team and role within it
- **Testing** - All team suggestions should be tested in practice; meta environments evolve quickly

## Example Queries

- "Build me a competitive VGC 2025 team around Indeedee"
- "Analyze my team: Incineroar, Landorus-T, Calyrex-S, Regieleki, Dirge, Wailord"
- "What movesets are competitive Landorus-T running in current VGC?"
- "The meta seems to be sun-based right now—how do I counter that?"
- "Is [Pokémon] viable in VGC 2025?"
