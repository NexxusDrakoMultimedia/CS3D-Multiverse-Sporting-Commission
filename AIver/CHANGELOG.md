# Changelog

## 1.0.2 — colours reverted, Team folder removed

The named colours and national-team files from 1.0.1 did not work in game, so both are
withdrawn. No competition, calendar, club or name data changed.

**`Data\Team` removed entirely.** The five national-team files added in 1.0.1 are gone, and
so is AFC Nexxus Drako's — the folder no longer exists. Every club in the world, AFC Nexxus
Drako included, now has its kit, reputation and squad generated at career start from its
division and its nation's name lists. The twenty-five youth players written for AFC Nexxus
Drako go with the file; the club itself still plays in the Itavrnai twelfth flight.

**Colours back where 1.0 had them.** The five associations with declared colours carry their
kit lines in their `Data\League` file again, as hex, exactly as in 1.0 — `#7f0000`/`#ffd900`
for Vyktoria, `#7f0000`/`#00007f` for New Bradman, `#ffff00`/`#0000ff` for the Itavrnai
Union, `#ff0000`/`#ffff00` for Ryukawa, `#00007f`/`#ffffff` for Castolo and Minanda.

---

## 1.0.1 — colours

A colour-only release. No competition, calendar, club or name data changed.
**Withdrawn in 1.0.2 — the changes below did not work in game.**

**Hex codes replaced with the game's colour names.** Every kit in 1.0 was written as a hex
code — `#7f0000`, `#ffd900` and so on — which the stock data never does. All of them are now
the game's own names.

| Nation | 1.0 | 1.0.1 |
|---|---|---|
| Itavrnai Union | `#ffff00` / `#0000ff` | yellow / blue |
| Vyktoria | `#7f0000` / `#ffd900` | claret / gold |
| New Bradman | `#7f0000` / `#00007f` | claret / darkblue |
| Ryukawa | `#ff0000` / `#ffff00` | red / yellow |
| Castolo and Minanda | `#00007f` / `#ffffff` | darkblue / white |
| AFC Nexxus Drako | `#7f0000` / `#ffd900` | claret / gold |

**National kits moved out of the League files.** In 1.0 the five nations' colours sat in
their `Data\League` file after `! Country`, where the game does not read them — stock league
files carry no kit lines at all. Each now has its own `Data\Team\<Nation>.txt`, the same
shape a club file takes, on the pattern of the game's `Zimbabwe.txt` and `Moldova.txt`. The
League files are back to plain `! Country` and `! Names`.

**Documented the colour vocabulary.** The stock data uses 21 colour names: `amber`, `black`,
`blue`, `brown`, `claret`, `darkblue`, `darkgray`, `darkgreen`, `darkred`, `gold`, `green`,
`lightblue`, `lightgreen`, `lightyellow`, `midblue`, `orange`, `red`, `redwine`, `violet`,
`white` and `yellow`, on `shirt`, `sleeves`, `stripes`, `shorts` and `socks`.

---

## 1.0 — first release

The first public build of the Multiverse Sporting Commission. Everything before this was
development, and none of it is carried forward here.

**The world.** 24 member associations, 130 divisions, 2,144 clubs, fourteen regions in
four blocs plus ten unregioned nations. Pyramids of 2, 4, 8 and 12 tiers, with promotion
and relegation chaining exactly so division sizes never drift. Vyktoria and New Bradman
reproduce their NationStates league threads down to tier four, club for club.

**Domestic competitions.** 96 of them — the same five in every association, named in its
own register: National Cup, League Cup, Semi-Pro Cup, Amateur Cup and Super Cup. Band cups
enter by division, so no club is ever in two of them, and each cup in a nation runs on its
own lane of weeks. Only the National Cup feeds the MSC Cup Winners Cup.

**MSC competitions.** 25 — the Champions Cup, Challengers League and Conference Trophy as
a staggered qualifying cascade sharing one calendar from the group stage on; the Cup
Winners Cup and the 256-club Coronation Tournament in the off-weeks; nine Coronation
qualifiers entering all 2,144 clubs; the Super Cup and the Ultimate Championship to close
the season. National teams get the World Cup, Nations League, three bloc championships,
the Associates Trophy and three friendly windows, on three interlocking cycles that never
collide.

**Scouting.** Eight providers and 23 packages, modelled one-for-one on the game's own
eight, with their header values and prices carried over. Packages are tiered by what they
actually report rather than by selection counts, which the engine does not enforce.

**Names.** 48 lists, about 29,500 names, all Windows-1252 safe.

**Teams.** One `Data\Team` file: AFC Nexxus Drako, in the Itavrnai twelfth flight.

**Start year** 2029.

### Known limits found along the way

- A pyramid cannot exceed 12 tiers.
- A competition cannot exceed 256 teams.
- `+ add 1 venue` occupies a seat in the field.
- `Scope selections` is not enforced on scouting packages.

None of these appear in the data-editing manual.
