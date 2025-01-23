---
title: "AnkiAutoSuspend plugin"
categories: [Coding, Anki, Languages]
tags: [coding, anki, languages, python]
---

# The problem
When you're learning a new language with flashcards, some cards eventually get *too easy*. 
You've reviewed them enough to know them inside out, but the system still schedules them for months down the line. 
It’s annoying, and managing this manually is a pain. Wouldn’t it be great if cards could just suspend 
themselves once you’ve clearly mastered them?


# AnkiAutoSuspend plugin

Presenting to you... the "AnkiAutoSuspend" plugin!

Addon to automatically suspend cards above specified interval. It performs the action automatically for the selected
collection (can be run manually via "Tools" -> "Auto suspend cards"). Go to "Tools" -> "Add-ons" -> "Auto suspend cards"
-> "Config" to edit the suspend point (for example setting it to "90" will result in automatic suspension of any card
which interval is >= 90 days).

Link to AnkiWeb: [AnkiWeb](https://ankiweb.net/shared/info/733229757) <br />
Link to GitHub: [Repo](https://github.com/KyattPL/anki-auto-suspend)