# Smart Close Cover

Helper script to intelligently close a cover entity when the sun is below the horizon after waiting for its window to be
closed. Useful in time-based cover automations.

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgitea.marquis.site%2FHomeAssistant%2Fblueprints%2Fscripts%2Fsmart_close_cover%2Fsmart_close_cover.yaml)

## General

This script chains a window entity to a cover for the action of closing the cover once if the sun is down. You can
optionally specify extra actions to be executed once the cover starts closing for example to activate a scene or send a
notification. If the window hasn't been closed after a configurable period of 14 hours, the script execution is,
canceled because the sun is probably up again.

## Inputs

| Name               | Description                                                                          | Default |
|--------------------|--------------------------------------------------------------------------------------|---------|
| Cover Entity       | **Required.** The cover entity to close                                              |         |
| Window Entity      | **Required.** The window to wait for if open at the time this script is triggered    |         |
| Close Duration (s) | The duration in seconds that the window needs to be closed before the cover is reset | `4`     |
| extra_actions      | Extra Actions to run when the cover starts closing                                   |         |
