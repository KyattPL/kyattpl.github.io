---
layout: post
title: "CSV Obsidian Movie/TV series catalogue"
category: generic
---

# The Problem
So if you're like me you wanted to create a personal DB where you can track your watched movies/tv series.
You're also an Obsidian user that likes to store everything in a single vault. Now, there are tutorials on YouTube
on how to create a movie catalogue in Obsidian. The problem arises when you realize that you might end up with
hundreds or thousands of .md files. There's gotta be something else for storing your data in a single place instead, right?
Well, I managed to do it using a single CSV file, and here's how:

# The initial setup
You can pretty much follow this tutorial up to 05m 50s: [https://www.youtube.com/watch?v=t-hKCgGhQuk](https://www.youtube.com/watch?v=t-hKCgGhQuk). If you also want
to have a traditional note-based DB (that is, a single note for every movie/tv series) - do exactly as he says. If you only
want the CSV solution, you can skip everything relating to 'Templater' plugin. Now, there are a couple of modifications we need
to make in the movies.js script.

# Movies.js
First, I add some imports and desired CSV_FILE_PATH (it will create the file at the root of the vault) at the beginning:

```js
const fs = require('fs');
const path = require('path');
const notice = msg => new Notice(msg, 5000);
const log = msg => console.log(msg);

const API_KEY_OPTION = "OMDb API Key";
const API_URL = "https://www.omdbapi.com/";
const CSV_FILE_PATH = path.join(app.vault.adapter.basePath, 'movies-series-db.csv');
```

Then, at the bottom of the file I make a new function that will append a new row to this CSV file. I might have some extra properties like 'totalSeasons'
that I've edited in myself so if you have the default script REMOVE THE `${movieData.totalSeasons}` PART.

```js
async function appendToCSV(movieData) {
    const csvLine = `"${movieData.Title}","${movieData.Year}","${movieData.Genre}","${movieData.Director}","${movieData.Actors}","${movieData.imdbRating}","${movieData.imdbID}","${movieData.Runtime}","${movieData.Poster}","${movieData.totalSeasons}","${movieData.Country}"\n`;
    try {
        fs.appendFileSync(CSV_FILE_PATH, csvLine);
        notice("Movie data appended to CSV file.");
    } catch (error) {
        console.error("Error appending to CSV:", error);
        notice("Failed to append data to CSV file.");
    }
}
```

Finally, at the end of the start function just add `await appendToCSV(selectedShow);`.

!!! Before you run the script I think you have to manually create your CSV file with the exact name and columns that you've used above !!!

# Displaying the data

Great, so now the data should be appended to your CSV file, but is there any way to display it? Yes there is!
I've found this helpful script for rendering interactive tables in Obsidian here: [https://github.com/anareaty/obsidian-snippets/blob/main/Dataview-interactive-tables/dvit-info-en.md](https://github.com/anareaty/obsidian-snippets/blob/main/Dataview-interactive-tables/dvit-info-en.md).

1. You have to install the 'Dataview' community plugin
2. In the 'Dataview' plugin options toggle 'Enable JavaScript Queries'
3. Install the 'CustomJS' plugin.
4. Download the [interactive-tables.js](https://github.com/anareaty/obsidian-snippets/blob/main/Dataview-interactive-tables/interactive-tables.js) file
and put it into the scripts folder (at 2m 40s in the video I shared above he shows how to set up the scripts folder).
5. Do the number 4 from above github page - section 'How to set up'.
6. Create a new note where you want to render your table and follow the next section

# Final script and possible workarounds
In the freshly made note you can paste my script which looks as follows:

```js
// wrap the script in ```dataviewjs ``` block

// DataviewJS code to replicate the provided Dataview query 
const movies = await dv.io.csv("movies-series-db.csv");
const sortedMovies = movies.sort(movie => movie.title);

const moviePages = sortedMovies.map(movie => {

	return { 
	file: { path: movie.title, name: movie.title },
	poster: movie.poster,
	title: movie.title,
	year: movie.year,
	country: movie.country.split(',').map(c => `${c.trim()}`),
	genre: movie.genre.split(',').map(g => `${g.trim()}`),
	imdbRating: `⭐ ${movie.imdbRating}`,
	myRating: `${movie.rating}`
	}; 
});

// General view settings
const settings = {
    "entries on page": 10,
    "cards image position": "horizontal",
    "full width": true,
}

// Properties settings
const props = [
	{
		"prop": "title",
		"name": "Title",
		"filter": true,
		"column": true
	},
	{
		"prop": "poster",
		"name": "Poster",
		"image": true,
		"column": true
	},
	{
		"prop": "year",
		"name": "Year",
		"filter": true,
		"column": true
	},
	{
		"prop": "country",
		"name": "Country",
		"filter": true,
		"column": true,
		"multiSelect": true
	},
	{
		"prop": "genre",
		"name": "Genre",
		"filter": true,
		"column": true,
		"multiSelect": true
	},
	{
		"prop": "imdbRating",
		"name": "⭐ IMDB",
		"filter": true,
		"column": true
	},
	{
		"prop": "myRating",
		"name": "My rating",
		"filter": true,
		"column": true
	},
]

await customJS.dvIT.renderView(settings, props, moviePages, dv)
```

There are a couple of things to mention:

1. Edit the csv filename!
2. I sort my movies by title, you can remove that line.
3. Settings and props are explained on the github, you can figure it out.
4. Now, doing that moviePages is kinda cheating since this script expect you to use dv.pages() functions and have a proper
note structure. BUT SINCE WE DON'T WANT THAT we have to work around it and that's why for each movie we need to create a proper
structure that resembles the obsidian note (especially the file: {path, name}), got it?
5. SO, make sure you have that file property.

Workarounds:
1. If you have a numeric field that you want to filter (filtering means choosing the exact value pretty much), then
inside the returned object write property: `${movie.XYZ}`, where XYZ is the csv header of that column. This will cast the numbers
to strings so you can filter it.
2. If you have fields such as genres or countries, that have a couple strings that repeat in many rows (that is, a movie title is pretty unique
but 'Fantasy' genre can of course apply to many films) AND that should be split apart (that is, no matter if movie is 'Fantasy & Action' or 
'Fantasy & Comedy' you would want to only filter 'Fantasy')... follow this:
- you can do something similar to me in the script above for country/genre, by that I mean split up your string and leave with an array of items
    (for example ['Fantasy', 'Action']).
- then you have to open the 'interactive-tables.js' file, find the 'getPropType' function (~421 line) and after `prop=="aliases"` add
    `|| prop == "XYZ"` where XYZ is the EXACT key used in the return object 
    (that is when I used `country: movie.country.split(',').map(c => '${c.trim()}'),` above, my key would be 'country').

Phew! That was a lot... With a couple of trials and errors you can work it out.