---
title: "Subtitle Translate Player"
categories: [Coding, Project]
tags: [coding, project, shadcn, nextjs, js]
---

# The Problem

Tracking progress in Soulsborne games can be overwhelming. With multiple bosses, hidden locations, and intricate item placements, players often rely on memory or external guides to track their progress. Whether you're a completionist aiming for 100% game completion, a speedrunner optimizing your route, or a casual player trying to keep track of defeated bosses, having an efficient tracking tool can enhance the experience.

This is where our **Soulsborne Tracker** comes in—a streamlined, interactive solution for managing your progress across multiple games in the series.

# Soulsborne Tracker: The Ultimate Progress Companion

Our project is a web-based tracker that helps players manage their progress in Soulsborne games. Designed for ease of use, it provides an intuitive interface to track bosses, character stats, and key locations while offering smooth UI interactions.

## Key Features

### 1. Multi-Game Dashboard
- The main page displays a grid of game titles, including **Demon's Souls, Dark Souls 1, Dark Souls 2, Dark Souls 3, Bloodborne, and Elden Ring**.
- Clicking a game opens its dedicated dashboard with specific tracking features.

### 2. Dark Souls 1 Dashboard
- A three-column layout featuring:
  - **Left:** Character and player statistics.
  - **Middle:** A **boss checklist** with a simple checkmark system for tracking defeated bosses.
  - **Right:** An **interactive map** showing boss locations, key items, and bonfires.
- Progress is saved locally using **localStorage**.

### 3. Boss Checklist Component
- Loads boss data from a structured JSON file.
- Players can check off defeated bosses.
- Data persists using **localStorage**, ensuring progress is saved across sessions.

### 4. Interactive Map Component
- Displays a **pre-rendered map** of Lordran (Dark Souls 1) with markers for bosses, bonfires, and key locations.
- Clicking a marker reveals a **popup with detailed information**.
- Includes toggle filters to display only specific markers (e.g., bosses, bonfires, items).

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