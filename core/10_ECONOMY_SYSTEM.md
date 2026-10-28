# Merzkava Universe — Economy System
Status: Official system module. This document defines currency, item-quality tiers, regional pricing, distribution, seasonal scarcity, and local market adjustments.

## 1. Official Currency

Currency abbreviations are standardized as follows:

- `xc` = Xuan Copper
- `xs` = Xuan Silver
- `xg` = Xuan Gold
- `zj` = Zun Jade
- `az` = Ancient Zun

### Fixed exchange rates

- 100 Xuan Copper (`xc`) = 1 Xuan Silver (`xs`)
- 100 Xuan Silver (`xs`) = 1 Xuan Gold (`xg`)
- 1,000 Xuan Gold (`xg`) = 1 Zun Jade (`zj`)
- 10 Zun Jade (`zj`) = 1 Ancient Zun (`az`)

These are the official nominal exchange rates. Do not change them during ordinary gameplay unless the repository owner explicitly revises this module.

### Zun Jade

Zun Jade is an octagonal coin made from Heavenly Meteorite. Its surface bears intricate formations that emit white light. The material is so old and hard that people of the current era cannot engrave or rework its surface.

Zun Jade is currency, not a cultivation tool or a crafting material. It cannot be used as a cultivation tool or as material for creating an Artificial Artifact.

### Ancient Zun

Ancient Zun is a hexagonal coin made from an ancient heavenly material that appeared only once, when the Heaven Realm opened in the distant past. No metal can match its material, including metals originating beyond the world. Its intricate surface formations emit a purer white light than Zun Jade.

The original material cannot be reproduced from a known later source, and people of the current era cannot engrave, alter, or process its surface. Ancient Zun is currency only: it cannot be used as a cultivation tool or as material for creating an Artificial Artifact. Its nominal exchange rate remains 1 Ancient Zun = 10 Zun Jade.

Do not invent additional abilities, cultivation effects, crafting uses, or ways to manufacture either currency.

## 1.1 Martial Soul Awakening Routes, Charges, Subsidy, and Debt — Golden Dragon Empire

The Golden Dragon Empire recognizes two distinct routes. **Do not mix their charges.** The every-two-year public outreach route is an Imperial-subsidized service; the independent route is paid by the individual. These rules apply only to the Golden Dragon Empire unless another territory adopts its own rules.

### Route A — Independent Paid Awakening

An individual may seek an available awakening facility independently rather than wait for the next public village visit. The individual pays the full standard amount:

| Charge | Standard amount | Rule |
|---|---:|---|
| Awakening service fee | **3 xg, 25 xs** | Charged once per individual |
| Service tax | **8% of the service fee** | Applied only to the service fee; equals 26 xs |
| Documentation and official record | **15 xs** | One set per individual awakening |
| Official awakening proof token | **10 xs** | Issued after the result is recorded |

At 100 xs = 1 xg, the independent route costs **3 xg, 76 xs total** (376 xs). No additional charge may be invented without an established rule.

### Route B — Biennial Imperial Public Awakening

The Golden Dragon Empire's public awakening visit generally occurs once every two years after New Year, with assigned officials or cultivators visiting villages according to local quotas and schedules.

- The Imperial subsidy covers the **awakening service fee, the 8% service tax, and documentation/official record**. The recipient pays **only the 10 xs proof-token fee**.
- This is the defined subsidy for the biennial public route; it is not a discretionary waiver that must be separately approved by each village. The public program must account for the subsidized service and documentation costs against its authorized Imperial budget.
- If a person cannot afford the 10 xs token fee, the token may still be issued through an **external lender's advance**. The lender pays or advances the token charge to the issuing service, and the person receives a written debt note for the exact amount advanced. The lender is **not the Golden Dragon Empire, the Hall, or an Imperial ministry**.
- The Golden Dragon Empire does not own, guarantee, set, or collect the private loan, and the subsidy does not cover private-loan interest. The debt note must identify the actual external lender, principal, rate, repayment schedule, due dates, and consequences disclosed by that lender. Never invent a loan or debt unless the character actually accepts/enters it in play.
- Choose from external financial organizations that plausibly operate in the local area. The available lender and its terms are randomized from the locally available organizations; do not always choose the cheapest lender. Ordinary reputable lenders commonly charge **3%–8% simple annual interest**; an unlucky draw may result in a high-cost lender charging **12%–24% simple annual interest**. These are canon gameplay bands for this token-fee debt, not a claim that every lender in the world uses them. The selected organization's stated rate applies to that loan; do not reroll after seeing the rate.
- Interest is simple annual interest on the outstanding principal, unless the signed debt note explicitly establishes a different lawful calculation. Do not compound interest or add fees, collateral, penalties, or collection powers that are not specified in the actual debt note. For a note lasting less than a year, calculate proportionally by elapsed time.
- The loan principal is limited to the unpaid portion of the **10 xs token fee**. Do not turn a small token advance into an invented large loan, or include the subsidized service fee, tax, or documentation in the debt.

### Token, Records, and Employment Consequences

- The official proof token is a durable physical token linked to the individual's awakening record. It helps verify completion when applying for basic employment and education. It does not guarantee a job, admission, scholarship, income, or preferential treatment based on rarity.
- Documentation records the identity as provided/verified, awakening date and place, issuing authority, unique token/record identifier, and confirmed awakening result. Do not invent extra mandatory identity documents or a universal public database.
- Defaulting on the external loan can damage the person's credit reputation with that lender and, where lenders or employers lawfully share or check such records, make it much harder to obtain decent-paying work, secure future credit, and maintain an adequate standard of living. This is a serious socioeconomic consequence, **not** an automatic legal ban across the Golden Dragon Empire on employment or proof that every employer rejects the person.
- Exact default procedures, lawful collection methods, credit-sharing practices, and any additional fees depend on the actual external lender and applicable local rules. Do not invent imprisonment, confiscation, universal blacklisting, or automatic wage seizure.
- Do not charge the initial documentation or token fee twice for the same awakening. Replacement-token charges and correction fees are not established here.
- These costs, subsidies, and debts do not change rarity odds, mutation odds, or awakening outcomes. Paying more or using a city facility does not improve the result.
- Record each actual service charge, subsidy expenditure, token payment, loan advance, debt-note agreement, interest accrual, and repayment in the relevant financial ledger. Do not deduct money from a character's Wallet unless a real transaction occurred and was recorded. A debt note is a liability, not cash income; show it separately from Wallet balance.

### Unidentified item display and pricing

If an item's identity, exact type, or relevant properties have not yet been established by canon or the GM, display it as ``*Unknown*`` **membutuhkan appraisal untuk lebih pastinya** in Inventory, Equipment, loot, transactions, and player-facing item descriptions. Use this exact label consistently; do not substitute `???`, `Belum ditetapkan`, or another generic placeholder for the unidentified item itself. Do not infer its price, quality tier, scarcity, effects, or danger from this label. Do not finalize an item-specific price or transaction-dependent description until the required identity/details are established; ordinary market items with known identities continue to use normal pricing without mandatory appraisal. Follow `core/TIER_ASSESSMENT_AND_APPRAISAL.md` for identification and appraisal. After appraisal, update only the facts actually established by the ruling.

## 2. Nine Item-Quality Tiers

Quality tier and scarcity are separate variables. A high-quality item is not automatically scarce, and a common-quality item can become scarce due to seasonal conditions or disrupted supply.

The following multipliers are the default quality-price multipliers. Tier 1 is the reference tier:

| Quality Tier | General category | Price multiplier |
|---|---|---:|
| Tier 1 | Common: basic snacks, roadside food, ordinary herbs | ×1.00 |
| Tier 2 | Standard: modestly better than common quality | ×1.30 |
| Tier 3 | Good: above-average quality | ×1.70 |
| Tier 4 | Excellent: clearly superior quality or workmanship | ×2.20 |
| Tier 5 | Premium: high-quality goods | ×2.90 |
| Tier 6 | Rare-grade quality: high quality with limited production | ×3.80 |
| Tier 7 | Superior: exceptional quality | ×5.00 |
| Tier 8 | Peak quality: extraordinary quality | ×6.60 |
| Tier 9 | Legendary quality: highest category in this classification | ×8.50 |

These are economic quality categories, not Spirit Realms, Spirit Beast tiers, Spirit Ring tiers, or automatic measures of combat power. Tier 9 does not automatically mean the item is scarce or unique. For ordinary goods, select the fitting category from their clear description and ordinary market role; a missing formal tier record does not trigger specialist appraisal. Use `core/TIER_ASSESSMENT_AND_APPRAISAL.md` when a special, disputed, unidentified, or consequential classification cannot be resolved from canon and ordinary market evidence. A valid MAA appraisal is authoritative for the exact examined item, while a GM estimate must remain explicitly labeled as provisional. Never infer scarcity or price from tier alone.

An item’s base price is specific to its type, size, condition, freshness, function, and region of origin. Items of the same quality tier can have different base prices.

## 3. Regional Base Price

Every priced item should have:
1. An item identity and a reasonable quality category. For ordinary goods, use the fitting routine category (commonly Tier 1 for basic snacks, roadside food, and ordinary herbs) when the description supports it; do not require specialist appraisal.
2. A local base price for Tier 1 (or an explicitly documented base price for its actual tier).
3. A region of origin or a clearly identified local market.
4. Relevant seasonal supply conditions, if known and material.
5. A distribution route or distribution adjustment when traded outside its local market.

Specialist tier appraisal is reserved for unusual, disputed, unidentified, or mechanically/economically consequential goods whose classification cannot be settled from canon and ordinary market evidence. A missing formal appraisal record does not make the quality of every everyday item unknown.

The base price is the ordinary local price in the region where the item is sourced, under normal seasonal conditions and ordinary market conditions. Do not treat one region's price as the universal price for the entire world.

Example: Snow Herb has a Tier 1 normal local base price of 5 xc in the northern region.

## 4. Seasonal Scarcity

Seasonal scarcity changes the available supply of an item according to its source, growing or harvesting conditions, storage life, and season. Different items can respond differently to the same season. Do not apply one global seasonal effect to every item.

Default scarcity multipliers:

| Supply condition | Multiplier | Tier 1 example when base price is 5 xc |
|---|---:|---:|
| Normal supply | ×1.00 | 5 xc |
| Mild scarcity | ×1.40 | 7 xc |
| Moderate scarcity | ×1.80 | 9 xc |
| Severe scarcity | ×2.40 | 12 xc |
| Extreme scarcity | No fixed multiplier | Determine from actual remaining stock, available supply routes, and recorded market transactions |

For the first four states, the multiplier applies to the item's quality-adjusted base price. Extreme scarcity has no universal fixed price; the GM must use grounded local circumstances and avoid arbitrary price jumps.

### Disaster-Driven Scarcity

A recorded disaster can intensify scarcity when it demonstrably damages production, stored goods, harvests, transport routes, market access, or other parts of the supply chain. Use the following disaster-impact multiplier as a guide to the resulting scarcity of each affected item in the affected market:

| Disaster impact on the item's supply | Disaster scarcity multiplier |
|---|---:|
| Minor disruption | ×1.10–1.25 |
| Moderate disruption | ×1.30–1.60 |
| Major disruption | ×1.70–2.20 |
| Catastrophic disruption | ×2.30–3.00 |

These are bounded ranges, not automatic prices or a multiplier applied to every good in the region. Choose a value within the relevant range using recorded damage, remaining stock, duration, access to alternative suppliers, and the condition of supply routes. Use the lower end when reserves or alternate routes cushion the shock; use the upper end when the item is directly affected and substitutes are scarce. The catastrophic range is the maximum default disaster-driven scarcity multiplier; exceeding ×3.00 requires explicit owner-approved canon.

**Integration rule:** the pricing formula uses one effective Scarcity Multiplier. Assess the ordinary seasonal scarcity and the disaster's actual supply impact together, then select the effective multiplier that represents the resulting shortage. Do not multiply a seasonal scarcity multiplier by a disaster multiplier when both describe the same shortage. If clearly independent supply pressures affect the item, explain the evidence and account for their combined effect only once in the effective scarcity assessment.

Apply the disaster effect only to goods whose supply is affected. A flooded grain route may raise grain prices without raising the price of unrelated locally produced tools. Markets outside the disaster area may experience a smaller increase or none, depending on their inventories, routes, and suppliers. Do not apply the same disruption again as a second local-market or demand adjustment.

Disaster scarcity persists only while the recorded supply disruption remains consequential. It must ease as stock, production, and routes recover; do not reset prices instantly when the immediate disaster ends, and do not continue the increase after recovery is established. Record the event and its scope in `world/DYNAMIC_EVENTS.md` when its consequences meet that module's persistence criteria. The event record establishes the cause and ongoing status; this economy module determines the price calculation.

## 5. Distribution and Destination-Market Adjustment

Distribution adjustment includes reasonable transport and trade costs, such as caravan or ship fees, handling, storage, spoilage, tolls, insurance, and route risk. It can be positive or negative relative to the reference route, but the chosen adjustment must be grounded in the route and current conditions.

A destination market may also adjust prices because of:
- Local inventory surplus or shortage.
- Demand changes.
- Competition between merchants.
- Blocked routes, war, storms, piracy, or other supply disruptions.
- Alternative local or regional suppliers.

Do not assume that a farther region must always have the highest price. A safe, efficient sea route or abundant destination stock can make an item cheaper there than in another region.

## 5.1 Approved Inter-Power Passenger Transit Fares

The following owner-approved fares are fixed baseline prices for the named transport services. They are per passenger for the complete round trip, not one-way and not per aircraft.

| Service | Round-trip fare per passenger | Power source / service |
|---|---:|---|
| Tianhai Yunzhou long-distance liquefied-energy passenger aircraft | 25 xc | Tianhai Yunzhou-refined liquefied energy; dedicated corridors between Longyuan Sky Transit Terminal, Beiming Heartland Sky Transit Terminal, and Cangqiong Sky Transit Terminal |
| Comparable ordinary Qi-powered flying ship | 86 xc | Qi propulsion; ordinary inter-power flying-ship service |

Rules:
- The Tianhai Yunzhou energy-aircraft service has greater passenger capacity per journey than an ordinary Qi-powered flying ship.
- These prices apply to the established comparable inter-power passenger journey and the full return trip. Do not interpret them as one-way fares.
- The 25 xc fare is supported by Tianhai Yunzhou's specialized energy-refining and distribution advantage; it does not imply that other powers can freely manufacture the same fuel or operate compatible aircraft.
- Exact flight durations, schedules, seating capacity, cargo rates, premium classes, taxes, and disruption surcharges remain unestablished. Do not invent them as fixed canon.
- Refer to `world/REGION_TIANHAI_YUNZHOU.md`, `world/GEOGRAPHY_AND_TRAVEL.md`, and `world/ARTIFICIAL_ARTIFACTS.md` for route and technology details.

## 6. One Unified Item Pricing Formula

Use **one formula only** for ordinary item pricing. Do not calculate separate competing prices from different sections, and do not apply the same market factor twice.

`Final Price = (Tier 1 Base Price × Tier Multiplier × Condition Multiplier × Scarcity Multiplier × Demand Multiplier) + Distribution Adjustment + Local Market Adjustment`

Calculate in this order:

1. **Tier 1 Base Price** — the item's ordinary local price in its source market under normal seasonal and market conditions. Set it according to the item's identity, type, size, function, freshness, and region; it is not a universal price shared by every item.
2. **Tier Multiplier** — use the official quality multiplier in §2: Tier 1 ×1.00, Tier 2 ×1.30, Tier 3 ×1.70, Tier 4 ×2.20, Tier 5 ×2.90, Tier 6 ×3.80, Tier 7 ×5.00, Tier 8 ×6.60, Tier 9 ×8.50. Quality tier does not itself establish scarcity, rarity by quantity, or combat power.
3. **Condition Multiplier** — assess the actual item condition, not its tier: damaged but usable ×0.70; worn or partly impaired ×0.85; ordinary usable condition ×1.00; unusually well-preserved and verified ×1.10. Apply the category supported by inspection, canon, or appraisal. If the item is spoiled or unusable, do not treat it as an ordinary saleable item; follow the item's specific rules. Do not add a separate antique/historical premium under condition unless an official appraisal or item-specific canon supports it.
4. **Scarcity Multiplier** — use the effective scarcity for the relevant supply market under §4, including seasonal conditions and any documented disaster-driven supply disruption. For a disaster, use the impact bands in §4's **Disaster-Driven Scarcity** table (×1.10–1.25 minor, ×1.30–1.60 moderate, ×1.70–2.20 major, ×2.30–3.00 catastrophic) when supported by the actual effect on the item's supply. This is one effective multiplier, not an automatic extra factor: do not multiply seasonal and disaster values when they represent the same shortage. Extreme scarcity without a defensible fixed multiplier must be priced from remaining stock, actual supply routes, and recorded market conditions. Reduce or omit the effect when destination stock or alternative suppliers support that decision.
5. **Demand Multiplier** — assess current demand for this specific item in the relevant market: weak demand ×0.80; ordinary demand ×1.00; high demand ×1.20; very high demand ×1.50. An exceptional, time-limited demand spike may reach ×2.00 only when a concrete event or recorded market evidence supports it. Record the reason. Do not reuse demand already counted in another factor, and do not apply an exceptional multiplier merely because an item is valuable.
6. **Distribution Adjustment** — add the supported net cost or saving for the actual trade route, including transport, handling, storage, spoilage during transport, tolls, insurance, and route risk. It may be positive or negative.
7. **Local Market Adjustment** — add a documented destination-specific amount for factors not already represented above, such as merchant competition, a local inventory surplus, or a market-specific restriction. Do not count seasonal scarcity, demand, or transport costs again here if they have already been included in their dedicated factors.

If an essential input is unknown, identify it and give a clearly labeled provisional estimate only when the available evidence supports one. Do not fabricate a precise price. Round only at the final step to a usable amount in the official currency, then normalize denominations using the official exchange rates.

### Worked Example: Snow Herb in Different Supply Conditions

Assume Snow Herb has a Tier 1 normal local base price of 5 xc in the northern source market, Tier 1 quality (×1.00), ordinary usable condition (×1.00), ordinary demand (×1.00), and no additional local-market adjustment. Distribution adjustments are +4 xc to the Golden Dragon Empire and −1 xc to Tianhai Yunzhou because that route is unusually efficient and supply is abundant.

| Supply condition | North | Golden Dragon Empire | Tianhai Yunzhou |
|---|---:|---:|---:|
| Normal (×1.00) | 5 xc | 9 xc | 4 xc |
| Mild scarcity (×1.40) | 7 xc | 11 xc | 6 xc |
| Severe scarcity (×2.40) | 12 xc | 16 xc | 11 xc |

These are illustrative results under the stated assumptions. In actual play, use verified condition, demand, local inventory, alternative suppliers, and route conditions. The table does not establish universal prices for Snow Herb in every market.

## 7. Mandatory GM Rules

1. Check the economy module whenever buying, selling, bargaining over prices, appraising goods, or updating a character's currency.
2. Use the correct item tier, regional base price, seasonal scarcity, distribution route, and local market conditions. Do not use a universal price for all regions.
3. Keep quality tier separate from scarcity, rarity by quantity, item power, and cultivation rank.
4. Do not change the official exchange rates without an explicit canon revision.
5. Do not invent past money, transactions, price history, stock, or merchant costs. Starting Wallet assignment is part of the unified new-character profile bootstrap defined in `templates/CHARACTER_PROFILE_TEMPLATE.md`, not a separate economy-only process. For a new character with no explicit starting balance, choose one concrete, conservative estimate based on the character's stated background, living conditions, family circumstances, known work or livelihood, responsibilities, assets, and plausible local access to money. Mark it as a GM estimate in the initial profile notes; do not invent prior earnings or transactions to justify it. If the background is sparse, use the most reasonable conservative estimate rather than a random draw. An explicitly provided or already recorded starting balance always takes precedence and must never be recalculated. Normalize the chosen amount using official exchange rates, record it once in the character snapshot, and keep it fixed. Once established, currency changes occur only through supported, recorded transactions.
6. When an exact price cannot be derived because an essential input is unknown, state the missing input or provide a clearly labeled estimate rather than pretending the value is fixed canon.
7. Keep the character profile's currency balances in the required compact format: `Wallet (wealth): ... xc | ... xs | ... xg | ... zj | ... az`. For a new character, assign and save the Wallet as part of the same unified profile bootstrap described in `templates/CHARACTER_PROFILE_TEMPLATE.md`; do not run a separate money draw or save path. A valid explicit or saved balance must be copied exactly.
8. The currency abbreviations defined in §1 are official. The character profile template must not duplicate their definitions.


### Tier Verification for Goods and Appraisal Services

Before pricing or recording an item, check relevant canon and market information. For ordinary goods whose identity and quality are clear, assign the fitting routine economic category from §2 (for example, basic roadside food may be Tier 1) and calculate the price with the single formula in §6; a formal canon entry or MAA appraisal is not required for every everyday item. If a meaningful special classification is uncertain, follow `core/TIER_ASSESSMENT_AND_APPRAISAL.md`: use an existing canon classification, then a completed MAA ruling for that exact examined item, or a clearly labeled provisional GM prediction only when evidence is sufficient. If the classification is consequential and evidence is insufficient, leave that special classification unresolved and seek appraisal when practical; do not block an ordinary transaction solely because no specialist tier has been recorded. Do not invent appraisal fees, taxes, or service charges: use an established local price or resolve the service's actual terms before changing Wallet. A tier assessment does not itself create a purchase, sale, ownership transfer, or price.

### Mandatory Transaction Log / Ledger

Every character income and expense MUST be recorded in a continuous transaction log (ledger). This is mandatory for all money entering or leaving a character's Wallet, including purchases, sales, rewards, wages, fees, gifts, taxes, loans, repayments, refunds, and other supported transfers. Do not change the Wallet balance for a transaction until its cause and ledger entry are established.

Each ledger entry must record:
- **Date/time:** the in-world timestamp of the transaction, consistent with the session calendar.
- **Transaction:** a concise description and the reason it occurred.
- **Source / recipient:** who paid, received, sold, bought, or charged the amount, when known.
- **Direction:** income or expense.
- **Amount:** the exact amount and denomination paid or received.
- **Conversion:** when currency is exchanged, the denominations, official exchange rate, and normalized result.
- **Balance before:** the character's confirmed Wallet balance immediately before the transaction.
- **Balance after:** the exact Wallet balance immediately after the transaction, in all five official denominations.
- **Evidence / cause:** the gameplay action, event, agreement, or other valid basis authorizing the transaction.

Use this entry format:

`[Date/time] | [Income/Expense] | [Source/Recipient] | [Reason] | [Amount] | [Conversion, if any] | Before: [xc | xs | xg | zj | az] | After: [xc | xs | xg | zj | az] | Cause: [gameplay event/action]`

Ledger requirements:
1. Record every income and expense as its own entry when it occurs. Do not merge separate transactions into one vague total.
2. Keep entries chronological and append-only. Never silently delete, rewrite, or invent historical transactions. If a genuine error is found, preserve the original entry and add a clearly identified correction entry that explains the error and its effect on the balance.
3. Verify that each entry's opening balance matches the previous confirmed closing balance, and calculate the closing balance using the official exchange rates. The Wallet displayed in the character profile must match the latest verified ledger balance.
4. The one-time bootstrap balance is an opening balance, not a fictional income transaction. Record it as the ledger's opening-balance entry with its source (character snapshot, valid Authority instruction, or one-time bootstrap draw); do not invent past earnings to explain it.
5. For a continuing session, resume from the latest available gameplay profile and ledger, then append only supported transactions that occurred afterward. Never reroll the opening balance or reconstruct missing transactions from guesses.
6. If a previous ledger is unavailable or a balance discrepancy cannot be resolved from recorded evidence, state the gap and use the latest verifiable balance as the reconciliation point. Do not fabricate entries or claim the ledger is complete beyond the evidence available.
7. The ledger is the transaction audit trail; it does not replace the Wallet field in the character profile and does not create a separate Wallet module. Maintain it in the ongoing session record/history so it can be continued and checked across turns. Do not claim that it has been permanently saved to GitHub unless the repository write was actually completed and verified.
8. Before finalizing any gameplay response involving money, verify that the transaction has a ledger entry, the balance calculation is correct, and the displayed Wallet matches the ledger. If the transaction cannot be supported or reconciled, do not invent a result.


### Mandatory Item Movement Log / Ledger

Every change to a character's item holdings MUST be recorded in a continuous item log/ledger, alongside the relevant gameplay history. This applies to all items and stackable materials, including equipment, consumables, currency-like objects treated as items, crafting materials, loot, quest items, relics, artifacts, and other inventory contents. Record changes to building Assets separately from carried Inventory when the item or property belongs there.

Record each event that changes ownership, quantity, condition, or location, including acquisition, purchase, reward, loot, gift, trade, sale, use, consumption, crafting, dismantling, transfer, storage, retrieval, loss, theft, breakage, destruction, or disposal. Do not change Inventory, Equipment, or Assets until the event has a valid cause and its log entry can be established.

Each item-ledger entry must record:
- **Date/time:** the in-world timestamp consistent with the session calendar.
- **Item:** exact item name and, where relevant, quality/tier, variant, unique identifier, durability/condition, or other distinguishing traits.
- **Action:** acquired, removed, used, consumed, crafted, transferred, damaged, destroyed, or other precise change.
- **Quantity:** exact amount added or removed, including unit or stack size where relevant.
- **Source / destination:** seller, buyer, giver, recipient, loot source, storage location, crafting result, or other known origin/destination.
- **Reason / cause:** the gameplay action, event, agreement, recipe, or other valid basis for the change.
- **Quantity before and after:** the character's confirmed quantity immediately before and after the event; for unique items, record the state/condition before and after instead of inventing stack counts.
- **Related transaction:** link or cross-reference the matching money-ledger entry whenever the item movement involves payment, sale, refund, fee, or another Wallet transaction. Record the matching entry ID/time or explicitly state that no money changed hands.
- **Resulting location/state:** Inventory, Equipment, Assets, storage, another holder, consumed, destroyed, or another established state.

Use this entry format:

`[Date/time] | [Item + distinguishing details] | [Action] | [Quantity: +/− amount] | [Source/Destination] | [Reason/Cause] | Before: [quantity/state] | After: [quantity/state] | Money ledger: [entry reference / no money changed hands]`

Item-ledger requirements:
1. Record each distinct item movement or state-changing event as its own chronological entry. Do not merge unrelated item changes into a vague summary.
2. Keep the ledger append-only. Never silently delete, rewrite, or invent past item movements. If an error is confirmed, preserve the original entry and append a clearly identified correction with its reason and effect.
3. Each item's opening quantity/state must match the previous confirmed closing quantity/state. The current Inventory, Equipment, and relevant Assets shown in the character profile must match the latest verified item ledger.
4. Starting items come from the applicable character snapshot, valid Authority instruction, or established session state. Record them as an opening inventory baseline, not as fabricated acquisitions during gameplay.
5. For a continuing session, resume from the latest available gameplay profile and item ledger, then append only supported changes that occurred afterward. Never reconstruct missing item history from guesses.
6. If an item ledger is unavailable or a discrepancy cannot be resolved from recorded evidence, state the gap and use the latest verifiable inventory/profile as the reconciliation point. Do not fabricate missing transactions or claim the ledger is complete beyond available evidence.
7. Money and item records must cross-reference one another when part of the same exchange. A purchase or sale is not consistent until both the money movement and the item movement are recorded and reconciled. For crafting, record the inputs consumed and outputs created, and verify the relevant crafting rules before changing quantities.
8. An item being used, consumed, equipped, damaged, or moved does not automatically mean it is destroyed or removed permanently; record only the change supported by the relevant mechanics and event.
9. The item ledger is an audit trail, not a replacement for the character profile's Inventory, Equipment, or Assets fields and not authorization to create a separate profile field or module. Maintain it in the ongoing session record/history so it can be continued and checked across turns.
10. Before finalizing any gameplay response that changes items, verify the item-ledger entries, quantities and resulting states, related money-ledger entries, and displayed profile. Do not claim the ledger has been permanently saved to GitHub unless the repository write was actually completed and verified.

### Unified Ledger, Natural Change Markers, and Immersive Narration

The money and item ledgers above are mandatory audit records. The same reporting standard applies to every actual Satiety change and every tracked change to Equipment, loot, or Assets. Keep the full chronological, append-only audit trail in ongoing session history; the visible block is a compact player-facing summary, not proof of a GitHub write.

**Required response order:** immersive in-world narration and relevant active dialogue → natural in-narrative report of each verified change with before → signed change → after → inline-code `Log tercatat!` exactly once after the report → one combined visible `LEDGER LOG` → reconciled character profile. A transaction must be described naturally in the narration itself, not hidden in the ledger alone. During passive player conversation, keep the scene alive with relevant sensory detail, active NPC dialogue/reactions, and local activity supported by canon, location, time, NPC knowledge, and established agendas. Do not force random events, invent facts, or take control of the player's character.

**Inline change-marker convention:** place the marker inside the natural narrative/change-report sentence:
- **🝰 MASUK · [item/uang + jumlah]** ⧟ ``*<Tier/Grade/Rarity/Quality/Unknown>*`` [keterangan jika relevan] for a verified increase to the player's holdings/balance.
- **🝰 KELUAR · [item/uang + jumlah]** ⧟ ``*<Tier/Grade/Rarity/Quality/Unknown>*`` [keterangan jika relevan] for a verified decrease, expense, consumed item, outgoing transfer, loss, or sale.
- For an exchange, show separate MASUK and KELUAR markers in the same narrative report, then use one combined ledger block. Use `🝰 PERUBAHAN` only for a verified condition/location change that is neither an inflow nor an outflow.
- Include only supported, relevant attributes. For an unidentified item, use the exact name ``*Unknown*`` **membutuhkan appraisal untuk lebih pastinya**; never invent its tier, grade, rarity, quality, price, or function. Ordinary goods with clear identities may use routine market categories; missing specialist appraisal alone does not make an everyday item's identity unknown.
- After the complete verified change sentence, write **`Log tercatat!`** exactly once. It confirms a session-ledger entry, not a GitHub write. Do not add another confirmation line.

**Example pattern only (replace all values with verified session state):** “Pedagang itu menerima 23 xc dan menyerahkan satu roti. Wallet: [saldo awal] → −23 xc → [saldo akhir]; Inventory: 0 → +1 roti → 1. **🝰 KELUAR · 23 xc** ⧟ ``*Xuan Copper*`` · **🝰 MASUK · 1× roti** ⧟ ``*Tier 1*`` / ``*kualitas rutin*``. **`Log tercatat!`**” For Satiety changes, include before → delta → after and the cause/duration or consumed item when relevant. If Satiety does not change, still state its current value and why; do not create a ledger solely for an unchanged value.

Use this mobile-friendly visible format; include only affected fields and preserve before → change → after:

```text
╭─ LEDGER LOG · #[ID]
│ Peristiwa/Aksi: [aksi/peristiwa penyebab perubahan]
│ [Waktu] · [Berhasil/Gagal/Dibatalkan]
│ 🝰 Item/Equipment/Loot/Aset: [MASUK/KELUAR · nama · ×jumlah · ⧟ ``*tier/grade/rarity/quality/Unknown*`` [keterangan jika relevan] · sumber/tujuan · awal → perubahan → akhir]
│ 🝰 Uang: [MASUK/KELUAR · sumber/penerima · jumlah · saldo awal → perubahan bersih → saldo akhir · kembalian jika ada]
│ Satiety: [awal → ±delta → akhir · penyebab/kategori/durasi jika relevan]
╰─
```

For multiple item movements, use one concise subentry per distinct movement under the same event ID. For a payment with a larger denomination, reconcile amount handed over, price, change returned, and net expense. A purchase followed by immediate consumption is one combined event and one visible log, not separate logs for payment, Inventory, and Satiety.

Audit rules:
1. Record each distinct money transaction and item movement as its own chronological, append-only audit entry, even when linked under one visible event. Cross-reference related money/item entries.
2. Show one combined visible ledger for all state changes from the same action/event. Wallet, Inventory, Equipment, Assets, and Satiety must match the verified closing state.
3. If a transaction fails or is cancelled, do not record money/item changes that did not occur. Record only the verified portion of partial payment, deposit, debt, barter, refund, or transfer.
4. If no tracked state changed, omit both `Log tercatat!` and the visible ledger. Satiety must still be mentioned after the latest activity, even if unchanged.
5. Keep full Satiety calculation details in session history: cause, duration, activity category, every applied multiplier, calculation, before, signed change, and after. The visible log may stay concise.
6. Before sending, reconcile the cause, money and item entries, quantities, currency conversion/change, relevant item quality/tier, Satiety, and resulting profile. If prior ledger history is missing or truncated, disclose the gap and reconcile from the latest verifiable state without inventing history.
7. The ledger is not a profile field and does not replace the character profile. Do not claim permanent GitHub persistence unless a repository write was completed and verified.

## 8. Global Wealth Distribution

The world-level baseline total and its territorial and social-holder allocations are defined in `world/WEALTH_DISTRIBUTION.md`. Social classes, housing insecurity, poverty, and social mobility are defined in `world/SOCIAL_STRATIFICATION.md`. The territorial table and social-holder table are two views of the same 400.463.763.789.849 xg total; never add them together. Land, sea, air markets and auction circuits are transaction channels, not additional ownership shares. This module remains the authority for exchange rates, prices, scarcity, transactions, and character currency balances. The global wealth tables do not establish the exact balance of any named character or organization.
