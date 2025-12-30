# Sonos Podcast Favorites Fix

A custom Home Assistant integration that adds support for podcast favorites in the Sonos media browser.

## The Problem

Podcasts saved as favorites in the Sonos S2 app don't appear in Home Assistant's Media Browser under Sonos Favorites. This is because the `object.container.podcast` DIDL-Lite class was not mapped in the official Sonos integration.

## The Solution

This custom component adds the missing podcast type mappings, allowing podcast favorites to appear in a "Podcast" folder within Media Browser → Sonos → Favorites.

## Installation

### HACS (Recommended)

1. Open HACS in Home Assistant
2. Click on "Integrations"
3. Click the three dots menu (top right) → "Custom repositories"
4. Add this repository URL: `https://github.com/divers33/sonos-podcast-fix`
5. Select category: "Integration"
6. Click "Add"
7. Search for "Sonos Podcast Fix" and install it
8. Restart Home Assistant

### Manual Installation

1. Download the latest release
2. Extract and copy the `custom_components/sonos` folder to your Home Assistant `config/custom_components/` directory
3. Restart Home Assistant

## Usage

After installation and restart, navigate to:
**Media Browser → Sonos → Favorites**

You should now see a "Podcast" folder containing your podcast favorites from the Sonos S2 app.

## Upstream PR

This fix has been submitted to the official Home Assistant core repository:
- PR: https://github.com/home-assistant/core/pull/159961
- Related issues: #138846, #124811

Once the PR is merged and released, you can uninstall this custom component.

## License

This project is licensed under the Apache License 2.0 - the same license as Home Assistant.
