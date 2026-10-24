# Xuanling Realm — Economy System
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
5. Do not invent past money, transactions, price history, stock, or merchant costs. For a new session, use an explicitly recorded starting balance from the character snapshot when available. If it is absent, perform a one-time bootstrap draw to establish a concrete starting balance, record that result in the first session profile, and keep it fixed for the session. The draw must not be inferred from occupation, assets, background, or expected income, and it is not a claim about past earnings or transactions. Never reroll the balance on later turns. Once established, currency changes occur only through supported, recorded transactions.
6. When an exact price cannot be derived because an essential input is unknown, state the missing input or provide a clearly labeled estimate rather than pretending the value is fixed canon.
7. Keep the character profile's currency balances in the required compact format: `Currency (xuan/zun): 0xc | 0xs | 0xg | 0zj | 0az` only if a valid starting balance has not yet been established. For a new registered character, establish the one-time bootstrap balance before the first gameplay profile; then show the exact recorded balances.
8. The currency abbreviations defined in §1 are official. The character profile template must not duplicate their definitions.

## 8. Global Wealth Distribution

The world-level baseline total and its territorial and social-holder allocations are defined in `world/WEALTH_DISTRIBUTION.md`. Social classes, housing insecurity, poverty, and social mobility are defined in `world/SOCIAL_STRATIFICATION.md`. The territorial table and social-holder table are two views of the same 400.463.763.789.849 xg total; never add them together. Land, sea, air markets and auction circuits are transaction channels, not additional ownership shares. This module remains the authority for exchange rates, prices, scarcity, transactions, and character currency balances. The global wealth tables do not establish the exact balance of any named character or organization.
