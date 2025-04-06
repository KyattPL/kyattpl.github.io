---
title: "Soulsborne tracker"
categories: [Coding, Project]
tags: [coding, project, shadcn, nextjs, js]
---

# The Problem

Tracking progress in Soulsborne games can be overwhelming. With multiple bosses, hidden locations, and intricate item placements, players often rely on memory or external guides to track their progress. Whether you're a completionist aiming for 100% game completion, a speedrunner optimizing your route, or a casual player trying to keep track of defeated bosses, having an efficient tracking tool can enhance the experience.

This is where the **Soulsborne Tracker** comes in—a streamlined, interactive solution for managing your progress across multiple games in the series.

# Soulsborne Tracker: The Ultimate Progress Companion

This project is a web-based tracker that helps players manage their progress in Soulsborne games. Designed for ease of use, it provides an intuitive interface to track bosses, character stats, and key locations while offering smooth UI interactions.

## Key Features

### 1. Multi-Game Dashboard
- The main page displays a grid of game titles, including **Demon's Souls, Dark Souls 1, Dark Souls 2, Dark Souls 3, Bloodborne, and Elden Ring**.
- Clicking a game opens its dedicated dashboard with specific tracking features.

### 2. Boss Tracker
- Mark bosses as defeated and track the number of attempts per boss.
- Helps players optimize runs and revisit challenging fights for improvement.

### 3. Character & Player Stats
- Keep tabs on your character's level, build, stats (like Vigor, Strength, etc.), and current progression.
- Useful for min-maxing or maintaining multiple builds.

### 4. Equipment Loadout
- View and edit what your character currently has equipped in each slot (weapon, armor, rings, etc.).
- Great for remembering gear setups or sharing builds with friends.

### 5. Site of Grace / Bonfire / Lamp / Archstone Tracking
- Track visited or unlocked fast-travel points across all games.
- Helps ensure full exploration and no missed zones.

### 6. Game-Specific Systems
- **Demon’s Souls**: Track both **Player Tendency** and **World Tendency**.
- **Bloodborne**: Track collected **Blood Gems** and **Chalices** for dungeons and upgrades.

### 7. Visual Map Integration
- View game maps with key elements marked (e.g., boss locations, NPCs, bonfires).
- Aids navigation and planning in intricate areas.

### 8. Local Progress Saving
- All data is saved to your browser's **localStorage** so your progress persists between sessions.

### 9. Twitch chat integration
- You can connect to any twitch channel and whenever the streamer or the moderator types a command it will update the tracker on currently opened tab.

## Tech Stack
- **Next.js (App Router)** – Provides a fast, server-rendered web application experience.
- **TypeScript** – Ensures type safety and robust development.
- **Tailwind CSS** – Enables modern, responsive UI styling.
- **Framer Motion** – Adds smooth animations and transitions.
- **ShadCN** – Enhances the UI component system.
- **localStorage** – Allows for local progress saving

# Try It Out
This project is open-source and free to use! If you're a Soulsborne fan looking for a seamless way to track your journey, check out the full repository on GitHub and contribute to improving the experience for all players.

🌐 **Website:** [Link](https://kyattpl.github.io/soulsborne-tracker/)<br />
🔗 **GitHub Repository:** [Link](https://github.com/kyattpl/soulsborne-tracker)