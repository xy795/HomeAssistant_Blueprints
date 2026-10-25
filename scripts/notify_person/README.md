# Notify Person

Helper script to notify a single person. Used to prevent the need of changing every occurrence of a notification
entity by instead only updating this script in case of a device change. Provides convenience to dismiss messages.

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgitea.marquis.site%2FHomeAssistant%2Fblueprints%2Fscripts%2Fnotify_person%2Fnotify_person.yaml)

## General

The only action for this script is to call the handler function and wait for its completion.

## Inputs

| Name    | Description                                | Default |
|---------|--------------------------------------------|---------|
| Title   | The title of the notification              |         |
| Message | The message of the notification            |         |
| URL     | Url for click action target                |         |
| Tag     | Tag for replacing / clearing later on      |         |
| Group   | Group name for notification grouping       |         |
| Clear   | Removes notifications with given tag       | `false` |
| Channel | Android notification Channel               |         |
| Actions | Actions to add to mobile app notifications |         |
