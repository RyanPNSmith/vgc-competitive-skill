# VGC Competitive Pokémon Skill
 
A [Claude skill](https://docs.claude.com) for building, analyzing, and optimizing competitive **VGC (Video Game Championships)** Pokémon teams. It helps with team building, team analysis, moveset and item choices, EV spreads, viability checks, and meta questions — and it grounds its advice in **live usage stats and real tournament team lists** instead of guessing from game mechanics.
 
## What it does
 
- **Team building** — suggests Pokémon and cores that fit a concept (sun offense, Trick Room, etc.) for the current format.
- **Team analysis** — reviews a team you paste in for coverage gaps, weaknesses, and synergy problems.
- **Moveset & item optimization** — recommends moves, items, abilities, and EV spreads for a specific Pokémon.
- **Meta analysis** — explains what's dominating right now, why, and how to counter it.
- **Matchup checks** — flags the Pokémon your team is likely to struggle against.
## How it works
 
This is a *skill*, not a program. A skill is a single instruction file (`SKILL.md`) that Claude reads when the topic comes up. The file doesn't run code — it tells Claude *how* to approach VGC questions. Three rules do most of the heavy lifting:
 
**1. It defaults to the current format automatically.**
VGC rotates its rules every few months (each window is a "regulation," e.g. Regulation M-A). The skill instructs Claude to figure out the active format on its own and apply that format's legal Pokémon, banlist, and mechanics — without asking you which format you mean. You only need to name a format if you want an *old* one.
 
**2. It pulls real data before answering.**
When a question depends on what's actually winning, the skill points Claude at live sources and tells it to go read them:
 
- **Limitless VGC** — usage percentages plus full tournament team lists. The team pages show every Pokémon's exact item, ability, nature, and four moves, so Claude can see what top players really ran (not just which Pokémon they used).
- **Pikalytics** — usage, win rates, and the most common moves/items/spreads/teammates per Pokémon.
- **Smogon (data.pkmn.cc)** — sample sets, used as a secondary sanity-check.
So a claim like "Garchomp is the most-used Pokémon" or "this set is standard" comes from a tournament database Claude actually fetched, with the specific event and placement cited.
 
**3. It refuses to confuse "possible" with "good." (the Evidence Rule)**
This is the most important part, and it came directly from a real mistake. Game mechanics tell you what's *legal*; only tournament results tell you what's *good practice* — and the two often disagree. The classic example: you can only Mega Evolve one Pokémon per battle, so it *seems* pointless to put two Mega Stones on a team. But top players do it constantly, because in bring-6/pick-4 team preview the second Mega is a matchup option, not a wasted slot. The skill forbids Claude from calling something "standard," "optimal," or "illegal" from mechanics reasoning alone — it has to open real team lists and confirm first, and if it can't verify, it has to say so.
 
The practical upshot: the skill is designed to be *correctable by data*. If Claude says something and the tournament lists disagree, it's instructed to check and walk it back rather than defend the guess.
 
## Installation
 
Drop the `SKILL.md` file into your skills directory (for example, `vgc-competitive/SKILL.md`). Claude loads it automatically when a VGC question comes up.
 
```
your-skills/
└── vgc-competitive/
    └── SKILL.md
```
 
It needs **web access** so Claude can fetch the live data sources above. Without it, the skill still works from general knowledge but loses its main advantage.
 
## Example questions
 
- "Build me a team around Sneasler for the current format."
- "Analyze my team: Garchomp, Tyranitar, Froslass, Hisuian Arcanine, Sinistcha, Sneasler."
- "What moves and item is Incineroar running right now?"
- "The meta seems sun-heavy lately — how do I counter that?"
- "Is [Pokémon] viable in the current regulation?"
- "What's the standard EV spread for [Pokémon]?"
## Things to keep in mind
 
- **Data has a small lag.** Tournament databases update within days of an event, so the very newest results may not be reflected yet.
- **EV spreads are starting points.** The right spread depends on a Pokémon's exact role on *your* team, not just the format average.
- **Always test.** Meta environments shift fast; treat recommendations as informed starting points, not final answers.
## Disclaimer
 
This is a fan-made tool for competitive play. Pokémon and all related names are trademarks of Nintendo, Game Freak, and The Pokémon Company. This project is not affiliated with or endorsed by them. Data is sourced from community sites (Limitless VGC, Pikalytics, Smogon); credit and thanks to those communities.
