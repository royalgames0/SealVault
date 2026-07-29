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
| Fish Dash | endless swim; dash through hazards, hunt the Lumina Fish |
| Ice Fishing | time the cast, then steer the lure deep for fish and treasure |
| Floe Survival | wave arena with a floating joystick, orca boss every 10 waves |
| Pearl Match | connected-blob match-3 bonus room |
| Belly Slide Race | rhythm slide, jump gaps, trick off ramps |
| Clam Dig | dig-timing on the beach; misses make the next dig easier |
| Synchronized Swim | endless four-lane rhythm; ten misses ends it |
| Iceberg Balance | spring-physics teeter on a shrinking berg |
| Seagull Chase | swat gulls, incl. golden thieves and the Radiant Gull |
| Deep Dive | fly a narrowing trench on one breath - depth only counts if you surface |
| Aurora Watch | calm memory round under the northern lights |

**220 cosmetics** across 8 slots that all stack — fur pattern, headwear, face, neck/back,
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
Founder's Tag + Salute for your first full prestige cycle. Two more are hidden in the vaults:
the Lumina Wake for catching the Lumina Fish in Fish Dash, and the Gilded Plume for downing
the Radiant Gull in Seagull Chase. Both are roughly one-in-many spawns; catching one again
after you own the cosmetic pays out a large fish bonus instead.

**Prestige** resets fish, gear and season level for a permanent seal trim, +22% fish and
+5% luck per rank, up to rank 5. Cosmetics, pearls and quests are never lost.

## Controls

- **Move** — arrow keys / WASD, the on-screen d-pad, or drag anywhere on the canvas: a
  floating joystick appears under your thumb in Fish Dash, Floe Survival and Deep Dive
- **A** — Space / Z / Enter, or the A button
- **B** — X / Shift, or the B button
- **Esc** — back out of a screen or leave a vault run
- **W / Q / H** — wardrobe, quests, help

## Saving

Progress is written to `localStorage` for this browser automatically. `SYS → EXPORT SAVE`
downloads a `.json` backup; `IMPORT FILE` or `PASTE SAVE` restores it on any device.
Damaged or hand-edited saves are sanitised on load rather than crashing the game.

### Home screen app (iPhone — important)

Safari deletes a site's saved data after roughly seven days of *browser* use without
revisiting, which will wipe your seal. Adding the game to your Home Screen runs it as a
standalone web app with its own storage timer, which resets each time you play — so saves
survive. On iPhone the game asks once when it opens; decline and it never asks again, and
`SYS → HOME SCREEN APP` still has the steps whenever you want them.

The app icon is baked into the file as a base64 PNG, drawn by the game's own seal renderer.
Export your save before adding the shortcut and import it afterwards: the browser tab and
the home screen app start with separate storage.

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

## Naming your seal

You are asked for a name on first run, and can change it any time from `SYS → RENAME SEAL`
or the RENAME button on the wardrobe preview.

## Accessibility

High-contrast palette, larger tap targets, reduced flashing, adjustable text size, and
colour-blind-safe rarity markers (shape + letter + colour). All in `SYS`.
