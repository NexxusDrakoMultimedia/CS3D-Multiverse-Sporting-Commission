# Changelog

All notable changes to the **Multiverse Sporting Commission** football world.

Created by Nexxus Drako, with Claude's assistance.

Everything before this release was a development build. What were versions 1.0
through 1.4 are renumbered 0.0 to 0.4, and this is the first release proper.

---

## 1.0 — first release

### The World Cup was a nation short

`+ add 1 venue` picks a host ground, and the engine counts that pick as an entry.
With the nations written as `+ <1 add 1 team` through `+ <24`, the venue already
held seat one, so the `<1` line never fired and only 23 of the 24 got in. The
nations are now plain `+ add 1 team` lines. The validator was making the same
mistake in reverse — counting the venue as a competitor — and now ignores it.

### The Coronation Tournament

Nine qualifiers, every one at the same rate of one club in sixteen over four
rounds, which brings 134 through. The Coronation trims the odd twelve in a
**Preliminary Round** and then starts its own numbering clean: First Round of
128, Second, Third, Fourth, then Quarter Finals, Semi Finals and the Coronation
Final. The old seeded preliminary and the borrowed numbering are gone.

### A Super Cup final

The four continental holders still play a group, but the top two now meet in a
**Super Cup Final** in week 50. That winner goes to the Ultimate Championship —
or, if it also won the Coronation and so cannot play itself, the club it beat
in that final, and then the group table behind them.

### Room to breathe

The club calendar is stretched across the whole season and every competition
keeps a uniform shape. Continental groups run on three-week gaps from week 16 to
30, knockouts from 32 to 42, finals in 44. The Cup Winners Cup keeps to the
off-weeks. Domestic cups now run from week 3 to week 46 rather than 4 to 41.

Within a nation, each cup gets its own **lane** — its own residue class of weeks
— so two cups a club could be in never fall on the same night. Cups drawing from
disjoint tier bands share a lane, because no club can be in both.

### Domestic competitions rebuilt

Every hand-written domestic cup is gone and each association now runs the same
set, named in its own register: a **National Cup** for the whole pyramid, band
cups for the tiers beneath it, and a **Super Cup** — National Cup holders against
the champions, one match, week two, with the league runners-up taking the second
seat when one club won both.

Which band cups an association gets follows the depth of its pyramid. Four tiers
is a professional half and an amateur half with no middle, so no Semi-Pro Cup.
Eight tiers bottoms out at semi-professional, so no Amateur Cup. Only the
twelve-tier Itavrnai pyramid carries all three. Castolo and Minanda, at two
tiers, has a League Cup and nothing below it.

The band cups enter by division rather than by country, which is how the stock
National Cup of Germany seeds its rounds, so each takes exactly the tiers it is
named for and no club is in two of them. Where a band does not hold a power of
two — the Itavrnai amateur tiers hold 96 — the opening round seeds the surplus
out rather than breaking the bracket.

This fixes three faults at once. The Itavrnai Grand Conclave, a second all-comers
cup, is gone. The Supercopa Unida was a four-team affair where every other
association had a two-team super cup, and is now one match like the rest. And the
super cups that pointed at a round their nation's cup does not have — Determi
closed on a *Final Rite*, Jarokn on an *Apotheosis* — now all close on a Final,
because every National Cup is built to the same bracket.

The MSC Cup Winners Cup takes the 24 National Cup winners.

### One naming rule for every round

Round names are standard throughout: **Round of N**, **Quarter Final**, **Semi
Final**, **Final**, and a **Preliminary Round** wherever a field has to be seeded
down to a power of two. Quarter Final, Semi Final and Final are reserved for
competitions that play to a single winner — the Coronation qualifiers stop early
and send several through, so their rounds are named for the field they start
with. The Super Cup's decider is now simply a Final.

The eleven Coronation qualifiers were regrouped so every one holds a power of two
— 256, 128, 64 or 32 — which means no qualifier needs a preliminary or a bye at
all, and each still qualifies at the same one club in sixteen.

### AFC Nexxus Drako

Takes the bottom place in the Itavrnai twelfth flight, at reputation nil, with a
`Data\Team` file of its own: twenty-five players, none over 20 at the 2029 start,
ability 58–95 against potential 207–228. Claret and gold.

### Colours and start year

Vyktoria, New Bradman, the Itavrnai Union, Ryukawa and Castolo and Minanda carry
national colours. The start year is **2029**, whose season runs into the 2030
World Cup.

---

## 0.4

### Backup entries were biased, and are not any more

Six competitions filled empty seats from a list of lines that all shared one threshold —
24 lines of `+ <24 add 1 from "…"` on the Cup Winners Cup, for instance. Each line fires
at most once and only while the field is still short, so a gap anywhere was filled by
whichever association sat highest in the list. Since the list ran in reputation order,
that meant the strongest associations took every spare seat.

The stock European Cup shows the correct shape: one **incrementing** threshold per seat,
with the fallback written directly beneath the entry it backs up.

```
+ <41 add 1 cup-winner "National Cup of England Final"
+ <41 add 1 from "England"
+ <42 add 1 cup-winner "National Cup of Spain Final"
+ <42 add 1 from "Spain"
```

Now every seat is owned by one association or one trophy, and falls back to itself:

- **Cup Winners Cup** — each association's trophy, backed by that association's league.
- **Super Cup** — each continental trophy, backed by the club beaten in its final.
- **Ultimate Championship** — seat one the Coronation winner, seat two the Super Cup
  group, passing down the table if the same club holds both.
- **World Cup** — one seat per nation instead of 24 lines racing for 24 places.
- **Supercopa Unida** and the **Vyktoria Charity Shield** — the cup holder's seat backed
  by the league, then the league placings behind it.

### Matching the stock layout

Domestic cups now write `+ draw` before round one, as the National Cup of Germany does,
rather than after it. Every one of the 24 league files was checked against the stock
layout — section key order, even division sizes, the presence of `! Country` and
`! Names`, and draw placement — and all 24 now conform.

---

## 0.3

### The World Cup

Four groups of six rather than eight groups of three, five match days each, and the top
**four** of every group go through to a round of 16. How many advance is set by the next
round's span — eight groups into a round of 16 is two each, four groups into the same
round is four each — which is how the rest of this world's group stages already read;
the manual does not document a directive for it.

The knockout rounds are renamed: **Semi Final** and **Third Place Playoff**, in place of
"Half finals" and "Match for third place".

Weeks move from 48–52 to 47–51: group stage 47, 47, 48, 48, 49, round of 16 and quarter
finals in 50, and the semi final, third place playoff and final in 51.

### The Cup Winners Cup

Main cups only. It previously took all 27 domestic knockout trophies, so the Itavrnai
Union, New Bradman and Ryukawa each had two entrants while everyone else had one. The
Grand Conclave, the New Bradman League Cup and the Ryukawa Sakura Shield are still
played at home but no longer qualify, which leaves exactly 24 — one per association.

The bracket is rebuilt to match: a **Preliminary Round** of the sixteen lowest-ranked
holders, with the top eight seeded straight through, so eight winners join eight byes
in the round of 16. Weeks are unchanged, still in the off-weeks between the three
league competitions.

### One club, two trophies

Two competitions could be left short because a single club filled two of their seats,
which is the same fault that stops a cup being played at all.

The **Ultimate Championship** seats the Coronation winner against whoever topped the
Super Cup group. One club can be both, and cannot play itself — that left a one-club
final. The Super Cup runner-up now steps up, with third place behind them.

The **MSC Super Cup** seats all four continental holders. The three league competitions
exclude one another, but the Cup Winners Cup does not, so a club can win its domestic
trophy and a continental one in the same season and leave a group of three. Beaten
finalists now fill any empty seat, in the same order.

### Cycles

**Three interlocking cycles, and no two ever share a year.** The World Cup counts from
2002 on a four-year offset, the Nations League from 2003 on a two-year one, and the four
bloc championships move to 2004 on a four-year one, which puts them midway between World
Cups the way real continental championships sit. 2030 — the suggested start year — is a
World Cup season; 2031 a Nations League one; 2032 the blocs. Previously the bloc
championships ran on the World Cup's own year and fired alongside it.

The validator was checking that a group stage always advances two per group. It now reads
the advancing count from the next knockout round and checks that it divides evenly by the
number of groups and leaves at least one team behind.

---

## 0.2

### Scouting providers rebuilt on the stock eight

The providers are now modelled one-for-one on the game's own eight. Every header value,
every coverage and freshness figure, and every monthly reference factor is carried over
from the stock provider each one stands in for, so the developer's own balance across
the eight is preserved rather than replaced with a formula.

**Markets.** One `Kind global` desk per provider, named for the provider, in the stock
global-market shape: Global factor set, Core/Regional/Export zeroed, no home nation or
home region. Stock local and regional markets hand their home association a cheaper rate
and put its name on the shop front; with 24 associations that is 24 storefronts per
provider, so every desk sells to every club on the same terms.

**Tiers.** Several stock providers ladder by selection count — RegionScope One / Three,
FutureXI Corridor 3 / 6 / 8, LowerLine Select 3 / 6 / 8. The game does not enforce
`Scope selections`: a buyer ticks as many competitions or associations as they like
whatever the file says, so those tiers were the same package at three prices. Each
ladder is rebuilt on `Fields` — which is what the game turns into its *Benefit* column —
plus age band, division range, market statuses and professional-only. Only the four
field combinations that appear in the stock files are used. Selective packages take the
stock `1 all` form with a bundle discount, as ClubWire does.

Earlier attempts in this version, all corrected: packages sold on `core regional export`
against desks that zeroed those three, which made HatchlingXI, DeepFlight and Crestwire
vanish entirely; then all four factors set on a global desk with all four relations,
which is not a stock shape and left no provider available at all; then selection ranges
like `1 4`, which the game does not cap.

### Name lists

`Nationalities.txt` still pointed all 40 entries at `names = Multiverse`, a shared pool
that was replaced by 48 per-nation lists back in 1.0 and is not in the package. Each
member association now names its own pair, and the sixteen inactive reference regions
borrow the pool of the nation they sit in.

---

## 0.1

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
spread evenly. Each cup's draw was pulled back to the week before its new opening night.
Two-legged rounds keep both legs a fortnight apart, and nothing runs past week 41, which keeps every domestic final clear of the MSC finals in weeks 42 to
45 and of the finale window in 50 to 52. Deliberately short competitions such as the
Castolo Supercopa keep their own tight dates.

### Season-one hardening

Both curtain-raisers — the **Vyktoria Charity Shield** and the **Supercopa Unida** —
opened in week 2 against a cup holder whose final is not played until week 41, so in
the first season of a career there was nothing to put in the slot. They now draw in
week 3 and play from week 4, and conditional entries back up every cup-winner place,
so the field fills from the league when no holder exists yet.

Domestic cups now open in week 4 rather than week 3, which puts every cup draw in week
3 instead of week 2.

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

## 0.0 — initial standalone-world release

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
