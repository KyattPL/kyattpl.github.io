---
title: "Kyatt's Corner: A Personal Tierlist & Media Collection Hub"
categories: [Coding, Project]
tags: [coding, project, react, nextjs, tailwindcss, typescript, personal]
---

# The problem
I've always wanted a single, clean place to host my personal rankings and media collections. Standard note-taking apps are too unstructured, and public platforms like Letterboxd don't cover everything or lack the specific custom fields I want for my tier lists. I needed a self-hosted, self-designed website to be the definitive source for my personal opinions on games, music, and movies.

# How to Use
The application is split into two main sections: the Tierlist Dashboard and the Movie Collection.

### Tierlist Dashboard
1.  Use the collapsible sidebar on the left to navigate through hierarchical categories (e.g., "Souls-like Universe").
2.  Click on a specific list, like "Overall Souls Games," to view its content.
3.  Toggle between **"Tier View"** for a classic, visual layout and **"Table View"** for a detailed, sortable data grid.
4.  Use the search bar at the top to instantly filter for specific items within the selected list.

### Movie & Series Collection
1.  Navigate to the "Movie Collection" page from the main dashboard.
2.  Use the powerful search bar to find media by title, director, or actors.
3.  Apply filters to narrow down the list by genre or watch status (e.g., "in-progress").
4.  On a desktop, click on any column header to sort the entire collection by that metric, such as my personal rating or the IMDb rating.
5.  On mobile, the view adapts to a poster-rich card layout for easy browsing.

## Functionality

- **Hierarchical Tierlist Navigation**: Browse nested categories and lists with a clean, collapsible sidebar.
- **Dual View Modes**: Switch between a visual "Tier View" and a detailed, sortable "Table View" for tierlists.
- **Advanced Media Collection Filtering**: Filter a large movie/series collection by genre, status, and a global search.
- **Dynamic Sorting**: All tables are sortable by any column, from item names to custom ratings.
- **Data-Driven Content**: The movie collection is powered by a simple CSV file, making it incredibly easy to update.
- **Fully Responsive Design**: The entire site is optimized for a seamless experience on both desktop and mobile devices.
- **Dark/Light Theme**: A modern theme toggle that respects system preferences and saves user choice.

# Where to access it
Project available on GitHub: [https://github.com/KyattPL/my-tierlists-ranking](https://github.com/KyattPL/my-tierlists-ranking)
Website available at: [https://kyattpl.github.io/my-tierlists-ranking/](https://kyattpl.github.io/my-tierlists-ranking/)

# Use cases

- **Personal Organization**: A central hub for me to track my media consumption and crystallize my opinions.
- **Sharing with Friends**: An easy way to share my favorite games, movies, or music recommendations.
- **Developer Portfolio**: A practical, real-world example of a modern web application built with the latest technologies.
- **Inspiration**: A template for others who want to build their own personal ranking or collection website.

# Technical details

Built with **Next.js (App Router)** and **TypeScript** for a robust, type-safe foundation. The user interface is styled with **Tailwind CSS** for a clean, utility-first design. All icons are provided by **Lucide React**. The tierlist data is currently mocked statically, while the movie collection is parsed from a local CSV file on the server at build time, ensuring lightning-fast performance.