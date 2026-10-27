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

The perspective maps also document the requested overland and mixed land/sea corridor framework. Treat these as broad connected travel corridors, not proof that every intermediate road, pass, ferry, port, or settlement is individually surveyed. Use the relevant regional modules for confirmed local edges; unresolved segments, landing points, schedules, fees, and travel times must remain unspecified. Do not infer that a direct air route requires or follows the land route.

Golden Dragon Empire and Beiming Gu have a confirmed direct corridor between Longyuan Sky Transit Terminal and Beiming Heartland Sky Transit Terminal. Tianhai Yunzhou remains a separate direct connection to Beiming Gu via that same Beiming terminal. Do not force a transfer through Tianhai Yunzhou when the direct corridor is available. Exact duration, departure frequency, and guaranteed availability remain unknown; check current events and access conditions. The tree is a navigation aid; this file and the endpoint regional modules remain authoritative for route validation.

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
