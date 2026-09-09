# CARIB roadmap

## Phase 1 — in progress
- [x] Satellite-style Caribbean map (clean geography, proper wheel zoom/pan)
- [x] Market UI overhaul with commodity icons
- [x] New game creation: captain name, vessel name, vessel choice
- [x] Start with no crew, no coin, debt scaled to the chosen vessel; weekly interest
- [x] Player stats (navigation, negotiation, combat, leadership, crafting) + XP
- [x] Crew members: nationality, age, role, skill, potential grade, wages, XP
- [x] Port recruiting pool (size/quality by port population), refreshed weekly
- [x] Port quest board: delivery, courier, bounty — advance payment on accept
- [x] Banner stats (player + crew)
- [x] Save schema reset

## Phase 2 — next
- [ ] Ship part customisation (hull, sails, guns, hold fittings) bought/salvaged
- [ ] Port access gated by reputation tier
- [ ] Port fortification + raiding, port prosperity damage/recovery
- [ ] Pirate banners roaming the map; bounties from hated factions
- [ ] Faction war state affecting ports and ships

## Phase 3
- [ ] Investments: buildings producing manufactured goods, 1–5 stars, assigned workers
- [ ] Player warehouses per port, transfer to ship / sell to trader
- [ ] Second ships with crew captains, 50% earnings share

## Phase 2 (in progress)
- [x] Regional charts orientation fixed (Mercator no longer mirrored)
- [x] Flag designer at game start (3 colours + charge), house colours shown on ships, fleet and header
- [x] Ship allegiance / national ensign per vessel
- [x] Ship deck plan with 7 upgradeable component slots and nation-locked parts
- [x] Reputation-gated diplomacy, crown trade licences enforced in the market
- [ ] Fortifications, raiding, pirate fleets and faction wars

## Phase A (done)
- Bounded map panning (pan only after zoom), fog/terra incognita edges, swell, soundings, sea names
- Weekly port events with market/prosperity/risk effects
- Port dossier: generated 2D harbour prospect, event notice, remote intel (wanting/surplus), fortification estimate, shore actions when docked
- Tavern (rumours, gossip, contracts, recruiting) and Shipwright's Yard (repairs, provisions, chandlery, hulls)
- HUD: date, gold, debt, supplies, condition, morale, ETA + prominent Continue button
- Docked repairs consume timber/pitch/canvas/cordage; sailing wear mitigated by crafting

## Next
- Deep ship-management: components as physical inventory (buy/store/install/remove/transfer), condition per component, crew stations
- Cargo physics: containers, preservation, security, legal restrictions, manifests, insurance
- Fortifications, raiding, pirate fleets, faction wars, combat

## Ship & crew rebuild (done)
- Five archetypes (Sloop/Brigantine/Brig/Galleon/Frigate) with hull, firepower, maneuverability, scouting, cargo, speed, crew capacity and component slots.
- Six ship regions with physical components, levels 1-5, install/upgrade/strip at a yard.
- Eight crew positions and eight skills; each post requires its quarter to be built before a man can be signed.
- Next: cargo physics (containers, preservation, livestock), component condition/wear, fortifications, pirate fleets, faction wars.

- [x] Skill rename (Navigation/Scouting), 20-99 skills, 30-99 hidden potential, per-skill XP with youth and first-mate bonuses
- [x] Ship's articles (crew share of prize gold and XP), per-man morale and health, desertion and death
- [x] Supplies/medicine/salvage drawn from real cargo, consumed at sea; cook, surgeon and carpenter work their stores
- [x] Ship schematic with clickable regions


## Sailing, marks and encounters (done)
- [x] All 630 port-pair routes audited land-free (`bun run scripts/audit-routes.ts`); routing now gives the coast a berth where there is sea room
- [x] Passage brief popup on setting course: position, sketched water road, stores needed, ETA, dangers
- [x] Rudder button rolls down a searchable list of every harbour, nearest first
- [x] Living sea: wrecks, flotsam, merchantmen, pirates, patrols, squalls and rumours sown daily at coordinates, fading with time
- [x] Scouting bubble round the ship reveals marks; running one close aboard pauses the passage with a choice (ignore, investigate, flee, fight, parley)
- [x] Harbour report pops up over the left of the chart on hover; clicking opens the passage brief
- [ ] Deeper combat: gun duels, boarding, prize crews, fortification bombardment

## Standing, Reputation and Infamy (done)
- [x] Courier goods sealed as QUEST cargo (no sale, no supplies/medicine/salvage)
- [x] Journal quest log: destination, deadline, track-on-chart, deliver, abandon
- [x] Abandon keeps the goods untagged and costs standing; deadline forfeits after a grace period at a steeper cost
- [x] Port standing (-100..100) per port: trade, tavern time, quests; half of faction standing applied; bans and fines; marginal price, recruit and quest effects
- [x] Faction standing (-100..100): independent captains start -20 (culture/faith mitigate), pirates -50; hostility at -50; contracts locked behind service permits
- [x] Banner Reputation and Infamy: 20 levels each (wood/copper/silver/gold); +2 faction standing per Reputation level, +2 pirate standing per Infamy level
- [x] Pirate Black Quests: illegal couriers paying more, goods sealed as CONTRABAND, inspections at sea and on docking with fines and forfeiture
- [ ] At-sea inspection encounters (guarda costa pulling over contraband runners)

## CARIB final-changes queue (from 2026-09-06 brief)
Done: crew wage/fee curve + rarer, fewer recruits; debt 5% monthly + repayment slider;
port levels 1-5 (+chart dot size); Spain yellow / England red; Denmark removed;
starting-purse slider; combat 1x/2x/3x; mock combat fleet size.

Open:
- Faction flags (historical, rectangular) + drape on port view; per-faction tariff/opinion rules.
- Pirate: black flag, -70 start, no permits, hidden generated ports (Caribbean lv2 capital, 13 Colonies lv1, Africa lv1).
- Port level effects on quests, market stock, shipyard part quality.
- Combat visuals: realistic top-down hulls, no overlap, cascading volleys, lively seas/time of day.
- Port combat (Defensiveness stat, Pillaged modifier, capture rules).
- World fleets: AI ships/captains per faction, patrols, scout-bubble engagements, 7-day map battles, yearly replenishment.
- Independent merchant ships (5, good/bad AI, yearly top-up).
- Crew/part significance rebalance; speed vs manoeuvrability by hull size.
- Shipyard: naval goods market, component market, schematic editing moved here.
- Component crafting with recipes + Carpenter's Workshop.
- Faction-to-faction relations web, monthly events, status-quo drift, war/alliance.
- Fleet orders (free merchant / follow), letters of marque.
- Capital buildings: Lisbon academy, Amsterdam Wisselbank, London Royal Dockyard, Nantes exchange, Sevilla Casa.
- Tavern/shipyard/market header paintings; permits moved to capital diplomacy.
- More quests/contracts incl. quest-generated map battles; richer map encounters.

## Faction batch (done this pass)
- Rectangular historical faction flags (`FactionFlag`), draped over every port view/painting.
- Monthly crown edicts wired into market buy prices (`policy.ts`): Spanish bullion +25% and rotating agricultural tariff, Portuguese agricultural tariff / naval −10% / investments +25%, English rotating manufactured break / military-naval +25% / investments −15%, French rotating luxury-alcohol tariff.
- Opinion rules: Spanish culture/faith penalties, Portuguese faith, French culture, English infamy penalty, French prestige bonus.
- Pirate starting standing −70. Dutch start: no permits, 8% monthly interest.
- Three hidden pirate havens generated per save (Caribbean level 2 capital, 13 Colonies, Africa) with own names, markets, painting fallback; found by the scouting bubble; excluded from every port list until found.
- Faction-to-faction relation web with historical status quo, monthly dispatch events, annual pull back to the status quo, war at −50 / allied at +50; circular relations grid in Diplomacy.
- Dev save option at character creation + Dev tab (gold, debt, prestige, infamy, reveal, permits); old debug button removed.

## Still queued (not built yet)
- World fleets: AI ships/captains per faction, patrols, AI-vs-AI combat over 7 days, yearly replenishment.
- Independent merchant ships (5 at a time, good/bad AI, bankruptcy, yearly respawn).
- Port combat (fort simulation, Defensiveness, pillaged modifier, level ≤2 change of control).
- Combat visual overhaul: ship icons, no overlap, cascading cannon-ball volleys, 8-12 battle map presets with weather/time of day.
- Shipyard: naval/military goods counter, component market, refit tab, quality by port level; Carpenter's Workshop crafting recipes.
- Capital buildings (Lisbon academy, Wisselbank, Royal Dockyard, Nantes exchange, Casa de Contratación) and capital-only faction diplomacy.
- Letters of marque at +50, sailing under a faction flag; fleet orders (follow / free merchant).
- Stronger crew-stat and component effects on ship stats; speed vs manoeuvrability split.
- Oil-painting headers for tavern, market and shipyard; more quest types.

## Batch: port size, crew boons, yard and finance (done)
- [x] Dev "reveal" cheat implemented; chart and rudder list refresh the moment a black harbour is found
- [x] Port level (1-5) now drives quest count and pay, market stock depth, and the best mark of work a yard can do
- [x] Crew skills lift ship stats at skill ÷ 2.25% on top of base and fitted parts; muster registered on every state change
- [x] Archetype speed/handling/eyes rebalanced (sloop nimble and slow, galleon fast and clumsy, frigate the hunter)
- [x] Captain's post takes no wage
- [x] Shipyard sells and raises components in the yard itself; Finance no longer lends coin or sells ventures
- [ ] Next: world fleets, independent merchants, port combat, combat visual overhaul, crafting recipes, capital buildings, letters of marque, painted headers, more quests

## Battlegrounds (done)
- 12 pregenerated tile battlegrounds (deep/shoal/land), named after Atlantic waters
- Every action is fought on one, drawn in chart style; hulls may not cross land
- Fort type (`BattleShip.fort`) and star-fort rendering in place; stationary, fires only
- State fields added: `CombatState.portId`, `npcShips`, `npcFleets`, `npcBattles`, `portControl`, `pillaged`

## Next
- [ ] Port assault: open combat against a harbour, Defensiveness from level/fortification, pillage + control change
- [ ] World fleets: 5 ships per crown, captains/crews/banners, patrols, AI actions over 7 days, annual replenishment
- [ ] Independent merchants: 5 free traders trading in the background, good/bad wits, bankruptcy and replenishment
- [ ] Fleet > Factions list with pirate/scouting visibility gating; chart markers for NPC ships and battles

## World batch (done this pass)
- Mock actions now draw a fresh battleground, light and wind every time.
- Port combat: `fortStats` (Defensiveness / firepower / guns by port level), a stationary
  fort combatant, "Stand in and engage the batteries" from the harbour dossier,
  and sacking rules (level 3+ pillaged 14 days; level ≤2 pillaged 7 days and changes hands).
- `sim/world.ts`: 6 crown squadrons of 5 archetypes with generated captains/crew/banners/
  components (best officer to heaviest hull), 5 free traders with 1,000 gold and good/poor
  trading wits, daily movement, scout-bubble engagements, 7-day actions resolved in the
  journal, port assaults by AI, bankruptcy, yearly replenishment.
- Chart shows other men's hulls inside the player's glass and week-long actions.
- Fleet > Faction squadrons list (pirates hidden unless the player flies the black),
  details only after a ship has been seen.

## Still open
- Ship-following / free-merchant orders for the player's own fleet, joining others' battles.
- Component crafting recipes + Carpenter's Workshop; capital buildings; letters of marque.
