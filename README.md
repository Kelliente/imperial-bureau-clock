# Galactic Clock

A Star Wars-themed retro-futuristic clock display with live weather, Aurebesh typography, and animated dashboard readouts. Built as a single HTML file — no install, no dependencies, no accounts needed.

Happy May the 4th.

## Quick Start

Open `index.html` in any browser. That's it. The clock shows your local time automatically, and weather is detected from your approximate location via IP.

## Saving to an iPad (or Any Tablet)

The easiest way to run this as a dedicated clock face on an iPad:

1. Host the file anywhere accessible by URL. Free options: drop it in a GitHub repo and enable GitHub Pages, deploy to Netlify or Vercel, or use any static file host.
2. Open the URL in Safari on your iPad.
3. Tap the **Share** button (square with arrow), then tap **Add to Home Screen**.
4. Name it whatever you want and tap **Add**.
5. Open it from your home screen — it launches fullscreen with no browser chrome, just the clock.
6. Turn off Auto-Lock in Settings > Display & Brightness to keep it on as a permanent display.

Alternatively, if you don't want to host it: email yourself the `index.html` file, open it on your iPad, and save it to Files. Open it from Files in Safari, then follow steps 3-6 above. Weather won't work from a local file since it needs network access for the API, but the clock and all themes will function.

## Themes

Seven themes are included. Tap the faction logo in the bottom-right corner to cycle through them, or jump directly via URL parameter:

| Theme | URL param | Color |
|---|---|---|
| Imperial | `?theme=imperial` | Gold |
| Rebel Alliance | `?theme=rebel` | Blue |
| Fulcrum | `?theme=fulcrum` | Burnt orange |
| Mandalorian | `?theme=mandalorian` | Green |
| Phoenix Squadron | `?theme=vaporwave` | Pink |
| Jedi Temple | `?theme=jedi` | White |
| Outlaws | `?theme=outlaws` | Cyan/yellow |

## Weather

Weather is provided by the free Open-Meteo API (no API key required).

**Automatic:** Your approximate location is detected via IP address. US visitors see Fahrenheit; everyone else sees Celsius. No location permission prompts.

**Manual override:** For more precise weather, add your coordinates to the URL:

```
?lat=40.71&lon=-74.01
```

To find your coordinates: search your city on Google Maps, right-click any spot, and the lat/lon appears at the top of the menu.

You can combine parameters:

```
?theme=rebel&lat=51.51&lon=-0.13&units=c
```

**Units override:** Force Fahrenheit or Celsius regardless of locale:

```
?units=f
?units=c
```

**If weather shows dashes:** The IP geolocation service may be blocked or unavailable. Use the manual `lat`/`lon` parameters as a fix.

## What Everything on the Screen Means

The dashboard is cosmetic flavor inspired by Star Wars computer terminals. The elements that show real data are: the clock (your local time), the date, the day of the week, and the temperature/weather description. Everything else — power bars, comm channels, hex readouts, sector designations, unit info — is decorative fiction that changes with each theme.

The text in the angular script is Aurebesh, the Star Wars galaxy's writing system. The line below the day of the week shows the Galactic Standard Calendar equivalent (e.g., "primeday" for Thursday).

## Credits

Fonts: Aurebesh (CDNFonts), Orbitron, Share Tech Mono (Google Fonts). Faction logos: Icons8, SVG Repo. Weather data: Open-Meteo. Built with plain HTML, CSS, and JavaScript — no frameworks, no build tools.
