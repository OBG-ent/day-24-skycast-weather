# SkyCast 🌦️

**A live weather command center powered by the Open-Meteo API — no account, no API key, just real data for any city on Earth.**

Weather apps bury the useful numbers under ads and upsells. SkyCast pulls **live data straight from the Open-Meteo API** — the same free, keyless API used by developers worldwide — and renders it as a clean dashboard: current conditions, a 24-hour temperature/rain chart, and a 7-day outlook.

## ✨ Features

- 🔎 **Live city search** — debounced autocomplete against the Open-Meteo Geocoding API, with region and country disambiguation
- 🌡️ **Current conditions hero** — temperature, feels-like, humidity, wind, pressure, today's range, sunrise/sunset
- 🕐 **24-hour chart** — hand-drawn Canvas line for temperature with rain-probability bars behind it
- 📅 **7-day outlook** — highs, lows, conditions, and UV index max for every day
- 📍 **"Use my location"** — browser Geolocation straight into the forecast endpoint
- ⭐ **Saved cities** — pin cities as chips (persisted in `localStorage`), click to switch, ✕ to remove
- 🔁 **°C / °F toggle** — converts every number on the page, remembered between visits
- 🛡️ **Real error handling** — failed fetches and denied location permissions surface as readable status messages, not blank pages

## 🚀 Run it in 30 seconds

No build tools, no server needed — you just need an internet connection for the live API:

1. Download or clone this repo
2. Double-click **`index.html`** — that's it

**Try this:** search for **Nairobi**, then pin **Toronto** beside it and flip between them — winter coats vs. t-shirt weather, two clicks apart. Then hit **°F** and watch the whole dashboard convert.

## 🧠 What I practiced

- The Fetch API with `async` patterns, HTTP error checks, and `.catch()` recovery paths
- Working with a real third-party REST API — query params, JSON shape discovery, WMO weather-code mapping
- Debounced input for search-as-you-type (280ms) so the API isn't hammered on every keystroke
- Canvas rendering — scaled line charts, proportional bar overlays, axis labels
- Geolocation API with graceful denial handling
- `localStorage` for saved cities and unit preference

## 🔌 APIs used (both free, no key required)

| Endpoint | Purpose |
|---|---|
| `geocoding-api.open-meteo.com/v1/search` | City name → coordinates |
| `api.open-meteo.com/v1/forecast` | Current, hourly, and daily weather |

## 🗂️ Project structure

```
day-24-skycast-weather/
├── index.html   # the whole app — markup, styles, and logic in one file
└── README.md
```

---

Day 24 of my daily coding streak — one simple build and one bigger build, every day. Follow along: [@Reynoldobago](https://x.com/Reynoldobago) · [github.com/OBG-ent](https://github.com/OBG-ent)
