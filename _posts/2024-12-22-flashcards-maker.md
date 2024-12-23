---
title: "Flashcards maker from your text data"
categories: [Generic]
---

# The problem
You have a list in a plain .txt format that you'd like to convert into flashcards.
Also, maybe you'd like to save some sets for free and/or have them stored locally.

# Setup
Simply gather your data in a txt file format:
- Each card on a separate line
- Choose one unique separator
- Format looks like "set1_card1\<separator\>set2_card1" for the first line
- Set2 will be the side shown first
- Paste the lines into the input field

## Functionality

- Click the cards to flip between front/back
- Press shuffle (🔀) button to randomize the flashcard study
- Save your flashcard set present in the input field (with a unique name)
    - All sets are saved using localStorage --> **fully locally... nice**
- Remove and load your sets

# Where to access it
Hosted at: [https://kyattpl.github.io/flashcards-maker/](https://kyattpl.github.io/flashcards-maker/)