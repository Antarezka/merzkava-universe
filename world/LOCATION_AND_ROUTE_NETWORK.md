# Merzkava Universe — Location and Route Network

**Purpose:** Define how settlements, districts, landmarks, and wilderness sites connect for exploration and travel.
**Canon rule:** This file defines the data format and navigation method, not new geography. Only explicitly confirmed routes are canon. A missing edge means “not established”, not “impossible to travel”.

## 1. Source-of-truth hierarchy

1. `world/MAP_AND_REGIONS.md` defines the broad geographic model and named regions.
2. `world/GEOGRAPHY_AND_TRAVEL.md` defines broad terrain and transport principles.
3. `world/GOLDEN_DRAGON_EMPIRE_ADMINISTRATIVE_ATLAS.md` is authoritative for imperial administrative names, counts, and parent relationships.
4. The matching `world/REGION_*.md` is authoritative for local settlements, local routes, local transport, regional economy, and the regional NPC registry.
5. `gameplay/TIME_AND_ACTION_RULES.md` governs travel-time resolution.
6. `world/DYNAMIC_EVENTS.md` may change route safety, access, or availability only when a relevant event is recorded.

If sources conflict, do not silently choose a convenient route. Follow the higher authority above and flag unresolved conflicts for owner review.

## 2. Model locations as a graph

Treat each named location as a node and each confirmed route as a separate connection (edge). Routes are not automatically reciprocal: a one-way pass, restricted gate, seasonal crossing, dangerous descent, or scheduled boat may allow travel in only one direction or under conditions.

Each route record should specify origin → destination; route type; access conditions; usual transport; known intermediate stops; travel-time source and estimate status; economic/social function; risks and disruptions; and canon source/confidence.

## 3. Connected three-power transit overview

Use [`world/WORLD_NAVIGATION_TREE.md`](WORLD_NAVIGATION_TREE.md) as the cross-power navigation index and [`world/THREE_POWER_PERSPECTIVE_MAPS.md`](THREE_POWER_PERSPECTIVE_MAPS.md) for three consistent line maps showing each power's perspective on land, maritime, wilderness, and air connections. Three direct inter-power air corridors are established: Longyuan Sky Transit Terminal (Golden Dragon Empire) ↔ Cangqiong Sky Transit Terminal (Tianhai Yunzhou); Beiming Heartland Sky Transit Terminal (Beiming Gu) ↔ Cangqiong Sky Transit Terminal; and Longyuan Sky Transit Terminal ↔ Beiming Heartland Sky Transit Terminal. The direct Golden Dragon–Beiming route uses the same Beiming destination terminal as the Tianhai–Beiming route. All dedicated liquefied-energy passenger-aircraft corridors operate 05:00–21:00 local terminal time and have a standard **25 xc per passenger round-trip fare**; exact duration and timetable remain unknown. Ordinary Qi-powered flying ships are a 24-hour alternative under normal access/operating conditions, with a comparable **86 xc round-trip fare**.

The maps and `world/GEOGRAPHY_AND_TRAVEL.md` define one connected sea network: Frostmirror Sea → northeastern maritime passage → Eastern Azure Sea → eastern open-water passage → Yunmeng Sea; Yunmeng Sea connects through Lantern Passage to Wufeng Sea, which links back toward Eastern Azure Sea through Three-Lantern Passage. Yunmeng's western/southern approach reaches Lawless Territories and then ordinary Black Tide Sea; only beyond Black Tide Sea's southern outer boundary lies far-southern Guixu Canghai. Cangqiong Harbor ↔ Dongxing Port is the established mainland shipping corridor. Wufeng Sea is favored by specialized liquefied-energy Artificial Artifact vessels because ambushes are uncommon, but it has no wind, waves, or currents. Exact coordinates, distances, durations, timetables, and safe-passage guarantees remain unspecified.

Golden Dragon Empire and Beiming Gu have a confirmed direct corridor between Longyuan Sky Transit Terminal and Beiming Heartland Sky Transit Terminal. Tianhai Yunzhou remains a separate direct connection to Beiming Gu via that same Beiming terminal. Do not force a transfer through Tianhai Yunzhou when the direct corridor is available. Exact duration, departure frequency, and guaranteed availability remain unknown; check current events and access conditions. The tree is a navigation aid; this file and the endpoint regional modules remain authoritative for route validation.


### 3.1 Owner-requested land and maritime corridor framework

The perspective maps connect the three powers through broad overland and mixed land/sea itineraries as well as the established air corridors. These are approved **corridor-level map links**, not proof that every local road, mountain pass, river crossing, ferry, mainland landing, or port-to-port sailing schedule has been surveyed. Validate each local segment against its regional module; resolve missing segments through exploration rather than inventing infrastructure.

| Perspective / endpoints | Mapped corridor sequence | Mode | Status and limits |
|---|---|---|---|
| Golden Dragon Empire ↔ Beiming Gu | Beiguan (Baiyue) → Nine Frost Wastes (external northern wilderness) → Stonegate March → Frostveil Range → Beiming Heartland | Land; overland travel | Owner-requested mapped corridor. Exact pass, road alignment, settlements, distance, and duration unknown; weather, cold, terrain, and security affect access. Separate from the direct air corridor. |
| Golden Dragon Empire ↔ Tianhai Yunzhou | Golden Dragon internal route network toward Xingluo / Dongxing → Dongxing Port → Eastern Azure Sea → eastern open-water passage → Yunmeng Sea → Cangqiong Harbor | Land + sea | Established corridor-level itinerary. Do not assume every imperial region has a direct road to Dongxing; verify internal legs. Exact sailing duration, schedule, fare, and local approach remain unspecified. |
| Tianhai Yunzhou ↔ Beiming Gu | Cangqiong Harbor → Yunmeng Sea → Eastern Azure Sea → northeastern maritime passage → Frostmirror Sea → Beiming northern coastal approach → northern land/wilderness route → Nine Frost Wastes → Stonegate March → Frostveil Range → Beiming Heartland | Sea + land | Mapped outer-sea corridor; the Azerion labyrinth exit is not a normal port. Exact landing point, local road alignment, vessel schedule, fare, and duration remain unspecified. Not a land bridge from the floating island. |

### 3.2 Eastern Azure Sea ports and coastal transfers

| Origin → destination | Route / waterway | Status and constraints |
|---|---|---|
| Dongxing Port → Cangqiong Harbor | Eastern Azure Sea → eastern open-water passage → Yunmeng Sea | Established main inter-power shipping corridor; exact duration, schedule, fare, and safe passage are not set. |
| Mingzhu Port ↔ Eastern Azure Sea | Local port access to the Eastern Azure Sea shipping lane | Established port; individual direct links to other ports are not assumed. |
| Lanfan Port → Wind Sail Hamlet | Coastal route | Established route; heavy goods move by boat, exact schedule unknown. |
| Chaoguan Port → Tideglass Hamlet | Small-vessel route | Established route; storms may force a detour. |
| Dongxing → Pearl Shoal Hamlet | Small coastal boat | Established route; landing depends on tide. |
| Yuhai Port, Yuandeng Port, Longchao Port | Eastern Azure coastal shipping | Established port settlements; exact pairwise routes and schedules remain unspecified. |
| Yanfeng coastal settlement | Eastern Azure coastal belt | Coastal settlement only; do not assume a dock or port. |
| Yunmeng Sea → Wufeng Sea | Lantern Passage | Established sea-to-sea corridor; Wufeng Sea has no wind, waves, or currents. Specialized liquefied-energy Artificial Artifact vessels are favored; ambushes are uncommon, not impossible. |
| Wufeng Sea → Eastern Azure Sea | Three-Lantern Passage | Established eastern connection; the route does not imply wind or currents inside Wufeng Sea. |
| Beiming northern coast → Eastern Azure Sea | Northeastern maritime passage via Frostmirror Sea | Established broad coastal connection; do not use the Azerion labyrinth exit as a port. |
| Yunmeng Sea → Lawless Territories → Black Tide Sea | Western/southern sea-facing approach and ordinary open water | Lawless is the nearest major organized region to Guixu Canghai. Black Tide Sea is ordinary water and separates Lawless from Guixu Canghai. |
| Black Tide Sea → Guixu Canghai | Cross the southern outer boundary of Black Tide Sea | Guixu Canghai is beyond this boundary at the far-southern, frigid edge of the world; no direct shore-to-Guixu shortcut exists. |
| Lawless southern coast → Southwake Port | Coastal access to the established southern Lawless port | Nearest organized port-side approach toward Guixu Canghai; no direct road from a named village is established. |
| Southwake Port → Lanternhook Isles | Vessel route across ordinary Black Tide Sea | Small pirate/criminal leisure and black-market archipelago; exact sailing time and schedule are unknown. |
| Lanternhook Isles → Guixu Canghai | Cross ordinary Black Tide Sea and then its southern outer boundary | Guixu remains beyond the boundary; the isles are not part of Guixu Canghai and do not guarantee safe passage. |

### 3.3 Shared Azerion Forest connections

| Perspective / endpoints | Mapped corridor sequence | Mode | Status and limits |
|---|---|---|---|
| Tianhai Yunzhou → Lawless Territories → Azerion Forest | Western side of Tianhai's floating position / sea-facing approach → Lawless Territories → easiest known Azerion Forest entrance | Sea-side approach + wilderness | Owner-confirmed geographic relationship. No mainland landing, sea name, exact route, or travel time is assigned. Tianhai remains a floating island; no land bridge is implied. |
| Azerion Forest → Golden Dragon Empire | Forest frontier → rushing-river trap corridor → small Golden Dragon Empire prison island in midstream → imperial side | Dangerous river-boundary route | Owner-confirmed geographic feature. Do not assume a bridge, safe ford, normal public crossing, river name, coordinates, or prison details. |
| Beiming Gu → Azerion Forest | Beiming northern coast → ruined/labyrinth exit on Azerion's northern deep-sea coast ← Mega Colossal Labyrinth ← ruins entrance in the central lake | Coastal approach + ruined underground route | Owner-confirmed route relationship tied to the existing canon that the labyrinth exits to the northern deep-sea coast. The interior is unmapped and hazardous; do not invent internal passages or promise safe transit. |

These connections describe different sides of the same forest and are not one continuous public road. The Lawless entrance is the easiest known forest entrance; the northern coastal ruined exit is the route relevant to Beiming; the rushing river and prison island form the Golden Dragon-facing obstacle.

### 3.4 Lawless regional links and unconfirmed edges

| Lawless region | Established geographic relationship | Map edge that may be used | Do not infer |
|---|---|---|---|
| Ashen Borderlands | Outside Golden Dragon Empire's western/southwestern borders; four named villages and four associated organizations | Lawless Territories → easiest known Azerion Forest entrance; separately, Azerion's eastern boundary → rushing-river trap → small Golden Dragon prison island → imperial side | A direct road from Greyrock, Blackreed, Broken Bell, or Dust Lantern Village to the forest entrance, river, or island; a safe ford or bridge; current faction ownership |
| Black Tide Expanse | Remote islands and sea routes outside Tianhai's direct control; four named settlements and four associated organizations | Yunmeng Sea western/southern approach → Lawless Territories → ordinary Black Tide Sea; Black Tide Sea → Guixu Canghai only after crossing its southern outer boundary | A direct harbor-to-every-island route, a universal island chain, an assumption that Black Tide Sea is cursed, or a shortcut directly from Lawless to Guixu |
| Nine Frost Wastes | Northern wilderness outside Beiming's official defenses; four named villages and four associated organizations | Beiguan → Nine Frost Wastes → Stonegate March → Frostveil Range → Beiming Heartland | That the Wastes are a Beiming district; direct village-to-village roads; exact pass, road alignment, safe passage, distance, or duration |

The three Lawless regions are separate map branches tied to different neighboring perspectives. Their presence on one map does not establish direct adjacency or a traversable route between them. Load the relevant regional modules before resolving a local trip; a missing edge remains unconfirmed, not impossible.

The named outer areas retain their own jurisdictional status: Nine Frost Wastes and Lawless Territories are not absorbed into either neighboring power by appearing on a route. Azerion Forest, Black Tide Expanse, Wanluo Sacred Expanse, and the high cloud-sea mountains are shown as wider-world geographic context or optional side regions, not mandatory transit points. See [the three perspective maps](THREE_POWER_PERSPECTIVE_MAPS.md) for all three views.


| Longyuan Sky Transit Terminal (Golden Dragon Empire) | Beiming Heartland Sky Transit Terminal (Beiming Gu) | Dedicated long-distance Artificial Artifact energy-aircraft | No intermediate stop established | Ticket, safety inspection, compatible fuel supply, aircraft availability; weather, security, maintenance, and supply disruption may suspend service | Passenger travel, official delegations, traders, and light baggage | Not set | Established direct inter-power corridor; standard round-trip fare 25 xc per passenger; exact duration and schedule unknown |

## 4. Regional location-network table

Every regional module should maintain a compact route table. Include only confirmed or explicitly owner-approved provisional routes.

| Origin | Destination | Route / transport | Intermediate stops | Access and constraints | Trade / social function | Travel time / source | Canon status |
|---|---|---|---|---|---|---|---|
| Belum ditetapkan | Belum ditetapkan | Belum ditetapkan | — | Belum ditetapkan | Belum ditetapkan | Unknown | Not established |

Do not fill this table with fabricated connections merely to remove blanks. If the owner asks the GM to develop the region, proposed connections must first be labeled **Proposal — pending owner confirmation**.

## 5. Connectivity and realism rules

- Not every village connects directly to a city. Some destinations require passing through a bridge, ferry, village, pass, gate, or port.
- Rivers, mountain ridges, ravines, forests, seas, walls, and hostile territory shape viable routes; do not draw straight-line roads through obstacles without an established crossing.
- A route being present on a map does not mean it is safe, open, free, fast, or available to every character.
- Do not infer route distance or travel duration from population, administrative hierarchy, or narrative prominence.
- Use only transportation that exists in canon and that the character can access.
- Trade links should reflect complementary local resources, labor, demand, transport capacity, and risks. A resource-rich village does not automatically have a profitable export route.
- If an action requires a missing connection, treat it as exploration of an unknown route or ask the owner; do not assert that it was already mapped.
- Travel can create encounters, delays, tolls, fatigue, cargo costs, rumors, and relationships when justified by location, time, and recorded conditions; these are not guaranteed events.
- Route changes caused by floods, war, landslides, Spirit Beast activity, blockades, or political decisions must be supported by a recorded event or explicitly framed as a new scene event.

## 6. Location-level life and economy

For each major settlement or exploration anchor, describe when established: settlement role and approximate scale (no invented precise population totals); local authority; daily rhythm, customs, public services, and access limitations; local skills, labor, resources, and goods; imports and needs; actual markets, craft, transport, lodging, medical, education, or Thinker services; nearby points of interest and access; recurring NPCs and canonical profiles; and local conflicts or events.

A small village may have a distinct economic role without needing a permanent profile for every resident or shop. Ordinary people can be portrayed situationally under `world/NPC_MANAGEMENT.md`.

## 7. Travel resolution

Before resolving travel: (1) identify origin and destination; (2) load regional modules for both ends and known intermediate places; (3) verify connection, route type, stops, transport, and restrictions; (4) check current events; (5) resolve duration and action costs using `gameplay/TIME_AND_ACTION_RULES.md`; (6) update the scene location only after travel completes.

## 8. Owner workflow

- [ ] Confirm settlements and parent jurisdictions.
- [ ] Add only geographically plausible, owner-approved routes.
- [ ] Make required intermediate locations explicit.
- [ ] Connect production to realistic demand and transport.
- [ ] Cross-reference important NPCs and faction records.
- [ ] Update the regional module and `INDEX.md` when a new canonical location or route is accepted.
