# Notify People

Helper script meant as central place for sending notifications in Home Assistant. Multiple parameters are available
including selecting notified people, only notifying people at home and a way to dismiss notification. Has options for
handling HA persistent notifications with the same message.

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgitea.marquis.site%2FHomeAssistant%2Fblueprints%2Fscripts%2Fnotify_people%2Fnotify_people.yaml)

## General

Loops over the provided `people` items and calls their [notification script](../notify_person/README.md).  
If `home` is true, script calls for people not at home will be skipped.  
Persistent notification management can be enabled by setting `create_persistent_notification` to true. An additional
condition template can be supplied to dynamically control creation of persistent notifications with
`persistent_notification_condition`.

## Inputs

| Name                                     | Description                                                                                                  | Default      |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------|--------------|
| Title                                    | The title of the notification                                                                                |              |
| Message                                  | The message of the notification                                                                              |              |
| URL                                      | Url for click action target                                                                                  |              |
| Tag                                      | Tag for replacing / clearing later on                                                                        |              |
| Group                                    | Group name for notification grouping                                                                         |              |
| Clear                                    | Removes notifications with given tag                                                                         | `false`      |
| Channel                                  | Android notification Channel                                                                                 |              |
| Actions                                  | Actions to add to mobile app notifications                                                                   |              |
| People                                   | People to notify. Defaults to everyone.                                                                      | <everyone>   |
| Only Home                                | If true, only sends notifications to people who are at home                                                  | `false`      |
| Create persistent Notification           | If true, creates a persistent notification in Home Assistant additionally                                    | `false`      |
| Create persistent Notification Condition | Creates a persistent notification in Home Assistant only of the given condition matches. Ignored if omitted. | `{{ true }}` |
