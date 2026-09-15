# Changelog

All notable changes to the **Multiverse Sporting Commission** football world.

Created by Nexxus Drako, with Claude's assistance.

---

## 1.1 — current

### The continental cascade

The three league competitions now run as a proper chain, UEFA-style, and the calendar
enforces it rather than merely implying it.

- **Champions Cup** is drawn in week 1 and qualifies in weeks 3 and 5.
- **Challengers League** is drawn in week 6, *after* Champions Cup qualifying has
  finished, and takes the 16 clubs knocked out of it. Its own qualifying runs weeks 7
  and 9.
- **Conference Trophy** is drawn in week 10 and takes the 16 knocked out of Challengers
  qualifying. Its own qualifying runs weeks 11 and 13, and its 32 direct entrants come
  entirely from the smaller associations.

Clubs dropping down enter seeded, straight into the group stage. Previously the
Conference Trophy was resolving before the Challengers League, so the drop-down clubs
could not have been known when it was drawn.

### A shared continental calendar

The four continental competitions never share a club after qualifying, so the big three
now play on the same nights throughout:

| Stage | Champions / Challengers / Conference |
|---|---|
| Group stage | 15, 17, 19, 21, 23, 25 |
| Round of 16 | 28, 30 |
| Quarter finals | 32, 34 |
| Semi finals | 37, 39 |
| Final | 43 |

The **Cup Winners Cup** is the exception and sits in the off-weeks between them — 16,
22, 27, 29, 31, 33, 36, 38, with its final in week 42. The **Coronation Tournament**,
which enters every club in the Commission, does the same: 10, 12, 14, 20, 26, 35, 40,
and its final in week 50.

### Tighter domestic cups

Every domestic cup of four rounds or more was re-timed so the early rounds come thick
and fast and the later ones breathe. Gaps now grow across the competition — two or
three weeks between opening rounds, eight or ten by the semi finals — instead of being
spread evenly. Two-legged rounds keep both legs a fortnight apart, and nothing runs
past week 41, which keeps every domestic final clear of the MSC finals in weeks 42 to
45 and of the finale window in 50 to 52. Deliberately short competitions such as the
Castolo Supercopa keep their own tight dates.

### Fixes

- Conference Trophy round of 16 had been scheduled before its own group stage finished.
- The Open Reach Coronation qualifier is the only one of the nine that needs three
  rounds rather than four; the Coronation was reading a fourth round that did not exist.
- Determi's cup final is the *Final Rite*, not the Final — the Cup Winners Cup was
  referencing a round name that does not exist.
- Scouting provider section headers were missing their `Product` and `Market` keywords.
- Itavrnai Grand Conclave jumped from a 16-team group stage straight to the quarter
  finals; a round of 16 now sits between them.
- Jarokn's Trial of Heroes finished on an odd three clubs; its bracket was rebuilt.

---

## 1.0 — initial standalone-world release

### The Commission

24 member associations, 2,144 clubs and 130 divisions, in four blocs plus ten
unregioned nations.

- **Itavrnai Union** — Itavrnai Union, Vyktoria, New Rythorn
- **New Bradmanian Commonwealth** — New Bradman, Ryukawa, Castolo and Minanda
- **Cyberya** — Layn's Wyred, Determi, Nexxie, Jarokn
- **Galatyan** — Mancunya, Centralya, Wyrmwoode, Esmeraldys
- **Unregioned** — Veslavia, Valcarena, Tianlu, Akwanta, Sindhara, Hanseong, Mazamba,
  Qamaria, Selanting, Norvalia

Vyktoria and New Bradman reproduce their NationStates league threads exactly down to
tier four, club for club and in thread order; the tiers below are merged and shuffled
from both sources. Every other nation is original.

Each pyramid keeps a flavoured top flight and counts in numerals beneath it. Cyberya
is the exception and stays thematic all the way down. Promotion and relegation chain
correctly everywhere, so division sizes never drift.

### Competitions

- 27 domestic cups, with deliberately different rules — all-in draws, staggered entry
  by rank, group-stage openers, two-legged everything, single-match rounds.
- Four continental club competitions: Champions Cup, Cup Winners Cup, Challengers
  League, Conference Trophy.
- **MSC Super Cup** — the four holders in a single group, three match days, winner
  through to the decider.
- **MSC Coronation Tournament** — every club in the Commission has a road in, through
  nine regional qualifiers feeding a 142-club final tournament.
- **MSC Ultimate Championship** — Coronation winner against Super Cup winner, one
  match, week 52, with nothing else played in week 51.
- National teams: MSC World Cup, MSC Nations League, three friendly windows, and four
  bloc championships covering all 24 nations without overlap — the **Nexxus Drako
  Shield** for the Itavrnai Union and the Commonwealth together, the Cyberya and
  Galatyan Championships, and the Associates Trophy for the unregioned ten.

### Names

48 name lists, 420 given names and 900 surnames per nation, about 29,500 names. Nineteen
nations draw on a real name-frequency corpus filtered per nation; Welsh and Scots are
curated by hand because the corpus only knows "GB"; the five invented nations are
generated from syllable sets in their own register. Within the Itavrnai Union, Galatyan
and Commonwealth blocs each nation keeps its own register as 70% of its lists and takes
the rest from its neighbours.

An earlier build used a single shared 183,000-name pool, which slowed the game badly.
Per-nation lists replaced it.

### Packaging

- `Package.ini`, a user-facing `README.md`, `Data\StartYear.txt` set to 2030.
- Eight scouting providers under `Data\ScoutingProvider\`.
- Every data file written as ANSI (Windows-1252) to match the stock data, CRLF for
  league and provider files, bare LF with no trailing newline for the name lists.
- Fourteen damaged names carrying replacement characters were repaired; one
  unrecoverable entry was dropped.

### Two undocumented engine limits

Both were hit during development and neither appears in the manual.

- **A pyramid cannot exceed 12 tiers.** The Itavrnai Union was rebuilt from 16 tiers of
  16 to 12 flights of 18, 22 and 24, keeping all 256 clubs.
- **A competition cannot exceed 256 teams.** The Coronation cannot be one 2,144-club
  bracket, so it became nine qualifiers, none larger than 256, feeding a final draw.

### Known install trap

Name lists inside a package are **not** read at runtime. They must be copied into the
shared `Documents\My Games\Championship Soccer\Data\Names\` folder or careers fail to
save with *"Invalid or empty career second names"*. This is step 2 of the install
instructions in the README.
