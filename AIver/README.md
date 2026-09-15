# Multiverse Sporting Commission

A standalone football world for **Championship Soccer**.

24 member associations, 2,144 clubs, 130 divisions, four blocs, and a competition
calendar that runs from a 2,144-club Coronation down to a single match for everything in
week 52.

**Created by Nexxus Drako, with Claude's assistance.**
Version 1.0 · Every club, nation and competition is fictional.

---

## Install

**Step 1 — the world.** Put the `Multiverse Sporting Commission` folder (or its zip)
into:

```
Documents\My Games\Championship Soccer\DataSets\
```

**Step 2 — the names. Don't skip this one.** Copy the 48 files from `Data\Names\` into
the *shared* folder:

```
Documents\My Games\Championship Soccer\Data\Names\
```

> Name lists inside a package are **not** read at runtime — the game loads them only
> from the shared `Data\Names` folder. Skip this step and the player-name pool comes up
> empty, which can make a career fail to save with *"Invalid or empty career second
> names"*. The copies inside the package exist purely for you to copy out.

**Step 3.** Start a new career, pick **Multiverse Sporting Commission** on the *Career
football world* screen, then choose countries and divisions on *Select Database*. The
start year suggests 2029 — that season runs into the 2030 World Cup — and can
be changed there.

---

## What's inside

```
Package.ini                    world name, author, version
README.md                      this file
Data\
  StartYear.txt                2029
  Nationalities.txt            country identities, aliases, region taxonomy
  League\                      24 nation files + International teams and tournaments.txt
  ScoutingProvider\            eight scouting providers, 23 packages
  Team\                        AFC Nexxus Drako
  Names\                       48 name lists - copy these out, see step 2
```

No `Team\` or `Player\` folders: clubs and squads are generated from each nation's name
lists, which is what keeps a 2,144-club world under 400 KB.

---

## The Commission

Fourteen regions in four blocs, plus ten unregioned nations.

| Bloc | Members |
|---|---|
| Itavrnai Union | Itavrnai Union, Vyktoria, New Rythorn |
| New Bradmanian Commonwealth | New Bradman, Ryukawa, Castolo and Minanda |
| Cyberya | Layn's Wyred, Determi, Nexxie, Jarokn |
| Galatyan | Mancunya, Centralya, Wyrmwoode, Esmeraldys |
| Unregioned | Veslavia, Valcarena, Tianlu, Akwanta, Sindhara, Hanseong, Mazamba, Qamaria, Selanting, Norvalia |

| Nation | Tiers | Clubs | Rep | Flavour |
|---|---|---|---|---|
| Itavrnai Union | 12 | 256 | 19 | draconic |
| New Bradman | 8 | 128 | 17 | British |
| Vyktoria | 8 | 128 | 16 | British |
| Mancunya | 8 | 128 | 16 | Northern English |
| Wyrmwoode | 8 | 128 | 16 | Welsh |
| Ryukawa | 4 | 64 | 15 | Japanese |
| Layn's Wyred | 4 | 64 | 15 | cyberpunk |
| Determi | 4 | 64 | 15 | gothic |
| Nexxie | 4 | 64 | 15 | cutesy |
| Jarokn | 4 | 64 | 15 | mythical |
| New Rythorn | 8 | 128 | 14 | Nordic |
| Centralya | 8 | 128 | 14 | Scots |
| Esmeraldys | 8 | 128 | 14 | Gaelic |
| Castolo and Minanda | 2 | 32 | 13 | Iberian |
| Veslavia | 4 | 64 | 12 | Slavic |
| Valcarena | 4 | 64 | 12 | Latin American |
| Tianlu | 4 | 64 | 12 | Chinese |
| Akwanta | 4 | 64 | 11 | West African |
| Sindhara | 4 | 64 | 11 | Indian subcontinental |
| Hanseong | 4 | 64 | 11 | Korean |
| Mazamba | 4 | 64 | 11 | Southern African |
| Qamaria | 4 | 64 | 10 | Middle Eastern |
| Selanting | 4 | 64 | 10 | South East Asian |
| Norvalia | 4 | 64 | 10 | North American |

Each pyramid keeps its named top flight and counts from one below it — New Bradman
Premier League then First to Seventh Division, Rythorn Överliga then Division Ett to Sju,
Wyrmwoode Uwch Gynghrair then Cynghrair Un to Saith. Cyberya is the exception and keeps
thematic names throughout: Wyred Mainline down to Darknet, Determi's High Requiem and
Pauper's Tier, Nexxie's Super Sparkle League, Jarokn's Pantheon.

Promotion and relegation chain correctly everywhere: each tier's relegation count equals
the promotion count of the tier below, so division sizes never drift.

**Vyktoria and New Bradman** reproduce their NationStates league threads exactly down to
tier four, club for club and in thread order. Vyktoria's ten original amateur clubs stay
together at the foot of the pyramid in V-League Eight.

---

## Competitions

### Domestic

Every association runs the same five competitions, named in its own register:

| | Field |
|---|---|
| **National Cup** | every club in the pyramid — the association's entry to the MSC Cup Winners Cup |
| **League Cup** | the top band of tiers |
| **Semi-Pro Cup** | the middle band — eight- and twelve-tier pyramids only |
| **Amateur Cup** | the bottom band — four- and twelve-tier pyramids only |
| **Super Cup** | National Cup holders against the champions, one match, week two |

Which band cups an association gets depends on how deep its pyramid runs. Four tiers is
a professional half and an amateur half with no middle, so those associations have no
Semi-Pro Cup. Eight tiers bottoms out at semi-professional, so those have no Amateur Cup.
Only the twelve-tier Itavrnai pyramid is deep enough for all three. Castolo and Minanda,
at two tiers, has a League Cup and nothing below it.

| Pyramid | Competitions |
|---|---|
| 12 tiers | National, League (1–4), Semi-Pro (5–8), Amateur (9–12), Super |
| 8 tiers | National, League (1–4), Semi-Pro (5–8), Super |
| 4 tiers | National, League (1–2), Amateur (3–4), Super |
| 2 tiers | National, League (1–2), Super |

The band cups enter by division rather than by country, so each takes exactly the tiers
it is named for and no club can be in two of them.

The **Super Cup** seats the National Cup holders against the champions. If one club won
both — and cannot play itself — the league runners-up take the second seat.

Names are local throughout: Itavrnai's Wyrmfire Cup, Drakonhold League Cup, Emberforge
Trophy, Hatchling Vase and Wyrmcrown Shield; Wyrmwoode's Cwpan Wyrmwoode, Cwpan y
Cynghrair, Tlws yr Her, Cwpan yr Amaturiaid and Darian Wyrmwoode; Qamaria's Kas Qamaria,
Kas ad-Dawri, Kas al-Ittihad, Kas al-Hawa and Kas al-Abtal.

Within a nation each cup runs on its own lane of weeks, so two cups a club could enter
never fall on the same night. The Semi-Pro and Amateur Cups share a lane, since no club
is in both.

### Club

| Competition | Field | Decided |
|---|---|---|
| MSC Cup Winners Cup | 24 — every association's National Cup winner | wk 43 |
| MSC Conference Trophy | 48 — 16 dropping from the Challengers, 32 smaller associations | wk 43 |
| MSC Challengers League | 48 — 16 dropping from the Champions Cup, 32 from the leagues | wk 43 |
| MSC Champions Cup | 48 — 16 seeded, 32 through qualifying | wk 43 |
| MSC Super Cup | the four holders in a group, then a final | wks 47–50 |
| MSC Coronation Qualifiers | nine, entering all 2,144 clubs, one in sixteen | wks 2–8 |
| **MSC Coronation Tournament** | the 134 who came through | wk 45 |
| **MSC Ultimate Championship** | Coronation winner v Super Cup winner | **wk 52** |

**The cascade.** The three league competitions run as a chain, UEFA-style, and the
calendar enforces it:

| | Draw | Qualifying | Receives |
|---|---|---|---|
| Champions Cup | wk 1 | wks 3, 5 | — |
| Challengers League | wk 6 | wks 7, 9 | the 16 knocked out of Champions Cup qualifying |
| Conference Trophy | wk 10 | wks 11, 13 | the 16 knocked out of Challengers qualifying |

Each competition is drawn only after the one above has finished qualifying, so the
clubs dropping down are already known. They enter seeded, straight into the group
stage. The Conference's own 32 qualifiers come entirely from the smaller associations,
so the third tier is theirs plus whoever falls out of the second.

Only qualifying is staggered. Once the groups begin no club is in more than one of
the three, so they share a calendar from there: group stage in weeks 15 to 25, round
of 16 in 28 and 30, quarter finals 32 and 34, semi finals 37 and 39, and all three
finals on the same night in week 43.

**The off-weeks.** The Cup Winners Cup and the Coronation both draw on clubs already
committed elsewhere, so neither is ever played on a night the big three are using.
The Cup Winners Cup takes weeks 16, 22, 27, 29, 31, 33, 36 and 38, with its final in
42; the Coronation takes 10, 12, 14, 20, 26, 35 and 40 before its own final in 50.

**The Coronation** gives every club in the Commission a road in. Nine qualifiers, none
larger than 256, between them enter all 2,144 at the same rate — one club in sixteen,
over four rounds — which brings 134 through. The Coronation trims the odd twelve in a
Preliminary Round and then counts from scratch: First Round of 128, Second, Third,
Fourth, Quarter Finals, Semi Finals, Coronation Final. Nothing is seeded past the
Preliminary.

**Domestic cups.** Every association has a Super Cup — champions against cup holders in
week two. Any pyramid of eight tiers or more also has a League Cup for its top four
divisions and a Semi-Pro Trophy for tiers five to eight, and the twelve-tier Itavrnai
pyramid adds an Amateur Vase below that. Tier cups enter by division, so each takes
exactly the band it is named for. Within a nation every cup runs on its own lane of
weeks, so two cups a club could be in never share a night.

**AFC Nexxus Drako** plays in the Itavrnai twelfth flight: reputation nil, twenty-five
players none over 20, ability in the fifties and sixties against potential in the
two-tens and twenties. Claret and gold. It has its own `Data\Team` file.

**One naming rule everywhere.** Every knockout round in the world is a **Round of N**,
a **Quarter Final**, a **Semi Final** or a **Final**. Where a field is not a power of
two, the opening round is a **Preliminary Round** that seeds the surplus out and lands
exactly on one — the Coronation's 134 down to 128, the Itavrnai Hatchling Vase's 96 down
to 64. Quarter Final, Semi Final and Final are only used where a competition plays to a
single winner, so the Coronation qualifiers — which stop early and send several through
— name their rounds for the field they start with throughout.

**Every seat belongs to someone.** Where a competition inherits named clubs, each seat
is written on its own incrementing threshold with its own fallback behind it, the way
the stock European Cup does — an association's cup winner, and that same association's
league if the cup went uncontested. A gap is never filled by whichever entry happens to
sit first in the list.

**The Cup Winners Cup** takes the main domestic trophy of each of the 24 associations
and nothing else — the Itavrnai Grand Conclave, the New Bradman League Cup and the
Ryukawa Sakura Shield are still played but no longer qualify, and nor do the two
curtain-raisers. The eight best-ranked holders go straight to the round of 16 and the
other sixteen contest a preliminary, so eight winners join eight byes.

**When one club wins two things.** The Super Cup seats the four continental holders,
but the Cup Winners Cup does not exclude the other three, so a club can arrive with two
trophies and leave a seat empty; beaten finalists fill any gap. The same goes one round
later — the Coronation winner may also have topped the Super Cup group, and cannot play
itself, so the Super Cup runner-up steps up to contest the Ultimate Championship.

Weeks 44 to 52 are the finale: the Coronation Final alone in week 50, no
club football at all in week 51, and the Ultimate Championship alone in week 52.

### National teams

| Competition | Field | Cycle | Weeks |
|---|---|---|---|
| MSC World Cup | all 24, four groups of six, top four through | every 4 years from 2002 | 47–51 |
| MSC Nations League | all 24, four groups of six | odd years from 2003 | 10–51 |
| **Nexxus Drako Shield** | Itavrnai Union and Commonwealth together, six nations | every 4 years from 2004 | 6–20 |
| Cyberya Championship | its four | every 4 years from 2004 | 6–16 |
| Galatyan Championship | its four | every 4 years from 2004 | 6–16 |
| MSC Associates Trophy | the unregioned ten | every 4 years from 2004 | 6–32 |
| Friendly windows × 3 | everyone | yearly | 8, 24, 44 |

The three cycles interlock, so no two of them ever share a year — the World Cup from
2002 on a four-year offset, the Nations League from 2003 on a two-year one, and the
bloc championships from 2004 on a four-year one, midway between World Cups:

| 2030 | 2031 | 2032 | 2033 | 2034 |
|---|---|---|---|---|
| World Cup | Nations League | bloc championships | Nations League | World Cup |

The suggested start year of 2030 is therefore a World Cup season. Friendly windows run
every year regardless.

Every nation has exactly one bloc-level championship, and the four cover all 24 with no
overlap. The **Nexxus Drako Shield** is the bloc championship for the Itavrnai Union
*and* the New Bradmanian Commonwealth, contested together — neither holds one of its own.

---

## Scouting

Eight providers and 23 packages, modelled one-for-one on the game's own eight
scouting providers. Every header value — price drift, offer chance and kinds,
discounts, rotating slots, small-club terms — and every coverage and freshness figure
is carried over from the stock provider each one stands in for, and so is every price.

Three things are changed, and only three:

**The markets.** One `Kind global` desk per provider, named for the provider, in the
stock global-market shape — Global price factor set, Core/Regional/Export zeroed, no
home nation and no home region. The stock local and regional markets give their home
association a cheaper rate than everyone else and put its name on the shop front; with
24 member associations that would mean 24 storefronts per provider, so every desk here
sells to every member club on the same terms.

**The tiers.** Several stock providers build their ladder out of selection counts —
RegionScope One / Three, FutureXI Corridor 3 / 6 / 8, LowerLine Select 3 / 6 / 8. The
game does not enforce `Scope selections`, so those tiers are all the same package at
different prices. Each ladder is rebuilt out of what a package actually tells you,
which is what the game shows in its *Benefit* column:

| Fields | Reads in game as |
|---|---|
| `identity sporting` | Player search + skill profile |
| `identity sporting development` | + potential |
| `identity market-contract` | Player search + market and contract |
| `identity sporting development market-contract` | + skills + potential + market |

Age band, division range, market statuses and professional-only carry the rest —
HatchlingXI steps u21 → u23, DeepFlight steps second-tier-down → ninth-tier-down,
LedgerPulse steps free agents → listed → everyone.

**The names.** MSC ones, with no association named anywhere.

| Provider | Stands in for | What it sells |
|---|---|---|
| Commission Registry | LeagueBase | The Commission's own club register. |
| CharterScope | RegionScope | A catalogue pointed at the competitions you scout. |
| MultiversePro | WorldPro | The expensive one. Top flights first. |
| HatchlingXI | FutureXI | Academies and reserve sides, nobody over 23. |
| LedgerPulse | MarketPulse | Contracts, wages and expiries. |
| DeepFlight | LowerLine | Below the top flight, down to the ninth tier. |
| Crestwire | ClubWire | Stringers filing from press boxes. |
| Frontier Relay | Touchline Relay | Slow, cheap, and two of four rotate each season. |

---

## Names

Each nation reads its own pair of lists, 420 given names and 900 surnames, about 29,500
names across 48 files. Nineteen nations draw on a real name-frequency corpus covering
around a hundred countries, filtered per nation and restricted to entries that survive a
Windows-1252 round trip; male and female given names are both included. Welsh and Scots
are curated by hand and extended along authentic patterns — `ap`/`ab` patronymics,
`Mac`/`Mc` stems — because the corpus only knows "GB". The five invented nations are
generated from syllable sets in their own register.

Within the Itavrnai Union, Galatyan and Commonwealth blocs, each nation keeps its own
register as 70% of its lists and takes the rest from its neighbours. Cyberya and the
unregioned ten stay pure.

---

## Notes and known limits

**Encoding.** Every data file is ANSI (Windows-1252), matching the stock data, so
accented names load correctly rather than as mojibake. League, Nationalities and provider
files use CRLF; the name lists use bare LF with no trailing newline. Don't re-save any of
them as UTF-8. This README is the exception — it is UTF-8, being documentation rather
than game data.

**Two undocumented engine limits** shaped this world. A pyramid cannot exceed **12
tiers**, which is why the Itavrnai Union runs 12 flights of 18, 22 and 24 clubs rather
than 16 of 16. A competition cannot exceed **256 teams**, which is why the Coronation is
nine qualifiers feeding a final rather than one 2,144-club bracket. Neither limit appears
in the manual.

**Comment character.** These files use `#`, matching the game's own shipped data. The
manual specifies `;`. Every comment sits on its own line and never trails a value, so if
a future build enforces the manual it is a find-and-replace.

**No team or player files.** Clubs and squads are generated. Add `Data\Team\<Club>.txt`
files if you want fixed kits, reputations or squads for particular clubs.

---

## Credits

Built by **Nexxus Drako**, with Claude's assistance.

Vyktoria and New Bradman are drawn from their NationStates league threads. Everything
else — the other 22 nations, the blocs, the competitions and the name lists — is original
to this world.
