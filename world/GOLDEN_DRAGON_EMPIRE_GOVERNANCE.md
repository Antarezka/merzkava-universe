# Merzkava Universe — Golden Dragon Empire Governance

**Scope:** Civil administration, imperial institutions, territorial hierarchy, public offices, oversight, and the separate military chain of command.  
**Status:** Established governance framework, with territorial counts and names maintained in `world/GOLDEN_DRAGON_EMPIRE_ADMINISTRATIVE_ATLAS.md`. Officeholders are recorded separately when established.  
**Primary references:** `world/WORLD.md`, `world/MAP_AND_REGIONS.md`, `world/GOLDEN_DRAGON_EMPIRE_ADMINISTRATIVE_ATLAS.md`, `world/FACTIONS.md`, and the seven regional modules.

---

## 1. Governing Principles

1. The Emperor is the highest sovereign authority of the Golden Dragon Empire.
2. The Empire is too large to be governed personally by the Emperor alone; administration depends on central institutions, regional governors, local officials, and public offices.
3. **A noble title, clan affiliation, Spirit Realm, or personal strength does not automatically grant a government office or legal jurisdiction.** Authority must come from a recognized appointment, lawful delegation, or established local arrangement.
4. Civil administration and military command are distinct chains. A governor is not automatically the commander of every garrison in their territory, and a military commander does not automatically administer civilian affairs.
5. The seven established regions are geographic and regional identities. They are not, by themselves, a complete list of administrative units or proof of exact borders.
6. The standard territorial counts and jurisdiction names are recorded in `world/GOLDEN_DRAGON_EMPIRE_ADMINISTRATIVE_ATLAS.md`. The named units are established; exact map coordinates, surveyed borders, legal codes, and current officeholders remain open unless recorded in the relevant module.

## 2. Civil Government — From the Center to the Local Level

```text
Emperor
└── Imperial Council / Grand Secretariat
    ├── Central Ministries and Imperial Agencies
    └── 7 Regional Governors
        └── 12 Prefectures
            └── 6 County Circuits (each coordinates two prefectures)
                └── Local offices and settlements (not counted as extra tiers)
                    └── 13 named rural villages in the official atlas
                        └── Household Register (population-record unit)
```

The administrative atlas establishes **7 regions, 12 prefectures, 6 county circuits, and 13 named rural villages** as the current simplified register. Each county circuit coordinates two prefectures; these are broad service jurisdictions, not small districts nested neatly inside a single prefecture. Small towns are not a separate official tier and cities have no fixed empire-wide count. The former counts of 33 prefectures, 268 counties, 361 cities, 1,838 towns, and 22 villages are superseded. Former prefectural seats remain settlements or service hubs; former county magistrates remain NPCs and may be reassigned to local or circuit roles. Household registers are population-record units, not a government tier.

### 2.1 Emperor

The Emperor is the supreme sovereign of the Golden Dragon Empire. The currently established ruler is **Jun Haotian (君昊天)**; see `../regions/golden-dragon-empire/npcs/JUN_HAOTIAN.md` and `world/WORLD.md`.

The Emperor's established sovereignty does not mean every local decision is personally made by him. Day-to-day governance is carried out through institutions and appointed officials.

### 2.2 Imperial Council and Grand Secretariat

The Imperial Council coordinates major policy, inter-ministerial matters, regional reports, and decisions requiring central review. The Grand Secretariat manages imperial documents, decrees, records, appointments, and the transmission of lawful orders.

These are functional offices in the governance framework; the council's exact membership, seat count, appointment procedure, and formal division of duties have not been individually named.

### 2.3 Central Ministries and Oversight

The following portfolio structure is the standard recommended model:

| Institution | Primary responsibility |
|---|---|
| Ministry of Personnel | Civil appointments, promotions, transfers, official evaluations, and staffing records |
| Ministry of Finance | Imperial revenue, public expenditure, tax administration, budgets, and fiscal reports |
| Ministry of Education and Rites | State academies, official examinations, ceremonies, and public educational standards |
| Grand Martial Soul Awakening Hall | Centralized imperial institution coordinating Martial Soul awakening, strategic workforce priorities, and the biennial subsidized public-awakening visits; it dispatches designated officials to villages rather than maintaining an assumed permanent branch in every locality |
| Ministry of Military Affairs | Central military administration, recruitment records, supplies, and coordination with the command structure; not automatic field command over every unit |
| Ministry of Justice | Imperial law, courts, legal procedure, appeals, and administration of penalties |
| Ministry of Public Works | Roads, bridges, canals, flood control, public buildings, and major infrastructure |
| Imperial Oversight Agency | Audits, misconduct investigations, official complaints, and review of abuse of authority |

The list defines portfolios, not a claim that every ministry already has named ministers, fixed subdivisions, or a fully documented legal code. Those details must be added only when established.

#### 2.3.1 Imperial Strategic Awakening and Workforce Program

The Empire runs a centrally funded program through the **Grand Martial Soul Awakening Hall**, coordinated with the Ministry of Finance and the Ministry of Education and Rites. Its purpose is to identify confirmed Martial Soul functions that answer documented imperial workforce shortages and connect suitable people with training, public service, or relevant occupations. Awakening remains a public service; the program does not change rarity odds or guarantee employment, academy admission, income, or a particular career.

**Central allocation rule**

- The central government sets the total program envelope, the funding period, the national shortage priorities, and the allocation to each region. Regional governments do not independently set their own share or replace the central formula with local economic conditions.
- The formula below is the default canon for this program. Let **B** be the total central budget for a funding period and **Sᵣ** be a region's verified Strategic Awakening Score.
- **Regional allocation = (20% × B ÷ 7) + (80% × B × Sᵣ ÷ ΣS)**, where ΣS is the sum of all seven regions' scores. If every region's score is zero, the performance pool is held for central review rather than divided using invented scores.
- The equal base portion keeps essential public awakening services operating in every region. The performance portion rewards verified outcomes that answer current imperial shortages. A region with a higher verified score receives a larger performance allocation; its local wealth, tax revenue, resident status, and raw rarity distribution do not directly increase the score.
- **Strategic Awakening Score:** count each distinct, verified awakening once, then multiply it by the centrally published priority weight for its confirmed function. The central priority schedule reflects documented shortages and may change between funding periods. A person cannot be counted twice for the same awakening, and rarity alone earns no points. Exact priority weights and the size of the total budget are set in the central funding order for each period, not improvised by a regional official or GM.
- A strategically useful awakening means that the Martial Soul's demonstrated or canonically established function fits a field in which the Empire has a documented shortage—such as medicine, irrigation, construction, material processing, transport, logistics, or another field named in the current central priority schedule. A simple or low-rarity Martial Soul may qualify; Myth or Legendary rarity alone does not.
- The program funds outreach, safe awakening facilities, assessment of confirmed practical aptitude, training referrals, approved service placements, and the defined biennial public-awakening subsidy. Funding must not be used to raise rarity odds, force mutation decisions, or promise a guaranteed outcome.
- **Two routes, different payment rules:** an independent paid awakening costs 3 xg 76 xs in total (3 xg 25 xs service fee, 8% service tax on that fee = 26 xs, 15 xs documentation, and 10 xs proof token). For the regular public visit held generally once every two years after New Year, the Imperial subsidy covers the service fee, its tax, and documentation; the individual pays only the 10 xs proof-token fee. This is the program's established subsidy and does not require a separate waiver for each resident. The service, tax, and documentation costs are recorded against the authorized central program budget.
- **Token-fee debt for people unable to pay:** if a person cannot afford the 10 xs token fee on the public route, a local external financial organization may advance that exact amount and issue a written debt note to the individual. The lender is a private/external organization, not the Empire, the Hall, or an Imperial ministry. The Empire does not guarantee or collect the private loan, and Imperial subsidy does not cover interest. Randomly select from plausible organizations available locally; ordinary reputable lenders commonly use 3%–8% simple annual interest, while an unlucky draw may be a high-cost lender at 12%–24% simple annual interest. The selected lender and rate are fixed for the note and cannot be rerolled. Principal is limited to the unpaid part of the token fee; do not borrow the already-subsidized service, tax, or documentation costs. Use proportional simple interest for periods under one year; no compounding or extra fees unless explicitly written in the note.
- The debt note must identify the lender, exact principal advanced, interest rate and calculation, repayment schedule, and due dates. Record the advance, liability, interest, and each installment separately. A loan is not income and must not be added to Wallet as spendable earnings if the lender paid the token issuer directly.
- **Default consequences:** nonpayment can harm credit reputation with the lender and, where such records are lawfully checked or shared, make decent-paying work, future credit, and a stable standard of living much harder to secure. This is a serious socioeconomic consequence, not an automatic empire-wide employment ban. Collection procedures and any other consequences depend on the actual lender's note and applicable local rules; do not invent imprisonment, automatic seizure, or universal blacklisting.
- The proof token is linked to the recorded awakening and helps verify completion for basic employment and education applications. It does not guarantee employment, admission, scholarship, income, or treatment based on rarity. Program records support verification and auditing but do not establish a universal public registry or mandatory certificate.
- The Hall submits outcome reports and a budget request; regional offices provide supporting records; the Ministry of Finance calculates and releases allocations under the central rule. The Ministry of Education and Rites coordinates relevant public education and ceremony standards. The Imperial Oversight Agency may inspect suspected manipulation or diversion under the oversight framework.
- Program records must support verification of counted outcomes and expenditure. This is a program-specific audit trail, **not** a declaration that a universal national registry or mandatory citizen certificate exists.

**Integrity risks and corruption**

The system creates incentives that can be abused. Plausible misconduct includes inflating the number of strategic awakenings, misclassifying ordinary outcomes to fit a priority field, counting the same person twice, fabricating training or placement records, bribing assessors, diverting outreach funds, steering contracts to allies, demanding kickbacks, or suppressing a region's valid results to shift funds elsewhere. Such conduct is a possible event, not an assumption that every official is corrupt.

Controls include cross-checking outcome records, sampling local cases, comparing claimed results with actual service or training evidence, reviewing expenditure, and referring suspicious discrepancies for investigation. The Ministry of Finance may withhold or recover disputed program payments pending review; the Imperial Oversight Agency may investigate suspected abuse within its established remit. Officials, noble houses, clans, and local elites can attempt to influence these controls, so oversight is not a guarantee that corruption is eliminated. Specific penalties, investigator appointment rules, and appeal procedures remain governed by the wider legal framework and are not invented here.

This funding rule does not change awakening rarity odds, mutation odds, or the fairness of the awakening process. Officials must not manipulate results to increase a region's score.


### 2.4 Regional Governors

Each of the seven regions has a regional administrative role responsible for coordinating the region's prefectures, reporting to the center, implementing imperial policy, and addressing issues that cross local jurisdictions.

The regional identities are:

- **Longyuan — Imperial Heartland:** court, central administration, nobles, and political institutions.
- **Canglan — Riverlands:** agriculture, irrigation, river transport, and inland trade.
- **Jinyue — Mineral Lands:** mining, spiritual metals, and artifact materials.
- **Tianfeng — Scholarly Heights:** scholarly traditions, talent development, literacy, and knowledge exchange; it is a source of gifted students for the two central academies in Huanglongcheng, not a regional academy network.
- **Yanling — Volcanic Mountains:** smithing, furnaces, and spiritual forging.
- **Baiyue — Frontier Marches:** border defense, fortifications, and military routes.
- **Xingluo — Eastern Ports:** maritime trade, diplomacy, and sea routes.

These seven regional identities and their administrative seats/counts are established in `world/GOLDEN_DRAGON_EMPIRE_ADMINISTRATIVE_ATLAS.md`. The current named governors are recorded in `world/GOLDEN_DRAGON_EMPIRE_OFFICIALS.md`; surveyed legal boundaries remain unestablished.

### 2.5 Prefectures

Prefectures coordinate multiple counties or a major urban jurisdiction. Their administration may cover regional transport, public works, revenue collection, inter-county disputes, and implementation of regional orders.

The 12 active prefectures and their seat cities are named in `world/GOLDEN_DRAGON_EMPIRE_ADMINISTRATIVE_ATLAS.md`. Their precise surveyed borders are unestablished; current prefects and reassigned regional officers are listed in `world/GOLDEN_DRAGON_EMPIRE_OFFICIALS.md`.

### 2.6 Counties

County circuits coordinate local civil administration, tax and population registers, courts of first instance where applicable, public works, and relations between settlements. They are broad service jurisdictions, not an additional layer of individual counties.

The atlas establishes six broad county circuits, each coordinating two prefectures; their hubs and responsibilities are listed in the atlas. Precise surveyed borders remain unestablished; current magistrates and reassigned circuit liaison officers are listed in `world/GOLDEN_DRAGON_EMPIRE_OFFICIALS.md`.

### 2.7 Cities, Towns, Townships, Districts, and Villages

- **Cities:** major population, trade, administrative, craft, or military centers. Their status as settlements does not automatically make them separate administrative tiers.
- **Towns and market settlements:** smaller urban places within a prefecture or service circuit. They do not imply a separate county tier; local administration follows the current atlas and any explicitly established appointment.
- **Townships / District Offices:** local offices that coordinate multiple villages or neighborhoods, or administer a defined urban district.
- **Villages / Neighborhoods:** the closest ordinary civil administration to residents, responsible for local registers, public notices, basic communal matters, and forwarding petitions or reports.
- **Household Register:** the lowest population-registration unit, recording a household and its recognized members. It is a registry unit, **not a separate government tier** and not proof that every household has an official ruler.

Village heads, neighborhood heads, clerks, and other local officers may be appointed or recognized through a procedure that will be documented later. Their cultivation level does not by itself determine their office.

## 3. Military Chain of Command — Separate from Civil Administration

```text
Emperor / Supreme Imperial Authority
└── Imperial High Command
    └── Regional Military Command
        └── Prefecture / Garrison Command
            └── Fortress or City Commander
                └── Unit Officers
                    └── Soldiers
```

This is the standard command model for imperial forces. Exact ranks, unit sizes, named commanders, and legal rules governing emergency authority remain to be defined.

- The Ministry of Military Affairs handles central administration and coordination; the High Command directs military operations.
- Regional governors and military commanders must coordinate but do not automatically replace one another.
- Baiyue's established identity as the Frontier Marches makes border garrisons and fortifications especially relevant there, but does not establish a specific garrison count or grant the civil governor direct military command.
- Clan troops, private guards, dojo forces, and other non-imperial forces are not automatically imperial units. Their legal status and relationship to the Empire must be established separately.

## 4. Justice, Oversight, and Accountability

- Civil officials are accountable through the applicable administrative chain and lawful oversight.
- Courts and legal offices operate under the Justice portfolio; exact court levels and appeal rules remain to be defined in a separate legal framework.
- The Imperial Oversight Agency may investigate suspected corruption or abuse, but its specific powers, appointment rules, and independence are not yet established.
- No officeholder is presumed honest, corrupt, loyal, disloyal, competent, or incompetent solely because of title or affiliation. Individual behavior must be established through canon or events.
- A noble, clan, dojo, or sect may possess social and political influence without automatically owning the territory or replacing its civil administration.

## 5. How Governance Information Is Stored

Use a modular storage pattern: one navigation index, one central reference per topic, and focused files for regions or individual institutions. This defines file organization only; it does not alter or duplicate world canon.

| Information type | Canonical storage |
|---|---|
| Core governance principles, hierarchy, ministries, and civil/military distinction | This file: `world/GOLDEN_DRAGON_EMPIRE_GOVERNANCE.md` |
| Seven regional identities and broad geographic relationships | `world/WORLD.md` and `world/MAP_AND_REGIONS.md` |
| Local settlements, jurisdiction, regional offices, local factions, and local NPC registry | The relevant `world/REGION_*.md` file |
| Central ministers, regional governors, all prefects and county magistrates: names, Spirit Realm, Martial Soul, background, motivation, and political stance | `world/GOLDEN_DRAGON_EMPIRE_OFFICIALS.md` |
| Full biography and established traits of an important official or recurring NPC requiring more detail | A dedicated `world/NPC_[NAME].md` profile linked from the regional registry |
| Clan, dojo, sect, and organization identity or relationships | `world/FACTIONS.md`; use a dedicated module when the institution requires detailed hierarchy or facilities |
| Confirmed historical appointments, reforms, wars, or past political events | `world/HISTORY.md` |
| Active or concluded persistent events and their ongoing world effects | `world/DYNAMIC_EVENTS.md`, following the owner-review workflow |
| Navigation, module links, and fetch triggers | `INDEX.md` |
| Human-facing project directory | `README.md` |

### 5.1 Record One Fact at Its Authoritative Source

Do not copy a full ministry description into every regional file. The central governance module defines the empire-wide structure; a regional file records only local implementation, confirmed officeholders, local jurisdictions, and relevant exceptions. Other files should link to the authoritative source instead of silently creating competing versions.

### 5.2 Required Fields for a Future Administrative Unit

When adding detail to an already registered prefecture, county, city, town, district, or village, record as much of the following as is confirmed:

- Official name and administrative type.
- Parent jurisdiction and governing authority.
- Confirmed seat, boundaries, and neighboring units, if known.
- Responsibilities and jurisdictional limits.
- Current officeholder and appointment source, if established.
- Confirmed settlements, public institutions, garrisons, and relevant factions.
- Revenue or economic role only when supported by the economy/world canon.
- Current status, known disputes, and links to relevant events/history.
- Canon source and status of each entry: **confirmed**, **provisional**, or **not established**.

Do not fill unknown fields with invented names, numbers, borders, or officeholders. Use `Belum ditetapkan` where appropriate.

### 5.3 Expansion Order

1. Treat the atlas as the single source for administrative names and totals.
2. Expand Longyuan's capital districts and local institutions in its regional module.
3. Expand the other six regional modules according to their established identities and recorded settlement totals.
4. Add individual NPC profiles when important officials are named.
5. When an administrative unit changes, update the atlas first, then synchronize the regional module and `world/MAP_AND_REGIONS.md`.

## 6. Canon Boundaries and Open Decisions

The following remain open unless established by a later owner-approved source:

- Exact surveyed boundaries and coordinates of prefectures, counties, and the imperial capital.
- Detailed capital districts and the current holders of central and regional offices.
- Ministers, council members, governors, prefects, county magistrates, and their current terms.
- Formal noble ranks, succession law, appointment procedures, taxation law, and civil-service examinations beyond the broad portfolio above.
- Detailed court hierarchy, appeal procedures, police/investigative authority, and emergency powers.
- Exact army ranks, unit sizes, garrison numbers, and relationships with clan or dojo forces.
- Any regional exception to the standard hierarchy.
- The Grand Martial Soul Awakening Hall's detailed internal hierarchy, staffing, and full reporting chain. Its centralized status and biennial public-awakening visits are settled; permanent regional or village branches are not established and must not be assumed. The central allocation principle and default formula are established; the central funding order still sets each period's total budget, priority weights, and funding dates. Specific penalties, investigator appointment rules, and appeal procedures remain open under the wider legal framework. Rules for fee waivers and subsidies require explicit authorization; the standard service charges and public token-only route are defined in `core/10_ECONOMY_SYSTEM.md` and `core/MARTIAL_SOUL_AWAKENING.md`.

The initial territorial names and totals are established by the administrative atlas, while exact geography and current officeholders remain separate facts. Do not use this module to overwrite established characters, clans, dojos, regional identities, or unrelated world lore. When a new fact conflicts with an existing official source, flag the conflict for owner review rather than silently rewriting either source.
