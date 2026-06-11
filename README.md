# WakaForge

WakaForge is a static web app for generating a WakaTime README stats workflow. It helps users configure README markers and a GitHub Actions YAML file for the open-source [`waka-readme-stats`](https://github.com/anmol098/waka-readme-stats) action by [`anmol098`](https://github.com/anmol098).

## Live Deployment

See the live deployment here: [https://wuisabel-gif.github.io/wakatime_forge/](https://wuisabel-gif.github.io/wakatime_forge/)

## What It Does

- Generates the README marker block:

```md
<!--START_SECTION:waka-->
<!--END_SECTION:waka-->
```

- Generates a GitHub Actions workflow for WakaTime README stats.
- Updates the YAML preview as options change.
- Shows a live README-style preview.
- Includes presets for minimal, Git-focused, and full-stat configurations.
- Supports copy buttons for generated output.
- Keeps clear attribution to the underlying GitHub Action.

## Usage

Open `index.html` in a browser.

Then:

1. Choose identity, metric, and automation options.
2. Copy the README marker block into your profile `README.md`.
3. Copy the generated YAML into:

```txt
.github/workflows/waka-stats.yml
```

4. Add these repository secrets:

```txt
WAKATIME_API_KEY
GH_TOKEN
```

5. Run the workflow from the GitHub Actions tab.

## Local Development

This project is currently a single static HTML file.

```txt
index.html
```

There is no build step required. You can edit the file directly and refresh the browser.

For a local server:

```bash
python3 -m http.server 4173
```

Then open:

```txt
http://localhost:4173
```

## Project Structure

```txt
.
├── AGENTS.md
├── README.md
└── index.html
```

## Attribution

Generated workflows use:

```yaml
uses: anmol098/waka-readme-stats@master
```

WakaForge is a companion UI for configuring that action. The underlying README stats workflow is powered by [`waka-readme-stats`](https://github.com/anmol098/waka-readme-stats) by [`anmol098`](https://github.com/anmol098).

## Status

The app is usable as a static generator. Future improvements may include deeper validation, more workflow options, stronger mobile polish, and packaging the generator logic into separate source modules.
