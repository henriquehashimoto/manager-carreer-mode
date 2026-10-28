# EA SPORTS FC 27 — Tactical & Systems Reference

**Project:** The Hammers Rebuild — West Ham United Career
**Purpose:** Standing reference for formations, player roles, custom tactics, and the Career Mode systems that affect player evaluation and squad building.
**Created:** 28 October 2026
**Game context at time of writing:** FC 27, Season 2 ("FC Heritage"), Title Update 1.1.0 live (27 Oct), Title Update 1.2.0 announced for mid-November.
**Companion document:** `AGENTS.md` (governing charter — this file supports it, it does not override it).

---

## 0. How to use this file

### Evidence tiers

Every claim in this file is labelled. Do not upgrade a claim's status without new evidence.

| Tier | Meaning | Examples used here |
|---|---|---|
| **[EA]** | Stated by EA in official Pitch Notes, Deep Dives, or Developer Notes | Team Press behaviour, Dynamic OVR pillars, injury rework |
| **[DATA]** | Community tracking of real squads/usage | Formation usage %, most-used roles per position |
| **[CONSENSUS]** | Community/pro editorial agreement, testable in-game | "4-2-1-3 launch meta", tactical slider values |
| **[UNVERIFIED]** | Circulated broadly but with no primary source | Numeric Role+/Role++ effects |

### The single rule for this file

**Nothing in here is a fact about *this save*.** It describes the game. What West Ham's actual players, ratings, role familiarity, budget and results are — that comes only from the save. See Section 8 for the checklist of what must be confirmed rather than assumed.

### Status of the tactical consensus

Almost all formation/role consensus below is derived from **Ultimate Team and Rivals (PvP) data**. The *mechanics* transfer directly to Career Mode vs CPU. The *recommended shapes* do not transfer automatically — a Championship side dominating possession against a deep AI block is a different problem from winning central scrambles against a human. Treat shape recommendations as hypotheses to test, not instructions.

---

## 1. The design thesis: FC 27 removes automation

FC 27 is built around **"greater gameplay control" and "less automation"** — the framing used by Gilliard Lopes, Principal Gameplay Designer **[EA]**. Nearly every tactical consequence in this document follows from that one decision.

The practical read:

- The game now rewards **what you do manually** and penalises **what you used to let the AI do**.
- Routes to goal that were previously automated (cross → header) became more expensive in input.
- Routes that were always manual (short central combinations, jockeying, timed runs) became relatively stronger.
- Formation and role choice therefore matters *less* than execution — but Role Familiarity matters *more*, because it governs how urgently players carry out the instructions you give them.

---

## 2. Core mechanics that shape every tactic

| Change | EA's wording **[EA]** | Tactical consequence |
|---|---|---|
| Team Press in own third | *"Team Press will now have no effect while the ball is in your defensive third."* | Pressing from your own box is a dead button. You need passive midfield cover, not pressure from centre-backs. |
| Manual defending | Defenders *"rely more on their positioning and support the play until you take control and choose when to make a tackle."* Manual jockey speed and stand-tackle range increased; AI interception reach reduced. | The player you control decides more interceptions. Holding contain and hoping is now actively bad. |
| Through passes | *"Ground and lobbed through passes no longer heavily assist you by steering toward open lanes away from your aim."* | Passes follow your aim strictly. Long diagonals into wide channels punish sloppy input. |
| Crossing | *"Crosses will now be delivered into space more often rather than directly onto a specific player"* — and *"it can miss everyone if it isn't placed with precision."* | Aim and power decide the outcome. The old wing-cross-header route is less reliable. |
| Headers | *"Connecting with a header from crosses and corners requires greater precision, making clean headers less frequent."* | Set-piece and crossing output should not be modelled as a repeatable supply line. |
| Triggered runs | *"Manually triggered runs only continue for a limited distance"*; they continue only *"if you keep playing within the range of the running player."* | Overlapping runs **expire**. Re-trigger constantly. This is the #1 wide-play error. |
| AcceleRATE | *"Slightly reduced the impact of AcceleRATE profiles on a player's running performance, bringing Explosive, Controlled, and Lengthy players a little closer together"* — with *"greater emphasis on a player's Acceleration and Sprint Speed Attributes."* | Raw Acceleration/Sprint Speed outweighs profile type. "Lengthy" is no longer a cheat code. |
| PlayStyles | Ten PlayStyles rebalanced. Finesse Shot *"updated to make player attributes play a bigger role in shot outcome."* Low Driven lost its shot-speed boost. | PlayStyles do less heavy lifting; base attributes do more. Judge players on attributes, not badges. |
| Attacking Spatial Awareness (new) | Roles *"can sometimes feel too strict"*; players *"will be better able to take advantage of the space in front of them, rather than always sticking to their positions and Roles."* | Attacking movement is less role-locked than FC 26. Roles are **less** decisive this year, not more. |

### Why narrow shapes got cheaper

Three of the above stack to tax width specifically:

1. Crossing yields space, not targets, and headers need precision.
2. Triggered runs expire, so width costs continuous input.
3. Through passes follow aim, so hitting a wide channel is less forgiving.

Meanwhile central combinations were untouched, and you can only manually defend one player at a time — so six central bodies always leave someone unmarked by you. That is the mechanism behind the narrow-meta complaint. It is a cost-shift, not a nerf to wingers as a category.

---

## 3. Formations

### 3.1 Usage data **[DATA — fut.gg community squads, Oct 2026]**

| Formation | Community | Pros | Default build-up / line |
|---|---:|---:|---|
| **4-2-1-3** | 25% (#1) | 16% | Balanced / Balanced (~60) |
| **4-3-1-2** | 24% (#2) | **30% (#1 pros)** | Balanced / Balanced |
| 4-4-1-1 | 14% (#3) | 10% | Balanced / Balanced |
| 4-1-2-1-2 Narrow | 9% (#4) | 12% | Balanced / Balanced |
| 4-3-3 Attack | 6% | 1% | Short Passing / Balanced |
| 4-3-3 Holding | 5% | 5% | Balanced / Balanced |
| 4-2-3-1 Wide | 4% | 4% | Balanced / Balanced |
| 4-4-2 | 4% | 11% | Balanced / Balanced |
| Everything else | <3% each | <3% | — |

**Critical caveat [EA]:** EA states formation win rates are *"evenly distributed with minimal variance"* and that *"a wider number of different tactical set ups"* are being used than in FC 26. EA publishes **no** win-rate table. **Popularity is not proof of superiority.** Do not build this project's identity around copying a meta shape.

### 3.2 The three shapes with real consensus behind them **[CONSENSUS]**

#### 4-2-1-3 — the two-CDM counter shape
- **Why it works:** two CDMs cover the space Team Press no longer contests; wide Inside Forwards get automatic cuts into the box; Shadow Striker CAM acts as a third-man runner without needing threaded through balls; single Advanced Forward punishes space behind a high line.
- **Most-used roles:** GK Goalkeeper/Defend · LB/RB Fullback/Defend · CB×2 Defender/Defend · CDM Deep-Lying Playmaker/Build-Up ×2 · CAM Playmaker/Balanced (50%) or Shadow Striker/Attack (40%) · LW/RW Inside Forward/Balanced · ST Advanced Forward/Attack.
- **Community slider values:** Balanced defensive style, Defensive Width ~48, Depth 50–55, **Counter** build-up, **Forward Runs** chance creation, Offensive Width ~55, Players in Box 4.
- **Weakness:** can be passive in possession; a single striker can be isolated if the CAM is marked out of the game.

#### 4-3-1-2 — the central-overload shape
- **Why it works:** six central players against a game where you can only manually defend one at a time. Short central combinations are the least punished passing route in FC 27.
- **Requires:** full-backs for all width (and therefore re-triggered runs every time), and a genuinely creative CAM — everything funnels through him.
- **Weakness:** no natural wide cover; vulnerable to the channel between centre-back and full-back; narrow-vs-narrow becomes a midfield pile-up with high variance.

#### 4-4-1-1 — the balanced shape
- **Why it works:** no structural hole. Two banks of four with a support striker; can be tuned from control to counter without changing shape.
- **Most-used roles:** GK Sweeper Keeper/Balanced or Goalkeeper/Defend · Fullbacks Fullback/Balanced · CB×2 Defender/Defend · CM Holding/Defend + Box-to-Box/Balanced ×2 (or Deep-Lying Playmaker/Build-Up ×2) · CAM Playmaker/Balanced · LM/RM Inside Forward/Balanced · ST False 9/Attack or Advanced Forward/Attack.
- **Weakness:** no area of overwhelming strength; can be overrun centrally by a 4-3-1-2 that gets six bodies into the middle.

### 3.3 Strong alternative

**4-2-3-1 Wide [CONSENSUS]** — second pick when there is no natural Shadow Striker or when the AMs are the squad's strongest area. Three attacking midfielders give more crossing coverage across the pitch; two CDMs still solve the Team Press gap. Reference values: Balanced / Width 50 / Depth 42 / **Direct Passing** / Offensive Width 58 / Players in Box 4.

### 3.4 Shapes the consensus advises against

| Shape | Reason |
|---|---|
| Flat 4-4-2 | No natural holding midfielder; two strikers draw the team forward and expose the centre. |
| High-press 4-3-3 Attack | Three CMs pressing into no-man's land once Team Press dies in your own third. |
| 5-2-1-2 / 5-3-2 | Wing-backs now depend on manual overlap timing; pulling them forward leaves a three-back exposed. |
| 3-4-3 diamond | No CDMs in a reduced-AI-defending game; very high risk. |

### 3.5 The three-slot preset habit **[CONSENSUS]**

FC 27 lets you store multiple tactic presets. A practical default:

| Slot | Purpose | Shape adjustments |
|---|---|---|
| 1 — Default | Balanced control | Chosen base shape |
| 2 — Protect a lead | Kill the game | Same shape, Low Block, Depth ~35, Offensive Width ~45 |
| 3 — Chase a goal | Force the issue | Wider shape or extra forward, Players in Box 6 |

Switching during a stoppage and switching back before kick-off is a legitimate habit, and more valuable in FC 27 because the game rewards shape discipline over AI auto-defence.

---

## 4. Custom tactics parameter map

### 4.1 Naming trap
The Edit Tactic menu calls the setting **Defensive Approach** (Deep / Balanced / High), while EA's Pitch Notes call the underlying behaviour **Defensive Depth**. They are the same thing. Most conflicting advice online comes from this label mismatch.

### 4.2 Parameters

| Phase | Parameter | Range / options | What it controls |
|---|---|---|---|
| Defensive | Defensive Approach / Depth | Deep → Balanced → High, plus numeric depth | How high the line sits, how early defenders retreat |
| Defensive | Defensive Width | numeric | Compactness across the pitch |
| Transition | Build-Up Style | Balanced / Short Passing / Counter / Fast Build-Up | How the team starts attacks |
| Attacking | Chance Creation | Forward Runs / Direct Passing / etc. | How the team creates openings |
| Attacking | Offensive Width | numeric | How wide the attack stretches |
| Attacking | Players in Box | numeric (commonly 3–6) | How many commit to the box |

### 4.3 Worked reference setups **[CONSENSUS — test before adopting]**

**4-2-1-3 (default control/counter)**
```
Defensive Approach: Balanced     Defensive Width: 48     Depth: 50–55
Build-Up: Counter                Chance Creation: Forward Runs
Offensive Width: 55              Players in Box: 4
GK Goalkeeper/Defend | LB Fullback/Defend | CB Defender/Defend | CB Defender/Defend | RB Fullback/Defend
CDM Deep-Lying Playmaker/Build-Up | CDM Holding/Defend
CAM Shadow Striker/Attack | LW Inside Forward/Attack | RW Inside Forward/Attack | ST Advanced Forward/Attack
```

**4-2-3-1 Wide (when the AMs are the strength)**
```
Defensive Approach: Balanced     Defensive Width: 50     Depth: 42
Build-Up: Balanced               Chance Creation: Direct Passing
Offensive Width: 58              Players in Box: 4
```

**4-3-3 Holding (only with one elite CDM + elite wide forwards)**
```
Defensive Approach: Balanced     Depth: 42
Build-Up: Fast Build-Up          Chance Creation: Forward Runs
Offensive Width: 62
```

> Risk noted in sources: a single Holding CM is exposed on turnovers. Only viable with full-backs who have high Defensive Awareness.

### 4.4 Tactic import codes
FC 27 supports importing a full custom tactic via an alphanumeric **code** (Community → Tactics → Import). Codes encode sliders and role defaults. They are a starting point, not an endorsement — always re-check role familiarity for your own players afterwards.

---

## 5. Player roles

### 5.1 What each layer does

| Layer | What it is |
|---|---|
| **Position** | Primary + up to six secondary positions. Playing in a secondary position carries **no penalty** **[EA]**; outside all of them triggers Out of Position. |
| **Role** | Off-ball tactical responsibility when you are not controlling the player: where they stand, when they track back, whether they hold width, whether they make runs. |
| **Focus** | Modifier on the role. Same role, materially different behaviour. |
| **Role Familiarity** | Per-player, per-role competence: **Base → Role+ → Role++**, plus the separate **Out of Position** state. |
| **Attributes / PlayStyles** | Do the work on individual actions. Roles shape positioning; they do not make a bad finisher score. |

**Key structural fact [DATA]:** role availability follows the **position**; familiarity follows the **player**. A player in a valid position can be assigned any role available there, but may be Base in one and Role++ in another.

**Count:** 37 position-role slots, ~30–31 distinct role names (seven roles appear at two positions), ~76 role+focus combinations. **EA has never published a role count.** No count is worth treating as permanent.

### 5.2 Full role list **[DATA — futbin / fut.gg]**

| Position | Roles (focuses) |
|---|---|
| **Goalkeeper** | Goalkeeper (Defend, Balanced) · Sweeper Keeper (Balanced, Build-Up) · Ball-Playing Keeper (Build-Up) |
| **Full-Back** | Fullback (Defend, Balanced, Versatile) · Falseback (Defend, Balanced) · Wingback (Balanced, Versatile) · Attacking Wingback (Support, Attack) · Inverted Wingback (Build-Up, Attack) |
| **Centre-Back** | Defender (Defend, Balanced) · Stopper (Balanced, Defend) · Ball-Playing Defender (Defend, Build-Up) · Wide Back (Defend, Aggressive, Support) |
| **CDM** | Holding (Defend, Roaming) · Centre-Half (Defend) · Deep-Lying Playmaker (Defend, Roaming) · Wide Half (Build-Up, Defend) · Box Crasher (Balanced) |
| **CM** | Box-to-Box (Balanced, Ball-Winning) · Holding (Defend) · Deep-Lying Playmaker (Defend) · Playmaker (Attack, Roaming) · Half-Winger (Support, Balanced, Attack) |
| **Wide Midfielder (LM/RM)** | Winger (Balanced, Attack, Versatile) · Wide Midfielder (Defend, Support, Build-Up) · Wide Playmaker (Attack) · Inside Forward (Balanced, Attack) |
| **Attacking Midfielder (CAM)** | Playmaker (Balanced, Roaming) · Shadow Striker (Attack) · Half-Winger (Roaming, Balanced, Attack) · Classic 10 (Versatile, Wide, Attack) |
| **Winger (LW/RW)** | Winger (Balanced, Attack, Versatile) · Inside Forward (Balanced, Attack, Roaming) · Wide Playmaker (Attack) |
| **Striker** | Advanced Forward (Attack, Versatile) · Poacher (Attack, Versatile) · False 9 (Build-Up, Attack) · Target Forward (Balanced, Attack, Wide) |

### 5.3 What familiarity actually does **[EA + UNVERIFIED]**

**What EA has confirmed [EA]:**

> "Player Roles continue to determine the types of runs a player can make based on their position and Role. Role Familiarity then influences the **urgency** with which a player makes those available runs. Players with greater familiarity in a Role, including Role+ and Role++, will show more urgency when making those movements."

**What nobody can confirm [UNVERIFIED]:** EA has **never published** a numeric effect for Role+ or Role++. There is **no EA Help article on Player Roles**. Any specific percentage ("+5% positioning") is invented. Community reports consistently say the effect is *noticeable on attackers and hard to feel on defenders* — which fits the mechanic, since attacking roles drive runs and runs are what you watch.

**Practical order of operations [CONSENSUS]:**
1. **Fix Out of Position first** — it is a real, EA-acknowledged penalty (simplified role + worse positioning). Free to fix, highest value.
2. **Pick the Focus before the Role** — most "my role is broken" complaints are a Focus problem (Defender/Defend vs Defender/Balanced step out differently).
3. **Refresh re-triggered runs** — an expired run looks identical to a role bug and isn't one.
4. **Don't chase familiarity on defenders** — lowest visible return.

### 5.4 Most-used role per position **[DATA — fut.gg]**

| Pos | Most-used role | Share |
|---|---|---:|
| GK | Goalkeeper / Defend | 62% |
| CB | Defender / Defend | 93% |
| RB | Fullback / Balanced | 47% |
| LB | Fullback / Balanced | 47% |
| CDM | Deep-Lying Playmaker / Build-Up | 43% |
| CM | Box-to-Box / Balanced | 37% |
| CAM | Shadow Striker / Attack | 51% |
| RM / LM | Inside Forward / Balanced | 65% / 68% |
| RW / LW | Inside Forward / Balanced | 66% / 66% |
| ST | Advanced Forward / Attack | 65% |

### 5.5 "New FC 27 roles" — the recurring error
**Wide Back, Inverted Wingback, Box Crasher, Ball-Playing Keeper and the Versatile focus all shipped in FC 26, not FC 27.** They are in FC 27 because they carried forward. FC 27's Pitch Notes announce **no new roles**. This matters for research quality: any guide claiming otherwise is not reliable on other points either.

---

## 6. Career Mode systems that change how players are evaluated

This section is the one that most affects this project's tracking, because it breaks the assumption that an OVR is a stable fact.

### 6.1 Dynamic OVR **[EA]**
Overall Rating now **rises and falls during the season**, driven by three pillars:

| Pillar | Behaviour |
|---|---|
| **Form** | No longer a fixed boost. Form works toward a target Dynamic OVR based on current form level and long-term potential outlook. Young players with room to grow can spike harder than veterans near their ceiling. Form boosts are applied to the attributes that matter for the player's position, not spread generically. |
| **Morale** | Now directly influences Dynamic OVR. Playing time, squad roles and expectations all feed it. Volatility increased — nobody stays emotionally static across a 60-match season. |
| **Match Fitness** | New Peak-to-Unfit state representing readiness at kick-off. Combines Energy Level and injury status. **Penalises rather than boosts** — it must be actively maintained through rotation and recovery. |

**Direct consequence for this project:** an OVR screenshot is only valid for the date it was taken. Every rating recorded must carry a date and, where visible, the Form/Morale/Fitness state behind it. Comparing an October OVR to a February OVR without that context produces false conclusions.

### 6.2 Training Plans removed
The Training Plan feature is gone, except **Energy Recovery**. Development is now influenced by Dynamic OVR and performance, not by a training assignment. Any development plan in this project's player cards must therefore be phrased in terms of **minutes, role, form and coaching**, not "set training to X".

### 6.3 Growth Profiles **[EA]**
Six distinct profiles govern how attributes evolve, when a player peaks, and how they decline. Some peak young, some improve into their late twenties, some sustain, some fade early. **Potential is a curve, not a number.**

### 6.4 Dynamic Potential **[EA]**
Consistently exceeding expectations can **raise a player's ceiling**; prolonged poor form can stall development. Also applies to AI teams in Deeper Simulation leagues. Performance and progression are now causally linked — which makes this project's emphasis on performance-based evaluation correct by design.

### 6.5 Positions
Up to **seven positions** per player, with **no penalty in any secondary position**. Baseline OVR is determined per position, and Form/Morale boosts apply to the secondary-position baseline when played there. This makes position conversion a legitimate, low-cost squad-building tool.

### 6.6 Squad Ranks **[EA]**
A new evaluation system predicting a player's impact in your squad, with accuracy set by staff knowledge (coaches for your players, scouts for others). Useful as a cross-check against raw OVR and against our own performance analysis.

### 6.7 Coaches **[EA]**
Coaches **no longer improve attributes**. Their job is to **assess and project potential**. Higher-quality coaches are more likely to identify a player's true ceiling; lower-quality coaches may **underestimate** it. 12 coaches, split across Goalkeeping / Defence / Midfield / Attack, with a Head Coach per department.

**Implication:** a scout or coach report may understate a player's ceiling. "No further growth" is a staff opinion, not a fact.

### 6.8 Scouting — four stages **[EA]**

| Stage | Focus |
|---|---|
| **Tactical Fit** | Performance and match ability |
| **Future** | Potential and growth |
| **Financial Assessment** | Player's interest, and the cost of supporting the move |
| **Status** | Player happiness and likelihood of interest in a move |

Attributes are now revealed instantly; the four stages add interpretation rather than progressively uncovering raw numbers. **Form and Morale are part of a scout report** — a struggling player may be undervalued relative to long-term quality, and a hot player may command a premium.

### 6.9 Transfers and contracts **[EA]**

| System | Behaviour that matters to us |
|---|---|
| **TransferRoom xTV** | Valuations evolve across a career and respond to form and league strength. Market value **moves** — a good season raises it, a bad one lowers it. |
| **Transfer stages** | Enquiry → permission → parallel club/player negotiation → possible renegotiation if a rival enters. Deals can be hijacked or revived. |
| **Deal structure** | Instalments, achievement bonuses, player exchanges, loan-backs, buyback / first-refusal / sell-on clauses. |
| **Contract terms** | Wages, length, sign-on, agent fees, **squad role promises**, performance bonuses (appearances/goals/assists/clean sheets), **automatic wage rises on promotion or European qualification**, automatic reductions after setbacks, release clauses. |
| **Squad role consequences** | Promised playing time that isn't delivered **has consequences** — this is what feeds Morale and therefore Dynamic OVR. |
| **AI club relationships** | Fierce rivals and local derbies are far less likely to do business; multi-club ownership networks are more likely. Relevant to any London-club target. |
| **Player interest** | Driven by relative stature, destination league, the player's OVR, career stage, current wages, contract length, continental competition, and **returning home**. |
| **AI recruitment** | AI clubs now use league statistics (goals, assists, ratings, clean sheets) and manager tactical fit when identifying targets. Standout performers attract bids. |
| **Deadline Day** | Expanded to 20 hours, with 1-hour and 2-hour advance options. |

### 6.10 Injuries **[EA]**
Injury frequency increased on Authentic. **Light injuries can persist beyond matchday and become part of Match Fitness management** — you may play through them, at the risk of aggravation and a more severe setback. Medium and severe injuries have recovery periods that can return a player *before* they are fully clear of risk. Injuries also affect Form and Morale.

**Implication:** "available" is no longer binary. Player cards should record fitness state, not just injured/not-injured.

### 6.11 Unexpected Events and press conferences **[EA]**
Expanded to include sudden injuries, **points deductions for financial mismanagement**, internal conflicts, and disciplinary issues. Events chain: one decision triggers the next stage. Press conferences are less frequent but higher-stakes, and typically offer **two options with no correct answer** — one may strengthen the group at the cost of an individual, or empower a player while creating friction.

**Implication:** a points deduction or dressing-room event is a legitimate, in-game narrative event for this project. It must be recorded as fact when it happens, and it has sporting consequences.

---

## 7. Application to this project

### 7.1 Tactical identity, made auditable
The Season 1 charter requires "establish a preferred formation and tactical identity by December." This document lets that be measured rather than asserted:

| Metric | How to record it |
|---|---|
| Chosen base shape | Formation name |
| Full role/focus assignment | All 11 slots, written down |
| Familiarity coverage | Count of starters at Base / Role+ / Role++ |
| Out of Position count | Number of starters carrying the penalty |
| Preset discipline | Whether the three-slot Default / Protect / Chase habit is in use |
| Results by shape | Points and goals for/against per shape, once enough matches exist |

### 7.2 Role Familiarity as a transfer filter
Under the five-signing cap in `AGENTS.md` §4, every permanent signing must earn its slot. Role Familiarity adds a legitimate sporting criterion:

- A player who is **Role++ in the exact role we need** is worth more than a higher-OVR player who arrives at Base familiarity — particularly at full-back and in central midfield, where FC 27's AI does less for you.
- This must be checked as part of the sporting-justification test in §4.3, not used as a substitute for it.
- It is **not** grounds for a signing on its own. "Great tactical fit, no sporting need" fails the policy exactly as "high overall, no sporting need" does.

### 7.3 Shape hypotheses to test for a Championship side
Unverified — these are the questions to answer in pre-season friendlies, not conclusions:

1. **Does a two-CDM shape starve the team of possession against a deep AI block?** If West Ham are the strongest side in the division, `Counter` build-up may be the wrong default.
2. **Is 4-4-1-1 the better control base, with 4-2-1-3 as the away/counter preset?** The balanced shape's weakness (no overwhelming strength) is less damaging when the squad is better than the opposition.
3. **How much width is actually needed to break a Championship low block?** Given crossing nerfs, the answer may be "width to stretch, then central penetration" rather than a crossing game.
4. **Does a Target Forward make sense in a division full of physical centre-backs** — or is the header nerf enough to rule it out as a primary outlet?

Answers should be recorded with actual friendly results. Do not adopt a shape because it is the Rivals meta.

### 7.4 What this does *not* license
Nothing in this file justifies:
- A signing outside the five-permanent-signing cap.
- Breaking the wage hierarchy.
- Bypassing the British/Irish priority.
- Skipping the mandatory academy promotion.
- Claiming a player's rating or role familiarity that hasn't been seen in the save.

---

## 8. Must be confirmed in the save — do not assume

- [ ] Actual division and season (is the Championship premise correct?)
- [ ] Difficulty, gameplay preset, and any sliders
- [ ] Actual squad: names, ages, positions, OVRs **with the date observed**
- [ ] Role familiarity per player (Base / Role+ / Role++) for the roles we intend to use
- [ ] Contract status and wages, where the game exposes them
- [ ] Transfer budget and wage budget
- [ ] Whether the manager's preferred formation is pre-set or free
- [ ] Board season objectives as the game states them
- [ ] Academy prospects and their assessed potential (with the coach-quality caveat in §6.7)
- [ ] Whether Title Update 1.2.0 is live in the user's build

---

## 9. Known bugs and cautions

| Item | Detail |
|---|---|
| **Custom tactics not saving** | Reported across EA Forums: roles, positions and formation settings can revert after leaving the menu. A Manager Career specific case (players placed in wrong positions after saving a new tactic) was addressed in TU 1.1.0, but reports continued. **If the setup looks wrong at kick-off, it may be the game, not you.** Re-save tactics after each title update. |
| **Patch timing** | TU 1.0.4 (7 Oct) and TU 1.1.0 (27 Oct) shipped **no gameplay balance changes**. TU 1.2.0, due mid-November, is the first: fullbacks holding the defensive line, better offside awareness, better AI attacking runs, higher line after kick-off, improved loose-ball auto-switching. **Do not rebuild tactics for a patch that hasn't landed.** |
| **Editorial sources** | Some widely-cited FC 27 tactics explainers are published by boosting/RMT vendors. Their EA quotations are usable; their conclusions should be treated as opinion. |
| **Data sources** | fut.gg and futbin track **squads people build**, not formations people play in matchmade games. Usage percentages are directional, not match data. |
| **EA's own silence** | No published role count, no Role+/Role++ numbers, no formation win rates, no EA Help article on Player Roles. |

---

## 10. Sources

**Official (EA):**
- Career Deep Dive Pitch Notes — 31 July 2026 — `ea.com/games/ea-sports-fc/fc-27/news/pitch-notes-fc27-career-mode-deep-dive`
- Gameplay Deep Dive — 29 July 2026 — `ea.com/games/ea-sports-fc/fc-27/news/pitch-notes-fc27-gameplay-deep-dive`
- Closed Beta Feedback Update — 3 September 2026
- Gameplay Developer Launch Update — 30 September 2026
- Title Update v1.1.0 notes — 27 October 2026
- Gameplay Developer Notes — 28 October 2026 — `ea.com/games/ea-sports-fc/fc-27/news/fc27-october-gameplay-developer-notes`

**Data trackers:**
- fut.gg — `/tactics`, `/tactics/4-2-1-3/`, `/roles` — formation and role usage
- futbin — `/27/roles` — role/focus database

**Editorial (used for EA quotations and analysis, discounted for marketing):**
- timesaver.gg — "FC 27 Player Roles Explained" (12 Oct 2026); "Best Formations: Launch Week" (20 Sep 2026); "4-3-1-2 Is Everywhere" (11 Oct 2026); "Title Update 1.2.0" (28 Oct 2026)
- Red Bull — "Best EA FC 27 custom tactics from pro players" (Oct 2026); "Career Mode changes could transform the game" (2 Sep 2026)
- RB Leipzig / RBLZ Gaming — "Top 3 Formations" (Sep 2026)
- NealGuides — tactics and code tables (Sep–Oct 2026)

---

## 11. Change log

| Date | Change |
|---|---|
| 28 Oct 2026 | Initial version. Compiled from EA Pitch Notes, fut.gg/futbin data, and community tactical analysis. All claims tiered in §0. |
