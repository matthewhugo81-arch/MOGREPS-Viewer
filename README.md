# MOGREPS Viewer

A browser-based viewer for Met Office MOGREPS-G ensemble imagery hosted by TheWeatherOutlook.

## Features

- Nine line-graph variables across 32 UK and European locations.
- Eight postage-stamp variables, including rain, snow, wind gusts and pressure.
- Two-panel stamp comparison with independent variables and shared forecast time and model run.
- Latest, 00Z, 06Z, 12Z and 18Z run selection.
- Three-hour forecast steps from 0 to 198 hours, with animation and time shortcuts.
- Full-screen viewing with automatic chart resizing.
- Collapsible chart selections and fit-width, whole-chart and original-size viewing.
- Chart selections and viewing preferences retained in the URL.

## Run locally

This is a static HTML, CSS and JavaScript app with no build step or package dependencies.

Serve the `dist` directory using a static web server. For example, with Python installed:

```sh
python -m http.server 4173 --directory dist
```

Then visit http://localhost:4173.

## Deploy

Publish the contents of `dist` using any static hosting service. The existing hosted viewer is at https://mogreps-chart-desk.matthugo81.chatgpt.site and may require owner sign-in.

## Source imagery

Images load directly from TheWeatherOutlook; this repository does not contain copies of the weather charts. Charts retain their source timestamps and attribution. Run directories update in place and are not an archive. Some images may be unavailable while the source updates.

- Source viewer: https://www.theweatheroutlook.com/twodata/mogreps.aspx
- Charts: TheWeatherOutlook
- Forecast data: Met Office

Third-party imagery retains its original rights and attribution.

## Files

- `dist/index.html` — viewer layout and controls
- `dist/style.css` — responsive styling
- `dist/app.js` — chart catalogue, URL selection, animation and image sizing

This export matches the deployed source at commit `83d5808d4bb1d4ebf3c060c75131242cdd07b3d0`. Hosting account configuration is managed separately.

