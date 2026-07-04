# Mise 🍽️ — Recipe Search App

A single-page recipe discovery app built with **React, HTML, CSS, and JavaScript**. Search any dish, browse by Veg / Non-Veg / Desserts, and get real-time ingredients, step-by-step instructions, and a cooking video — all in one clean, responsive interface.

Live in one file: `food-app.html`. No build step, no install — just open it in a browser.

## Features

- 🔍 **Real-time recipe search** powered by [TheMealDB API](https://www.themealdb.com/api.php)
- 🥦 **Veg / Non-Veg / Desserts filtering**, with a classic green/red/mustard diet-mark indicator on every recipe card
- 🍳 **Category browsing** (Seafood, Pasta, Breakfast, and more)
- 📋 **Full recipe detail view** — ingredients with measurements, numbered cooking steps, and an embedded YouTube tutorial when available
- ✅ **Interactive ingredient checklist** — tap to check off items as you cook
- 🔢 **Client-side pagination** (12 recipes per page)
- 📱 **Fully responsive** — works cleanly from mobile to desktop

## Tech Stack

| Layer | Tech |
|---|---|
| UI | React 18 (via CDN, no build tooling) |
| Styling | Hand-written CSS (custom design system, no framework) |
| Data | [TheMealDB](https://www.themealdb.com/api.php) free public API |
| Fonts | Fraunces, Public Sans, JetBrains Mono (Google Fonts) |

React and Babel are loaded directly via `<script>` tags from unpkg, and JSX is compiled in-browser — so the entire app lives in a single `.html` file.

## Getting Started

No installation required.

1. Download `food-app.html`
2. Open it in any modern browser (Chrome, Firefox, Edge, Safari)

That's it — the app fetches live data from TheMealDB as soon as it loads.

> **Note:** an internet connection is required since recipes, images, and videos are fetched live from the API.

## How It Works

- **Search bar** — hits `search.php?s={query}` on TheMealDB and renders matching recipes
- **Category chips** — hit `filter.php?c={category}` for category-based browsing
- **Veg / Non-Veg / Desserts tabs** — group TheMealDB categories into three buckets:
  - Veg → `Vegetarian`, `Vegan`
  - Non-Veg → `Chicken`, `Beef`, `Lamb`, `Pork`, `Seafood`, `Goat`
  - Desserts → `Dessert`
- **Recipe modal** — hits `lookup.php?i={id}` to fetch full ingredients, instructions, and a YouTube video link, parsed and rendered client-side

## Project Structure

```
food-app.html   → entire app: markup, styles, and React logic in one file
README.md       → this file
```

## Credits

- Recipe data, images, and videos courtesy of [TheMealDB](https://www.themealdb.com/)
- Built with React

## License

Free to use, modify, and share for portfolio or learning purposes.
