# Merzkava Universe — Connected Power Tree & Transit Map

**Purpose:** One connected navigation tree for the three major powers and their established regional branches, canonical source files, and inter-power transit. For matching line maps from each power's perspective—including land, maritime, wilderness, and air corridors—see [`world/THREE_POWER_PERSPECTIVE_MAPS.md`](THREE_POWER_PERSPECTIVE_MAPS.md).
**Status:** Navigation and route index. This file organizes existing canon; it does not create new settlements, borders, roads, routes, prices, or travel times.
**Authority:** Follow `INDEX.md` → `templates/AUTHORITY_ORDER.md` → `world/CANON_DECISIONS_AND_PRECEDENCE.md`; use the linked source files for their respective facts.

## 1. World tree — one root, three power branches

```text
MERZKAVA UNIVERSE
├── WORLD FOUNDATION
│   ├── INDEX.md
│   ├── templates/AUTHORITY_ORDER.md
│   ├── world/CANON_DECISIONS_AND_PRECEDENCE.md
│   ├── world/MAP_AND_REGIONS.md
│   ├── world/GEOGRAPHY_AND_TRAVEL.md
│   ├── world/LOCATION_AND_ROUTE_NETWORK.md
│   └── world/DYNAMIC_EVENTS.md
│
├── GOLDEN DRAGON EMPIRE — EAST
│   ├── Regional authority: world/GOLDEN_DRAGON_EMPIRE_GOVERNANCE.md
│   ├── Administrative tree: world/GOLDEN_DRAGON_EMPIRE_ADMINISTRATIVE_ATLAS.md
│   │   ├── Longyuan → Huanglongcheng (regional seat; imperial capital)
│   │   │   ├── Huanglong Prefecture
│   │   │   └── Jade Seal Prefecture
│   │   ├── Canglan → Qinghe
│   │   │   ├── Qinghe Prefecture
│   │   │   └── Jiangbei Prefecture
│   │   ├── Jinyue → Yumai
│   │   │   ├── Jadevein Prefecture
│   │   │   └── Ironcloud Prefecture
│   │   ├── Tianfeng → Tianshu
│   │   │   ├── Heavenly Script Prefecture
│   │   │   └── Cloud Summit Prefecture
│   │   ├── Yanling → Honglu
│   │   │   ├── Red Furnace Prefecture
│   │   │   └── Ashen Peak Prefecture
│   │   ├── Baiyue → Beiguan
│   │   │   └── Northwatch Prefecture
│   │   └── Xingluo → Dongxing
│   │       └── Eastern Star Prefecture
│   ├── Six county circuits (cross-prefecture service layer)
│   │   ├── Imperial Heartland Circuit → Huanglong + Jade Seal
│   │   ├── Riverlands Circuit → Qinghe + Jiangbei
│   │   ├── Mineral Lands Circuit → Jadevein + Ironcloud
│   │   ├── Scholarly Heights Circuit → Heavenly Script + Cloud Summit
│   │   ├── Furnace Mountains Circuit → Red Furnace + Ashen Peak
│   │   └── Frontier–Maritime Circuit → Northwatch + Eastern Star
│   ├── 13 officially registered named villages
│   │   ├── Longyuan → Dragonwell Village, Willowbend Village
│   │   ├── Canglan → Reedbank Village, Fish Lantern Village
│   │   ├── Jinyue → Orebrook Village, Jade Hollow Village
│   │   ├── Tianfeng → Inkstone Village, Crane Rest Village
│   │   ├── Yanling → Ashbrook Village, Ember Hollow Village
│   │   ├── Baiyue → Watchfire Village, Stonegate Village
│   │   └── Xingluo → Salt Lantern Village
│   ├── Other named hamlets/local settlements → see the atlas; not official villages
│   ├── Local modules: world/REGION_LONGYUAN.md, REGION_CANGLAN.md,
│   │   REGION_JINYUE.md, REGION_TIANFENG.md, REGION_YANLING.md,
│   │   REGION_BAIYUE.md, REGION_XINGLUO.md
│   ├── Governance / officials / public services:
│   │   world/GOLDEN_DRAGON_EMPIRE_GOVERNANCE.md
│   │   world/GOLDEN_DRAGON_EMPIRE_OFFICIALS.md
│   │   world/GOLDEN_DRAGON_EMPIRE_POPULATION_SERVICES.md
│   ├── Transit node: Longyuan Sky Transit Terminal
│   └── NPCs: regions/golden-dragon-empire/INDEX.md → npcs/REGISTRY.md → relevant profile
│
├── TIANHAI YUNZHOU — SOUTHWESTERN OCEAN / FLOATING ISLAND
│   ├── Main source: world/REGION_TIANHAI_YUNZHOU.md
│   ├── Seven established districts
│   │   ├── Yunxiao Terrace — government and Maharaja's administration
│   │   ├── Tianji Core — floating-island support-system area
│   │   ├── Cangqiong Harbor — harbor, shipping, logistics
│   │   ├── Haiyue Market — trade and high-value exchange
│   │   ├── Linggong District — crafts, engineering, manufacturing
│   │   ├── Xuanchao Ward — defense and maritime security
│   │   └── Misty Shoals — outer maritime zone and exploration
│   ├── Institutions: world/TIANHAI_ACADEMIES_AND_THINKER_INSTITUTE.md
│   ├── NPC power structure: regions/tianhai-yunzhou/npcs/POWER_STRUCTURE.md
│   ├── Established local anchors (full route graph in §§12–14)
│   │   ├── Yunxiao Terrace — Court Steps
│   │   ├── Lanternwake Village → Glasscurrent Hamlet
│   │   ├── Xuanchao Ward → Northwatch Quay → Reedmist Fishing Village
│   │   ├── Cangqiong Harbor ↔ Westwake Anchorage
│   │   ├── Haiyue Market → Pearlstep Landing → Bluefin Cove → Windglass Islet
│   │   └── Cangqiong Sky Transit Terminal — inter-power passenger hub
│   ├── Local route graph and services: world/REGION_TIANHAI_YUNZHOU.md §§12–14
│   ├── Transit node: Cangqiong Sky Transit Terminal
│   └── NPCs: regions/tianhai-yunzhou/INDEX.md → npcs/REGISTRY.md → relevant profile
│
└── BEIMING GU — NORTH
    ├── Single regional source: world/REGION_BEIMING_GU.md
    ├── Seven established districts
    │   ├── Beiming Heartland — main settlements and administration
    │   ├── Frostveil Range — cold mountain barrier
    │   ├── Azureflame Basin — spiritual basin / blue-flame association
    │   ├── Silverpine Wilds — forests, Spirit Beasts, herbs, hunting
    │   ├── Stonegate March — mountain passages and border defense
    │   ├── Hollowmoon Valley — remote valleys and secluded paths
    │   └── Ironroot Reach — minerals, raw materials, workshops
    ├── District-level settlement names and internal routes: not yet established
    ├── Transit node: Beiming Heartland Sky Transit Terminal
    └── NPCs: regions/beiming-gu/INDEX.md → npcs/REGISTRY.md → relevant profile

CROSS-POWER TRANSIT — THREE CONNECTED POWER NODES
├── Golden Dragon Empire: Longyuan Sky Transit Terminal
│   ├── dedicated liquefied-energy passenger aircraft ↔ Cangqiong Terminal
│   │   └── Tianhai Yunzhou
│   └── dedicated liquefied-energy passenger aircraft ↔ Beiming Heartland Terminal
│       └── Beiming Gu
├── Tianhai Yunzhou: Cangqiong Sky Transit Terminal
│   ├── dedicated liquefied-energy passenger aircraft ↔ Longyuan Terminal
│   │   └── Golden Dragon Empire
│   └── dedicated liquefied-energy passenger aircraft ↔ Beiming Heartland Terminal
│       └── Beiming Gu
└── Beiming Gu: Beiming Heartland Sky Transit Terminal
    ├── dedicated liquefied-energy passenger aircraft ↔ Cangqiong Terminal
    │   └── Tianhai Yunzhou
    └── dedicated liquefied-energy passenger aircraft ↔ Longyuan Terminal
        └── Golden Dragon Empire

All three powers have a direct mapped connection to each other. The GDE–Beiming corridor uses
the same Beiming Heartland Sky Transit Terminal as the Tianhai–Beiming corridor; it is a
separate origin-to-destination edge, not a requirement to transfer through Tianhai Yunzhou.
```

> **Tree-reading rule:** A branch shows source hierarchy and known geographic organization. It does not prove that every child location has a direct road, that every district is internally mapped, or that all routes are open. For actual movement, use the route edges in §3.

## 2. Canonical regional source directory

| Power / branch | Primary regional source | Administrative / supplementary authority | NPC ↔ Map path |
|---|---|---|---|
| Golden Dragon Empire | The matching `world/REGION_<REGION>.md` file for the scene | `world/GOLDEN_DRAGON_EMPIRE_ADMINISTRATIVE_ATLAS.md`; governance, officials, and population-services files as needed | NPC → profile → map; or map → local NPC entries → plausible profiles |
| Tianhai Yunzhou | `world/REGION_TIANHAI_YUNZHOU.md` | `world/TIANHAI_ACADEMIES_AND_THINKER_INSTITUTE.md`; NPC power structure; local routes and service networks in §§12–14 of the regional module | NPC → profile → map; or map → local NPC entries → plausible profiles |
| Beiming Gu | `world/REGION_BEIMING_GU.md` (all seven districts) | The consolidated module is the source for district-level confirmed facts; unspecified settlements and routes remain unspecified | NPC → profile → map; or map → local NPC entries → plausible profiles |

### Golden Dragon Empire administrative hierarchy

The atlas is authoritative for the seven regions, twelve prefectures, six county circuits, and thirteen officially registered named villages. The tree lists the established regional seats, prefectures, circuits, and official village roster for navigation. County circuits coordinate two prefectures each; they are a cross-prefecture service layer, not another region or a tiny district nested under one prefecture. Consult the atlas for exact parent relationships, the 21 separately classified hamlets/local settlements, and the named local route framework. Do not revive superseded counts or promote hamlets to official villages.

The atlas also establishes these six named administrative corridors: **Imperial Dragon Road** (Huanglongcheng ↔ Yuxi), **Twin River Route** (Qinghe ↔ Jiangbei), **Ore Vein Road** (Yumai ↔ Tieyun), **Cloudstep Scholar Road** (Tianshu ↔ Yunding), **Furnace Spine Road** (Honglu ↔ Huifeng), and **Frontier–Maritime Relay** (Beiguan ↔ Eastern Star). The last is a staged land/sea administrative relay, not one direct road. These route names do not establish exact distances or travel times; use the atlas and local regional modules for route legs and constraints.

### Tianhai Yunzhou district hierarchy

The seven district names and broad identities are established, but they are not a complete settlement map. Follow the local route graph in the regional module for known corridors, docks, train links, transfer points, and conditional boat routes. An unlisted edge remains unestablished.

### Beiming Gu district hierarchy

The seven district names and broad identities are established in one consolidated regional module. Exact adjacency, named towns/villages, district officials, and most internal routes remain unestablished. The seven legacy district files are compatibility pointers, not independent canon sources.

## 3. Inter-power transit graph — established edges only

| Edge | Direction | Transport | Fare | Operating window | Intermediate stops / duration | Canon status |
|---|---|---|---|---|---|---|
| Longyuan Sky Transit Terminal ↔ Cangqiong Sky Transit Terminal | Both directions | Dedicated Tianhai Yunzhou liquefied-energy Artificial Artifact passenger aircraft | **25 xc per passenger, round trip** | **05:00–21:00 local terminal time** | No intermediate stop established; exact duration, departure frequency, and aircraft capacity unknown | Established corridor |
| Beiming Heartland Sky Transit Terminal ↔ Cangqiong Sky Transit Terminal | Both directions | Dedicated Tianhai Yunzhou liquefied-energy Artificial Artifact passenger aircraft | **25 xc per passenger, round trip** | **05:00–21:00 local terminal time** | No intermediate stop established; exact duration, departure frequency, and aircraft capacity unknown | Established corridor |
| Longyuan Sky Transit Terminal ↔ Beiming Heartland Sky Transit Terminal | Both directions | Dedicated Tianhai Yunzhou liquefied-energy Artificial Artifact passenger aircraft | **25 xc per passenger, round trip** | **05:00–21:00 local terminal time** | No intermediate stop established; exact duration, departure frequency, and aircraft capacity unknown | Established direct corridor; same Beiming destination terminal as the Tianhai–Beiming service |

### Connected travel between all three powers

The established network is connected as a graph through Tianhai Yunzhou:

- **Golden Dragon Empire → Tianhai Yunzhou:** use Longyuan Sky Transit Terminal ↔ Cangqiong Sky Transit Terminal.
- **Beiming Gu → Tianhai Yunzhou:** use Beiming Heartland Sky Transit Terminal ↔ Cangqiong Sky Transit Terminal.
- **Golden Dragon Empire ↔ Beiming Gu:** a direct corridor connects Longyuan Sky Transit Terminal and Beiming Heartland Sky Transit Terminal. It uses the same Beiming destination terminal as the established Tianhai Yunzhou–Beiming Gu corridor; travel does not require a transfer through Tianhai Yunzhou.
- The **25 xc fare is the standard round-trip fare per passenger for each dedicated energy-aircraft corridor**, including the direct Longyuan–Beiming Heartland corridor. Do not infer a one-way price, bundled fare, exact duration, or departure time.
- When the dedicated aircraft service is closed or unavailable, ordinary Qi-powered flying ships are established as a 24-hour alternative subject to access and operating conditions. A comparable round trip costs **86 xc per passenger**. Do not infer exact departure times, duration, or guaranteed availability.
- Aircraft service may be suspended for weather, security, maintenance, or fuel-supply disruption. Check current events and scene conditions before resolving travel.
- Transit hours use each terminal's local time. Exact time-zone offsets and flight duration are not established.

## 4. How the GM resolves a route

1. Identify the character's actual origin and intended destination.
2. Follow the tree to the correct power and regional module at both ends.
3. Open `world/LOCATION_AND_ROUTE_NETWORK.md` and verify each edge. For cross-power travel, check this section and the two endpoint modules.
4. Check `world/GEOGRAPHY_AND_TRAVEL.md`, `world/DYNAMIC_EVENTS.md`, and relevant access/security restrictions.
5. Resolve duration and action costs only through `gameplay/TIME_AND_ACTION_RULES.md`. Unknown duration must stay unknown until the official time-resolution rules support a result.
6. For a two-leg journey through Tianhai Yunzhou, resolve each leg and any transfer separately; do not skip the intermediate location or assume a guaranteed connection.
7. Update the character's location only after the travel action completes.

## 5. Route-map data rules

Every confirmed route is a graph edge with its own source, transport, access conditions, known intermediate stops, fare basis, schedule status, duration status, and disruption conditions. A route may be directional or conditional; do not assume all edges are reciprocal merely because a terminal pair is shown with ↔. Here, the two named passenger-aircraft corridors are established as round-trip services between their terminal pairs.

Use these status labels consistently:
- **Established** — explicitly confirmed in a canonical source.
- **Conditional** — established route, but operation depends on weather, pilot, schedule, access, or other stated condition.
- **Unknown / not established** — no confirmed edge or detail; not proof that travel is impossible.
- **Proposal — pending owner confirmation** — a suggested new route, never treated as active canon before approval.

## 6. Source links

- [Central bootstrap](../INDEX.md)
- [GM authority](../templates/AUTHORITY_ORDER.md)
- [Canon precedence](CANON_DECISIONS_AND_PRECEDENCE.md)
- [Map and regional overview](MAP_AND_REGIONS.md)
- [Geography and travel rules](GEOGRAPHY_AND_TRAVEL.md)
- [Location and route network rules](LOCATION_AND_ROUTE_NETWORK.md)
- [Golden Dragon administrative atlas](GOLDEN_DRAGON_EMPIRE_ADMINISTRATIVE_ATLAS.md)
- [Tianhai Yunzhou regional module](REGION_TIANHAI_YUNZHOU.md)
- [Beiming Gu consolidated regional module](REGION_BEIMING_GU.md)
- [Dynamic event registry](DYNAMIC_EVENTS.md)
