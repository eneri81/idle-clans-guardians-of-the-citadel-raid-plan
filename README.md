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

1. **Clone or download** this repository.
2. Open **`index.html`** in a modern browser (Chrome 90+, Firefox 88+, Safari 14+, Edge 90+).
3. Choose your input mode:
   - **Enter Players:** type usernames, click **Fetch & Calculate**
   - **Enter Clan Name:** type clan name, select team size, click **Fetch Clan & Recommend**
4. Review the suggested role assignments and transition plan.
5. *(Optional)* Click a saved username to reuse it, or clear history.

---

## Repository structure
