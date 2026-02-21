# Guardians of the Citadel Raid Planner — Idle Clans

A lightweight, single-page raid planner for **Idle Clans: Guardians of the Citadel**. It fetches player skill data from the **IdleClans public API** and helps you coordinate **support-role assignments** for a **2–6 player** team, including phase transition strategies.

**Inspired by** [Warscroll's Reckoning of the Gods Planner](https://github.com/Warscroll/idleclans-ReckoningoftheGods-Planner)  
**Raid reference:** [Guardians of the Citadel — Idle Clans Wiki](https://wiki.idleclans.com/index.php/Guardians_of_the_Citadel)

---

## What it does

### Fetches player skill data
- **Player mode:** Enter up to 6 usernames to fetch individual profiles
- **Clan mode:** Enter a clan name, select team size (2–6 players)
- Data source: [`https://query.idleclans.com/api`](https://query.idleclans.com/api)

### Converts XP to skill levels
The IdleClans API returns skill experience points (XP). The planner converts XP → level using an embedded lookup table (supports levels 1–120).

### Recommends optimal support setup
Analyzes the six **key Citadel support skills**:
- **Foraging** & **Woodcutting** → early-phase resource gathering
- **Farming**, **Brewing**, **Carpentry** & **Crafting** → mid-to-late phase production

The planner then:
1. **Ranks all players** for each skill
2. **Suggests role assignments:**
   - Primary Forager (highest Foraging level)
   - 1–2 Woodcutters (best available)
   - Distributed Farming / Brewing / Carpentry / Crafting roles
3. **Provides a transition plan** – how to shift people from gathering → production as the raid progresses

> The general intent mirrors typical Citadel progression: focus on gathering seeds/wood/ingredients early, then pivot team members to Carpentry/Crafting once setup is complete.

---

## Features

- **Flexible input modes**
  - **Enter Players:** you + 1–5 others (manual entry)
  - **Enter Clan Name:** auto-populate from clan member list, choose team size
- **Single HTML file** – no build step, no dependencies
  - Open `index.html` directly in a modern browser
- **Dark Mode toggle** – preference saved to `localStorage`
- **Recently used names** – quick-click history saved locally
  - Clear history button to reset
- **Built-in safety & privacy**
  - Username sanitization (limited character set and length)
  - Content Security Policy headers
  - All data is local + live API calls only (no backend, no accounts, no tracking)

---

## How to use

### Option 1: Use GitHub Pages (fastest)
1. Visit: **https://eneri81.github.io/idle-clans-guardians-of-the-citadel-raid-plan/**
2. Start entering player names or a clan name and click **Fetch & Calculate** or **Fetch Clan & Recommend**
3. Done! No installation needed.

### Option 2: Download and run locally
1. Click **Code** → **Download ZIP** on this repository
2. Extract the ZIP file to any folder
3. Open **`index.html`** in your browser (double-click or drag into browser)
4. Enter player names or clan name and start planning

### Option 3: Clone the repository
1. Clone this repo:
   ```bash
   git clone https://github.com/eneri81/idle-clans-guardians-of-the-citadel-raid-plan.git
   ```
2. Open `index.html` in your browser
3. Review the suggested role assignments and transition plan

---

## Requirements

- **Browser:** Modern browser with ES6+ support
  - Chrome 90+, Firefox 88+, Safari 14+, Edge 90+
- **Network:** Internet access to `https://query.idleclans.com` (IdleClans API)
- **Files:** `index.html` and the `files/` directory (assets)

---

## Data & privacy

- **No backend:** Player/clan data is fetched live from the IdleClans API; nothing is sent to a server.
- **Local storage only:**
  - Dark mode preference
  - Recently entered usernames
- **No analytics, no tracking, no accounts** – use it entirely offline after the first API fetch.

---

## Not affiliated

This is a community-made helper tool and is **not officially affiliated with IdleClans**.

---

## Credits

- **Inspired by:** [Warscroll's Reckoning of the Gods Raid Planner](https://github.com/Warscroll/idleclans-ReckoningoftheGods-Planner)
- **Idle Clans game:** [idle-clans.com](https://idle-clans.com)
- **Community wiki:** [wiki.idleclans.com](https://wiki.idleclans.com)



