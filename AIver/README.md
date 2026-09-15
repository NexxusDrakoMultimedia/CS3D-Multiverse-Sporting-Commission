# Multiverse Sporting Commission

A standalone football world for **Championship Soccer**.

24 member associations, 2,144 clubs, 130 divisions, four blocs, and a competition
calendar that runs from a 2,144-club Coronation down to a single match for everything in
week 52.

**Created by Nexxus Drako, with Claude's assistance.**
Version 1.1 · Every club, nation and competition is fictional.

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
start year suggests 2030 and can be changed there.

---

## What's inside

```
Package.ini                    world name, author, version
README.md                      this file
Data\
  StartYear.txt                2030
  Nationalities.txt            country identities, aliases, region taxonomy
  League\                      24 nation files + International teams and tournaments.txt
  ScoutingProvider\            eight scouting providers
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

Every nation has at least one cup, and the rules deliberately differ. The Itavrnai
Wyrmfire Cup takes all 256 clubs. New Bradman, the Galatyan four and Jarokn stagger entry
by rank. Determi mourns every round twice and settles only the Final Rite in one night.
Nexxie plays single matches and hands out rosettes. Ryukawa's Sakura Shield and Layn's
Wyred's Root Access Cup open with group stages. Castolo squeezes a four-team Supercopa
into two match days. Vyktoria opens its cup to amateurs from round one and adds a Charity
Shield.

### Club

| Competition | Field | Decided |
|---|---|---|
| MSC Cup Winners Cup | 32 — all 27 domestic trophies | wk 42 |
| MSC Conference Trophy | 48 — 16 dropping from the Challengers, 32 smaller associations | wk 43 |
| MSC Challengers League | 48 — 16 dropping from the Champions Cup, 32 from the leagues | wk 43 |
| MSC Champions Cup | 48 — 16 seeded, 32 through qualifying | wk 43 |
| MSC Super Cup | the four holders in one group | wks 46–48 |
| MSC Coronation Qualifiers | nine, entering all 2,144 clubs | wks 2–8 |
| **MSC Coronation Tournament** | the 142 who came through | wk 50 |
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
larger than 256, between them enter all 2,144; each halves down to its last sixteen, and
the 142 survivors contest the Coronation itself — a preliminary trims the field to 128,
then seven rounds to the final. Nothing is seeded past the preliminary.

Weeks 50 to 52 are reserved for the finale: the Coronation Final alone in week 50, no
club football at all in week 51, and the Ultimate Championship alone in week 52.

### National teams

| Competition | Field | Cycle | Weeks |
|---|---|---|---|
| MSC World Cup | all 24, eight groups of three | every 4 years | 48–52 |
| MSC Nations League | all 24, four groups of six | odd years | 10–51 |
| **Nexxus Drako Shield** | Itavrnai Union and Commonwealth together, six nations | every 4 years | 6–20 |
| Cyberya Championship | its four | every 4 years | 6–16 |
| Galatyan Championship | its four | every 4 years | 6–16 |
| MSC Associates Trophy | the unregioned ten | every 4 years | 6–32 |
| Friendly windows × 3 | everyone | yearly | 8, 24, 44 |

Every nation has exactly one bloc-level championship, and the four cover all 24 with no
overlap. The **Nexxus Drako Shield** is the bloc championship for the Itavrnai Union
*and* the New Bradmanian Commonwealth, contested together — neither holds one of its own.

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
