---
title: "Dual Subtitle Player"
categories: [Coding, Project]
tags: [coding, project, html5, javascript, video]
---

# The problem
You're watching content in a foreign language and want to compare different subtitle versions (original vs. translated) without constantly switching video tracks or opening multiple players.
Also, maybe you want a lightweight solution that works offline and respects your privacy by keeping everything local.

# Setup
Simply download the HTML file and open it in your browser OR visit the website: [Link](https://kyattpl.github.io/dual-subtitle-player/):
- Load your video file using the "Open Video" button
- Add your first subtitle file (.srt format) using the "Open SRT" button under "Subtitle 1"
- Add your second subtitle file using the "Open SRT" button under "Subtitle 2"
- Use the 'S' key or the toggle button to switch between subtitle files while watching

## Functionality

- Press 'S' key to instantly toggle between both subtitle files
- Click the "Switch Subtitle" button for the same effect
- Enter fullscreen mode while keeping subtitle switching capabilities
- Works with standard SRT subtitle files and common video formats
- Everything runs locally in your browser — **no data sent to any servers... nice**
- No installation or dependencies required

# Where to access it
Project available on GitHub: [https://github.com/KyattPL/dual-subtitle-player](https://github.com/KyattPL/dual-subtitle-player)
Website available at: [Link](https://kyattpl.github.io/dual-subtitle-player/)

Download the HTML file and open it directly in any modern browser. No server required!

# Use cases

- **Language learners**: Toggle between native language and target language subtitles
- **Film students**: Compare different translations or subtitle versions
- **Accessibility**: Choose the most helpful subtitle version for your needs
- **Translation study**: See how the same content is translated differently

# Technical details

Built with pure HTML5, CSS3, and JavaScript for maximum compatibility. The player parses SRT files into time-indexed objects and synchronizes display with video playback, allowing seamless switching between subtitle arrays based on user input.

Simple, lightweight, and privacy-focused!