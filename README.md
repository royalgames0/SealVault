# SEAL VAULT

A single-file, offline, pixel-art arcade game. You are a seal. So is everyone else.

Open `index.html` in any modern browser — that's the whole install. No server, no build
step, no external assets. Every sprite, sound and loot table is generated in code.

## The loop

Wander the ice-floe village, dive into a rotating **vault** minigame, come back with fish,
XP and loot rolls, spend it on gear and cosmetics, then prestige when the season maxes out.

## What's in it

**11 minigames**, five of which rotate into the vault gate each day (rerollable for fish):

| Vault | Type |
| --- | --- |
| Fish Dash | endless swim, dodge nets/orcas/rocks |
| Ice Fishing | tap-timing hook, push-your-luck chains |
| Floe Survival | wave arena, auto-attack, orca boss every 10 waves |
| Pearl Match | match-3 bonus room, pure loot |
| Belly Slide Race | rhythm slide, jump gaps, trick off ramps |
| Clam Dig | dig-timing on the beach, crabs and fake-outs |
| Synchronized Swim | four-lane rhythm routine, graded S–D |
| Iceberg Balance | physics teeter on a shrinking berg |
| Seagull Chase | swat gulls raiding your fish stash |
| Deep Dive | one-breath descent, jellyfish, deep caches |
| Aurora Watch | calm memory round under the northern lights |

**218 cosmetics** across 8 slots that all stack — fur pattern, headwear, face, neck/back,
flippers, trail, emote and badge. One item per slot, every combination allowed.

**Seven rarity tiers.** Six drop from vault loot (Common → Mythic); EXCLUSIVE items come
only from the quest track and glow in the grid. Rarity is shown by shape *and* colour *and*
text, so the tiers stay readable without colour vision.

**Pity timers, not predation.** EPIC guaranteed every 22 rolls, LEGENDARY every 65, MYTHIC
odds ramp after 150 and cap at 220. Duplicates convert to pearls for slot-focused pulls.
All trackers are visible in the Loot Vault screen.

**Quest cosmetics** on their own track: Old Whiskers, Golden Flipper, Storm Rider Cape,
Deep Diver Goggles, Aurora Crown, Shellback Armor, Fisherman's Hat (a four-part chain
ending with an NPC delivery to Old Marlin), Ghost Trail (seasonal event only), and the
Founder's Tag + Salute for your first full prestige cycle.

**Prestige** resets fish, gear and season level for a permanent seal trim, +22% fish and
+5% luck per rank, up to rank 5. Cosmetics, pearls and quests are never lost.

## Controls

- **Move** — arrow keys / WASD, the on-screen d-pad, or drag on the canvas in the swim games
- **A** — Space / Z / Enter, or the A button
- **B** — X / Shift, or the B button
- **Esc** — back out of a screen or leave a vault run
- **W / Q / H** — wardrobe, quests, help

## Saving

Progress is written to `localStorage` for this browser automatically. `SYS → EXPORT SAVE`
downloads a `.json` backup; `IMPORT FILE` or `PASTE SAVE` restores it on any device.
Damaged or hand-edited saves are sanitised on load rather than crashing the game.

### Auto-save file (Chrome / Edge on desktop)

`SYS → LINK A SAVE FILE` lets you pick a `.json` once. After that the game writes every
save straight to that file and loads it back automatically next time you open the game —
no exporting, no importing, and it survives a cache clear.

This uses the File System Access API, so it is **desktop Chrome and Edge only**. Firefox,
Safari and every phone browser fall back to the manual export/import above, and the
settings panel says so rather than showing a button that does nothing.

Two safeguards worth knowing: writes are throttled so rapid autosaves batch into one disk
write, and on load the game compares timestamps — whichever of the file or the browser save
is newer wins, so neither can silently clobber the other.

## Accessibility

High-contrast palette, larger tap targets, reduced flashing, adjustable text size, and
colour-blind-safe rarity markers (shape + letter + colour). All in `SYS`.
