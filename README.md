# Blueprints for Home-Assistant

This is our blueprint collection from our private Home Assistant instance that developed over time and have proven to be
useful.  
Use at your own risk.

## Contents

<!-- TOC -->
* [Blueprints for Home-Assistant](#blueprints-for-home-assistant)
  * [Contents](#contents)
  * [Blueprints](#blueprints)
    * [Script: Notify People](#script--notify-people)
    * [Script: Notify Person](#script--notify-person)
    * [Script: Smart Close Cover](#script--smart-close-cover)
    * [Automation: Open Cover with Window](#automation--open-cover-with-window)
<!-- TOC -->

## Blueprints

### [Script: Notify People](./scripts/notify_people)

Helper script meant as central place for sending notifications in Home Assistant. Multiple parameters available
including selecting notified people, only notifying people at home and a way to dismiss notification.

### [Script: Notify Person](./scripts/notify_person)

Helper script to notify a single person. Used to prevent the need of changing every occurrence of a notification entity
by instead only updating this script in case of a device change. Provides convenience to dismiss messages.

### [Script: Smart Close Cover](./scripts/smart_close_cover)

Helper script to intelligently close a `cover` entity when the sun is below the horizon after waiting for its `window`
to be closed. Useful in time-based cover automations.

### [Automation: Open Cover with Window](./automations/open_cover_with_window)

This is a convenience automation that connects a `window` device with a `cover` device. If the window will be opened, it
triggers the opening of the cover and returns it to the previous state when the window is closed again.
