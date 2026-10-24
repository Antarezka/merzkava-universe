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

The Empire's public awakening visit generally occurs once every two years after New Year, with assigned officials or cultivators visiting villages according to local quotas and schedules.

- The Imperial subsidy covers the **awakening service fee, the 8% service tax, and documentation/official record**. The recipient pays **only the 10 xs proof-token fee**.
- This is the defined subsidy for the biennial public route; it is not a discretionary waiver that must be separately approved by each village. The public program must account for the subsidized service and documentation costs against its authorized Imperial budget.
- If a person cannot afford the 10 xs token fee, the token may still be issued through an **external lender's advance**. The lender pays or advances the token charge to the issuing service, and the person receives a written debt note for the exact amount advanced. The lender is **not the Empire, the Hall, or an Imperial ministry**.
- The Empire does not own, guarantee, set, or collect the private loan, and the subsidy does not cover private-loan interest. The debt note must identify the actual external lender, principal, rate, repayment schedule, due dates, and consequences disclosed by that lender. Never invent a loan or debt unless the character actually accepts/enters it in play.
- Choose from external financial organizations that plausibly operate in the local area. The available lender and its terms are randomized from the locally available organizations; do not always choose the cheapest lender. Ordinary reputable lenders commonly charge **3%–8% simple annual interest**; an unlucky draw may result in a high-cost lender charging **12%–24% simple annual interest**. These are canon gameplay bands for this token-fee debt, not a claim that every lender in the world uses them. The selected organization's stated rate applies to that loan; do not reroll after seeing the rate.
- Interest is simple annual interest on the outstanding principal, unless the signed debt note explicitly establishes a different lawful calculation. Do not compound interest or add fees, collateral, penalties, or collection powers that are not specified in the actual debt note. For a note lasting less than a year, calculate proportionally by elapsed time.
- The loan principal is limited to the unpaid portion of the **10 xs token fee**. Do not turn a small token advance into an invented large loan, or include the subsidized service fee, tax, or documentation in the debt.

### Token, Records, and Employment Consequences

- The official proof token is a durable physical token linked to the individual's awakening record. It helps verify completion when applying for basic employment and education. It does not guarantee a job, admission, scholarship, income, or preferential treatment based on rarity.
- Documentation records the identity as provided/verified, awakening date and place, issuing authority, unique token/record identifier, and confirmed awakening result. Do not invent extra mandatory identity documents or a universal public database.
- Defaulting on the external loan can damage the person's credit reputation with that lender and, where lenders or employers lawfully share or check such records, make it much harder to obtain decent-paying work, secure future credit, and maintain an adequate standard of living. This is a serious socioeconomic consequence, **not** an automatic Empire-wide legal ban on employment or proof that every employer rejects the person.
- Exact default procedures, lawful collection methods, credit-sharing practices, and any additional fees depend on the actual external lender and applicable local rules. Do not invent imprisonment, confiscation, universal blacklisting, or automatic wage seizure.
- Do not charge the initial documentation or token fee twice for the same awakening. Replacement-token charges and correction fees are not established here.
- These costs, subsidies, and debts do not change rarity odds, mutation odds, or awakening outcomes. Paying more or using a city facility does not improve the result.
- Record each actual service charge, subsidy expenditure, token payment, loan advance, debt-note agreement, interest accrual, and repayment in the relevant financial ledger. Do not deduct money from a character's Wallet unless a real transaction occurred and was recorded. A debt note is a liability, not cash income; show it separately from Wallet balance.

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

These are economic quality categories, not cultivation realms, Spirit Beast tiers, Spirit Ring tiers, or automatic measures of combat power. Tier 9 does not automatically mean the item is scarce or unique.

An item’s base price is specific to its type, size, condition, freshness, function, and region of origin. Items of the same quality tier can have different base prices.

## 3. Regional Base Price

Every priced item should have:
1. An item identity and quality tier.
2. A base price for Tier 1 (or an explicitly documented base price for its actual tier).
3. A region of origin or a clearly identified local market.
4. Relevant seasonal supply conditions, if known.
5. A distribution route or distribution adjustment when traded outside its local market.

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

Scarcity is evaluated for the relevant supply market. If a source region suffers a shortage, imported goods can carry a higher price. However, a destination with substantial old stock or alternative suppliers may experience a smaller increase or no increase at all. Apply a documented local-market adjustment when such evidence supports it.

## 5. Distribution and Destination-Market Adjustment

Distribution adjustment includes reasonable transport and trade costs, such as caravan or ship fees, handling, storage, spoilage, tolls, insurance, and route risk. It can be positive or negative relative to the reference route, but the chosen adjustment must be grounded in the route and current conditions.

A destination market may also adjust prices because of:
- Local inventory surplus or shortage.
- Demand changes.
- Competition between merchants.
- Blocked routes, war, storms, piracy, or other supply disruptions.
- Alternative local or regional suppliers.

Do not assume that a farther region must always have the highest price. A safe, efficient sea route or abundant destination stock can make an item cheaper there than in another region.

## 6. Unified Pricing Formula

Use the following formula when the necessary inputs are available:

`Final Price = (Base Price × Quality Multiplier × Scarcity Multiplier) + Distribution Adjustment + Local Market Adjustment`

Where:
- **Base Price** is the normal Tier 1 local price for the item in its source market.
- **Quality Multiplier** is the multiplier for the item's tier.
- **Scarcity Multiplier** represents the relevant shortage affecting the item's available supply.
- **Distribution Adjustment** accounts for the actual trade route and delivery costs.
- **Local Market Adjustment** reflects supported destination-specific inventory, demand, and competition effects. It can be positive or negative.

Use a scarcity multiplier of ×1.00 when supply is normal. If the destination has enough stored stock or alternative supply to insulate it from source-region scarcity, reduce or omit the scarcity effect only when the local market evidence supports that decision.

### Example: Snow Herb sold in three regions

Assume:
- Tier 1 normal local base price in the North = 5 xc.
- Normal distribution adjustment to the Golden Dragon Empire = +4 xc.
- Normal distribution adjustment to Tianhai Yunzhou = −1 xc because its route is unusually efficient and supply is abundant.
- No extra local-market adjustment.

| Market condition | North | Golden Dragon Empire | Tianhai Yunzhou |
|---|---:|---:|---:|
| Normal | 5 xc | 9 xc | 4 xc |
| Mild scarcity | 7 xc | 11 xc | 6 xc |
| Severe scarcity | 12 xc | 16 xc | 11 xc |

The destination examples carry the same source-scarcity surcharge for illustration. In actual play, local stock, alternative suppliers, demand, and route conditions may change the destination-market adjustment.

## 7. Mandatory GM Rules

1. Check the economy module whenever buying, selling, bargaining over prices, appraising goods, or updating a character's currency.
2. Use the correct item tier, regional base price, seasonal scarcity, distribution route, and local market conditions. Do not use a universal price for all regions.
3. Keep quality tier separate from scarcity, rarity by quantity, item power, and cultivation rank.
4. Do not change the official exchange rates without an explicit canon revision.
5. Do not invent past money, transactions, price history, stock, or merchant costs. For a new session, use an explicitly recorded starting balance from the character snapshot when available. If it is absent, perform a one-time bootstrap draw using this default range: 0–9 xg, 0–99 xs, and 0–99 xc, with 0 zj and 0 az unless an explicit canon rule establishes otherwise. Convert/normalize the draw using the official exchange rates, record the concrete result in the first session profile, and keep it fixed for the session. The draw must not be inferred from occupation, assets, background, or expected income, and it is not a claim about past earnings or transactions. Never reroll the balance on later turns. Once established, currency changes occur only through supported, recorded transactions.
6. When an exact price cannot be derived because an essential input is unknown, state the missing input or provide a clearly labeled estimate rather than pretending the value is fixed canon.
7. Keep the character profile's currency balances in the required compact format: `Wallet (wealth): 0 xc | 0 xs | 0 xg | 0 zj | 0 az` only if a valid starting balance has not yet been established. For a new registered character, establish the one-time bootstrap balance before the first gameplay profile; then show the exact recorded balances.
8. The currency abbreviations defined in §1 are official. The character profile template must not duplicate their definitions.


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

## 8. Global Wealth Distribution

The world-level baseline total and its territorial and social-holder allocations are defined in `world/WEALTH_DISTRIBUTION.md`. Social classes, housing insecurity, poverty, and social mobility are defined in `world/SOCIAL_STRATIFICATION.md`. The territorial table and social-holder table are two views of the same 400.463.763.789.849 xg total; never add them together. Land, sea, air markets and auction circuits are transaction channels, not additional ownership shares. This module remains the authority for exchange rates, prices, scarcity, transactions, and character currency balances. The global wealth tables do not establish the exact balance of any named character or organization.
