# ⭐ QuestForge

**Your daily life as a role-playing game.** Everyday tasks are *Daily Quests*, big tasks are *Boss Battles*, and finishing them earns XP and gold, levels up your hero and defeats monsters in an animated pixel-art battle scene.

QuestForge is **rewards-only**: nothing is ever taken away. Missing a day never costs XP, gold or health, and streaks are protected by Rest tokens, holiday mode and next-day ticking.

It's a single web page with no build step and no server of its own. It runs in any modern browser on a computer or phone, works offline, and can optionally sync between devices.

> **Status:** first prototype. Everything below works and is covered by built-in self-tests. Cloud sync has been tested against a simulated server, but not yet against a real Supabase project or on a real phone.

---

## Contents

- [Quick start](#quick-start)
- [Features](#features)
- [How the numbers work](#how-the-numbers-work)
- [Phone app and sync](#phone-app-and-sync)
- [Your data, backups and privacy](#your-data-backups-and-privacy)
- [Project files](#project-files)
- [Customising and extending](#customising-and-extending)
- [Self-tests](#self-tests)
- [Troubleshooting](#troubleshooting)
- [Known limitations](#known-limitations)

---

## Quick start

1. Double-click **`QuestForge.html`** to open it in Chrome, Edge, Firefox or Safari.
2. Choose your hero's name and look.
3. Example quests, a sample boss and a *Job Hunt Campaign* are loaded so the app isn't empty. When you're ready, use **🧪 Clear examples**, or **🧹 Start blank** to remove every quest and boss.
4. Add your own with **＋ New Daily Quest** and **🐉 New Boss**.

Progress saves automatically in your browser. To use it on your phone too, see [Phone app and sync](#phone-app-and-sync).

---

## Features

### 🔁 Daily Quests: small, everyday tasks
- Choose which **days of the week** each one repeats. They reset at midnight (local time).
- Each has a **difficulty** (Trivial → Epic), one or more **life areas**, and optional **time estimate**, **energy level** and **notes**.
- **Daily target with extras:** set a target such as *3 job applications a day* to get a **＋1 counter**. Reaching the target completes the quest, and every one past the target earns **bonus XP and gold**.
- **Steps:** an optional checklist inside a quest. On Daily Quests the ticks reset each day.
- **Tick yesterday's quests:** forgot to tick something you did last night? A **🌙 Yesterday** section on Today lets you log it for yesterday until midnight. Your streak waits for you in the morning.
- **Undo** anything ticked by mistake.
- **Drag to reorder** with the ⋮⋮ handle (mouse or finger). Completed quests drop to the bottom until the next day.
- **Habit streaks:** each quest shows its own 🔥 run, counting only the days it's scheduled.

### 🐉 Boss Battles: big tasks
- A boss is a large task (e.g. *Tidy my room*) broken into **sub-quests**.
- It has an **HP bar**; each finished sub-quest deals damage equal to its difficulty.
- Defeating it plays a victory animation and opens a **gold chest**: **2× the sub-quests' XP** plus **their gold + 50**.
- Pick the creature (Dragon, Hydra, Golem, Kraken, Demon Lord), its colours, its name, an optional **deadline** and one or more life areas.
- **Campaigns** chain bosses in order on a map. The example is the *Job Hunt Campaign*: Polish CV & Portfolio → Send 10 Applications → Land First Interview → Ace the Interview → Get the Offer.

### ⚔️ Animated battle panel
- Your pixel-art hero faces a monster for your next unfinished quest. Bigger quests bring bigger monsters (slimes, bats, mushrooms, beetles, wisps, goblins, imps, brutes).
- Completing a quest triggers an attack, a damage number, the monster's defeat, and XP and coins popping out.
- **Boss mode** brings in a large boss with its own HP bar. Each sub-quest is a hit, and the final hit plays a bigger victory with confetti.
- With nothing left to do, the hero rests by a campfire.
- All characters and creatures are original designs drawn in code.

### 🧙 Character, levels and unlocks
- An XP bar and level, with titles that change as you grow (Novice → Adventurer → Knight → Champion → Legend).
- **Every level up to 20 unlocks something**: 9 colour themes, titles, portrait frames, headgear, weapons, capes/wings and auras. Equip them in **🎒 Inventory**. Each level after 20 adds a ★ under your portrait.

### 🧭 Life areas
- Career, Fitness, Home, Social, Learning and Wellbeing. You can add, rename, recolour or remove areas in Settings.
- Each area has its own level, shown as bars and a radar chart, with a gentle hint about areas that have been quiet lately.
- A quest can belong to **several areas**, and each one gets the quest's full XP.

### 🔥 Streaks, Rest tokens and holidays
- A **daily streak** for completing at least one quest a day, with an **XP bonus**: +10% at 3 days, +20% at 7, +30% at 14+.
- **Rest Day tokens:** earn one per 7-day run (hold up to 3). A missed day automatically uses one.
- **🏖️ Holiday mode:** set your trip dates and your **normal Daily Quests pause** and your **streak is frozen**: blank days never break it and use no tokens. Quests marked **Holidays only** appear instead, and completing them still grows your streak. You can plan trips in advance, and **I'm back** ends one early.
- Losing a streak is never punishing; you just get a friendly "start a new one" note.

### 🛒 Rewards Shop
- Create your own real-life rewards with gold prices (e.g. *1 hour of gaming: 200 gold*).
- Rewards can be **one-off or repeatable**. Purchases are logged with the date and can be refunded if you bought one by mistake.

### 🏆 Achievements
24 badges with pop-up notifications, for example *First Blood*, *Giant Slayer*, *On Fire* (7-day streak), *Unstoppable* (30-day), *Well-Rounded*, *Job Hunter*, *Above and Beyond* and *Bon Voyage*. Locked ones show greyed out in the **Trophy Room**.

### ⏱ "Just Start" focus timer
- Press **▶ Start** on any quest or sub-quest for a 10, 15 or 25-minute timer.
- **+3 XP just for starting** (once per quest per day), to beat procrastination.
- A gentle bell plays at the end. It has its own on/off switch, separate from the other sound effects.

### 📅 Planning
- **Today:** your Daily Quests, the Yesterday section, active bosses, and a **daily load** bar that gently warns if you've planned more than about 6 hours or more than 3 Hard/Epic quests.
- **Quest Log:** week and month views of your Daily Quests, boss deadlines and holidays. Click a day to create a boss due that day, and drag a 💀 deadline to move it.
- **📊 Weekly Recap:** XP, quests, bosses, best streak, gold earned and spent, the life area that grew most, and an XP-per-day chart. A summary pops up the first time you open the app each new week.

### 🎨 Feel and accessibility
- Pixel/fantasy headings, a clean body font, dark theme by default plus a light theme and unlockable ones.
- Sound effects generated in the browser, with a mute button.
- **Reduce motion:** follows your system setting or can be set in Settings. It tones animations down.

---

## How the numbers work

| Difficulty | XP | Gold | Boss damage |
| --- | --- | --- | --- |
| Trivial | 5 | 2 | 5 |
| Easy | 10 | 5 | 10 |
| Medium | 25 | 10 | 25 |
| Hard | 50 | 20 | 50 |
| Epic | 100 | 40 | 100 |

- **Levels:** XP needed for the next level = `round(100 × level^1.5)`, so 100, 283, 520, 800, … Life areas use a faster curve, `round(50 × level^1.5)`.
- **Streak bonus** applies to XP only (gold is unchanged).
- **Extras past a daily target** are worth `round(quest XP ÷ target × 1.5)` XP and `round(quest gold ÷ target × 1.5)` gold, plus your streak bonus. For a Medium quest with a target of 3, that's +13 XP and +5 gold each.
- **Boss victory bonus:** 2 × the sub-quests' combined base XP, and a chest of their combined gold + 50.
- **Rest tokens** only cover a gap if they can cover the whole gap. If not, the streak quietly resets and you keep your tokens.

---

## Phone app and sync

QuestForge can be installed on your phone like an app and keep your progress in step across devices. This uses two free services, each needing an account you create yourself:

| Service | What it's for |
| --- | --- |
| **Supabase** | Stores your save in the cloud and handles sign-in. |
| **GitHub Pages** | Gives the app a web address to open and install on your phone. |

**Full click-by-click instructions are in [`SETUP-PHONE-AND-SYNC.md`](SETUP-PHONE-AND-SYNC.md)** (about 20–30 minutes, once). In short:

1. **Supabase:** create a free project and run the setup SQL (**Settings → ☁️ Sync → 📋 Copy setup SQL** copies it). Copy the **Project URL** and **publishable (anon) key**. Never use the secret / service_role key; the app refuses it.
2. **Your computer:** **Settings → ☁️ Sync**, paste the URL and key, then **Create account**. Your current progress uploads. Afterwards, turn off new sign-ups in Supabase so no one else can create accounts on your project.
3. **GitHub Pages:** create a public repository, upload `QuestForge.html`, `index.html`, `manifest.webmanifest`, `sw.js` and the `icons` folder, then enable Pages.
4. **Your phone:** open the web address, then **Add to Home Screen** (Safari → Share on iPhone; Chrome → ⋮ → Install app on Android). In **Settings → ☁️ Sync**, sign in and choose **Use the cloud save on this device**.

**How sync behaves**
- Changes upload a couple of seconds after you make them. Each device checks for updates when the app opens, when you switch back to it, and every minute while it's open.
- **Completed quests, XP and gold from every device add up**, even after using two devices offline. An undo or refund on one device is applied everywhere.
- For things you edit (quests, bosses, rewards, settings, holidays), **the most recent edit wins** if the same thing is changed on two devices at nearly the same time.
- The first sign-in on a device that already has a cloud save asks which progress to keep.
- The **☁️ button's dot** shows the status: green synced, blue syncing, amber offline, red needs attention.
- **Settings → Reset everything** while signed in also resets the cloud copy, and so every device.

**Optional:** the Project URL and publishable key can be built into the app (the `SYNC_DEFAULTS` line in `QuestForge.html`) so each device only needs to sign in. They're designed to be public; your data is protected by Supabase's row-level security and your login.

---

## Your data, backups and privacy

- Everything is stored **in your browser** (localStorage) under one key, `questforge.save.v1`. Sync sign-in details are kept separately under `questforge.sync.v1` and are never included in backups.
- **💾 Export backup** downloads all your data as a JSON file; **📂 Import backup** loads one, replacing what's there. Both are in the side menu on desktop and in Settings.
- Opening `QuestForge.html` as a file and opening the hosted web address keep **separate local copies**. Sync connects them, or you can move data across with Export/Import.
- Without sync, nothing leaves your device. With sync, your save goes only to **your own** Supabase project.
- The GitHub repository holds only the app's code, never your quests or progress. Anyone with the address sees an empty app.
- Google Fonts are loaded from the web. Offline, the app falls back to system fonts.

---

## Project files

| File | Purpose |
| --- | --- |
| `QuestForge.html` | **The whole app**: HTML, CSS and JavaScript in one file. |
| `index.html` | Redirects the hosted site's root address to `QuestForge.html`. |
| `manifest.webmanifest` | App name, colours and icons for "Add to Home Screen". |
| `sw.js` | Service worker: lets the installed app open offline. Pages load from the network first, so updates arrive automatically. Sync traffic is never cached. |
| `icons/` | App icons (pixel-art star), including iPhone and Android versions. |
| `SETUP-PHONE-AND-SYNC.md` | Step-by-step phone and sync setup. |
| `README.md` | This file. |

To **update the hosted app**, upload the new `QuestForge.html` to the GitHub repository (Add file → Upload files; the same name replaces the old one). Phones pick it up the next time they open the app online.

---

## Customising and extending

`QuestForge.html` is organised into numbered sections. Search for the `=====` banners; a file map sits at the top of the file.

| Section | What's there |
| --- | --- |
| 1. STYLES | Colour themes (CSS variables), layout, the mobile layout, animations |
| 2. MARKUP | The static shell: top bar, menu, main area, battle panel |
| 3. CORE | Pure game logic with no page access: XP and levels, streaks, holidays, boss HP, weekly recap, sync merging, **self-tests** |
| 4. CONTENT | **Unlock table, achievements, default life areas, example data**: the easiest place to tweak |
| 5. STORE | Saving, loading, backup import/export, upgrading older saves |
| 6. SOUND | Sound effects generated with the Web Audio API |
| 7. ART | The pixel painter and every hero, monster and boss sprite |
| 8. BATTLE | The animated battle panel |
| 9. FX | Toasts, confetti, sparks |
| 10. UI | All screens and pop-ups |
| 11. ACTIONS | Everything that changes your data |
| 12. SYNC | Supabase sign-in and syncing |
| 13. BOOT | Startup, the midnight reset, timers |

Common tweaks:
- **Rewards per difficulty, streak bonus tiers, load limits:** top of section 3 (`DIFFICULTIES`, `STREAK_TIERS`, `LOAD_LIMIT_MIN`, …).
- **New achievement:** add a line to `ACHIEVEMENTS` in section 4 with an `id`, `icon`, `name`, `desc` and a `test(c)` condition.
- **New unlock:** add a line to `UNLOCKS` in section 4.
- **New colour theme:** add a `body[data-theme="…"]` block of variables in section 1 and a matching `UNLOCKS` entry.

---

## Self-tests

**Settings → 🧪 Run self-tests** checks the game logic: XP maths and level thresholds, streak bonuses, Rest tokens, holidays, next-day ticking, daily resets at midnight, daily targets and extras, multiple life areas, boss HP and victory bonuses, the daily load warning, and sync merging. There are currently **69 tests, all passing**.

---

## Troubleshooting

| Problem | What to do |
| --- | --- |
| "Could not save to browser storage" | The browser is blocking storage (e.g. a private window). Use a normal window, and Export a backup. |
| Progress missing after switching between the file and the web address | They're separate copies. Sign in to sync on both, or Export from one and Import into the other. |
| Sync: "Wrong email or password" | Check them. Use **Create account** only the first time. |
| Sync: "Please confirm your email first" | Click the link in the Supabase email, then **Sign in**. |
| Sync: "row-level security" or "relation … does not exist" | Run the setup SQL again in Supabase's SQL Editor. |
| Sync: "Invalid API key" | Re-copy the publishable/anon key (**Settings → Sync → Change project**). |
| Sync stopped after a long break | Free Supabase projects pause after a week without use. Open the Supabase dashboard and click **Restore project**. |
| Phone shows an old version | Close and reopen the app while online. |

---

## Known limitations

- Sync is **last-edit-wins per list** (e.g. the whole quest list). Editing your quests on two devices at nearly the same moment keeps only the later edit. Completions, XP and gold always merge safely.
- Ticking a quest late only goes back **one day**.
- Completed Daily Quests drop to the bottom of the list until the next day, so a custom order only applies within the done and not-done groups.
- Boss deadlines can be dragged in the Quest Log with a mouse. On a phone, change them in the boss's edit screen.
- The weekly summary pop-up appears on your first visit of each new week, not strictly on Mondays, so you don't miss it if you skip a Monday.
