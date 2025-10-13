---
title: "Metal Bands World Map - A D3.js & React Visualization"
categories: [Coding, Project, Data Visualization]
tags: [coding, project, react, nextjs, d3js, data visualization, maps, music]
---

# The problem
As a huge metal fan, I know that the genre is a global phenomenon. But simply reading a list of bands and their home countries is boring. I wanted a way to *see* the geography of metal, to explore where my favorite bands come from on an interactive, visual platform. Existing maps were often static or part of larger, more complex applications. I needed a fast, clean, and focused tool to turn a simple dataset into an engaging experience.

# How to Use
Simply visit the website: [Link](https://kyattpl.github.io/metal-map/):
1.  The world map loads immediately, with countries color-coded by the number of bands.
2.  **Hover** over a country to see a quick preview of its bands in a tooltip.
3.  **Click** on a country to populate the sidebar with a full, scrollable list of all its bands.
4.  **Scroll** with your mouse or use the `+` and `-` buttons to zoom in and out.
5.  **Click and drag** the map to pan and explore different regions.
6.  Use the "Reset View" button to return the map to its original position and zoom level.

## Functionality

- **Interactive Choropleth Map**: Countries are shaded based on the density of bands, providing an at-a-glance view of metal hotspots.
- **Dynamic Tooltips**: Get instant information on hover without having to click.
- **Detailed Sidebar**: Clicking a country provides a clean, dedicated space to browse its complete list of bands.
- **Smooth Zoom & Pan**: Powered by D3.js, the map navigation is fluid and intuitive.
- **Customizable Data**: The entire map is driven by a simple data file, making it easy to add your own favorite bands.
- **Clean & Responsive**: A modern, dark-themed interface that looks great on any device.
- **Self-Contained**: Everything runs in the browser with no backend or database required.

# Where to access it
Project available on GitHub: [https://github.com/KyattPL/metal-map](https://github.com/KyattPL/metal-map)
Website available at: [Link](https://kyattpl.github.io/metal-map/)

# Technical details

Built with a modern web stack to ensure a high-quality, performant user experience.
- **Framework**: Next.js and React for building the user interface and managing component state.
- **Data Visualization**: D3.js for rendering the map, handling zoom/pan behavior, and binding data to SVG paths.
- **Map Data**: TopoJSON for efficiently loading and parsing the world geography data.
- **Styling**: Tailwind CSS for a utility-first approach to creating a clean, responsive design.
- **UI Components**: Shadcn/UI for the pre-built, accessible components like Cards and Buttons.
- **Language**: TypeScript for type safety and improved developer experience.