---
title: "Update to CSV Obsidian Movie catalogue"
categories: [Coding, Obsidian, Movies, TV-series]
tags: [coding, obsidian, movies, tvseries, js, csv]
---

# The Problem
When trying to use the 'fuzzySearch' for movie/tv series titles you might get an error that toLowerCase
function is not defined. It will pop up if you have an entry that is only a number (for example "1899").
The trick I mentioned in [my first post](https://kyattpl.github.io/posts/csv-obsidian-movie-catalogue/) that
uses artificial 'file: {name: ...}' object screws this up.

# Solution
To make the 'fuzzySearch' option work you have to change the line number 585 from this:
```js
pages = pages.filter(p => p.file.name.toLowerCase().includes(key.toLowerCase()))
```

to this:
```js
pages = pages.filter(p => `${p.file.name}`.toLowerCase().includes(key.toLowerCase()))
```

Enjoy!