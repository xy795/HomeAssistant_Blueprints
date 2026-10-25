# Open Cover with Window

... and resets it to its previous state when the window is closed again. This Accepts also a door instead of a window.

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgitea.marquis.site%2FHomeAssistant%2Fblueprints%2Fraw%2Fbranch%2Fmain%2Fautomations%2Fopen_cover_with_window%2Fopen_cover_with_window.yaml)

## General

This Automation uses the `cover.open_cover` to immediately open the cover when the window or door opens.  
Before touching the cover state, it is preserved in a temporary scene, which is applied and removed to restore the
cover's state.

If the automation is canceled due to home assistant stopping, it will be picked up again after boot. There is a
configurable delay to ensure all integrations and devices have initialized again.

## Inputs

| Name                    | Description                                                                                         | Default                                                     |
|-------------------------|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| Cover                   | **Required.** The cover to control                                                                  |                                                             |
| Window/Door             | **Required.** The window (or door) that controls the cover                                          |                                                             |
| Close Duration (s)      | The duration in seconds that the window needs to be closed before the cover is reset                | `4`                                                         |
| Boot Timeout (s)        | The duration in seconds how long to wait after home assistant boots to continue with the automation | `30`                                                        |
| Scene id value template | The template used for creating the scene_id used for saving and restoring the cover position        | `tmp_{{ cover \| regex_replace(find='\\.', replace='_') }}` |
