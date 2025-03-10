---
title: "Subtitle Translate Player"
categories: [Coding, Project]
tags: [coding, project]
---

# The Problem

Watching videos in a foreign language can be challenging, especially when subtitles are not available in your preferred language. Whether you're a language learner, an international film enthusiast, or someone who frequently watches educational content in multiple languages, subtitles play a crucial role in understanding and enjoyment. However, finding accurate subtitles in the desired language is often difficult, and machine-translated captions on platforms like YouTube can be unreliable.

This is where our **Subtitle Translator** project comes in handy. It provides an easy-to-use solution for translating subtitles on any video file, ensuring a seamless viewing experience with accurate translations.

# Subtitle Translator: A Simple Solution

Our project allows users to translate subtitles for videos using LibreTranslate. This tool ensures that subtitles are accurately converted from one language to another, making content accessible to a wider audience.

## How It Works

### 1. Load Your Video and Subtitle Files
- Open `index.html` in your browser.
- Click **Open Video** to load a video file.
- Click **Open SRT** to load the corresponding subtitle file.
- Select the **Source Language** (original subtitle language) and the **Target Language** (translation output).

### 2. View Translations
- Subtitles appear as the video plays.
- Click on the subtitle text to toggle translations on/off.
- Press **Enter Fullscreen** to display subtitles over the video for a more immersive experience.

## Installation and Setup

### 1. Clone the Repository or Download the ZIP
To get started, clone this repository using Git:
```sh
git clone https://github.com/KyattPL/subtitle-translate-player.git
```
Alternatively, download the ZIP file and extract it to your preferred location.

### 2. Install LibreTranslate
LibreTranslate is required for subtitle translation. Install it using `pip` inside a virtual environment:
```sh
python -m venv venv
source venv/bin/activate  # On Windows, use 'venv\\Scripts\\activate'
pip install libretranslate
```

### 3. Start LibreTranslate
Run LibreTranslate with the required languages:
```sh
libretranslate --load-only en,es,<lang_codes>
```
Replace `<lang_codes>` with the language codes you want to support (e.g., `fr`, `de`).

## Features
- Supports various video formats.
- Works with `.srt` subtitle files.
- Auto-detects and translates subtitles using LibreTranslate.
- Clickable subtitles to toggle translation visibility.
- Fullscreen mode with overlay subtitles.

# Try It Out
This project is open-source and free to use! Check out the full repository on GitHub and contribute to improving subtitle translations for everyone.

🔗 **GitHub Repository:** [GitHub Link](<repo_url>)