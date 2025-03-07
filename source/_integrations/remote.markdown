---
title: Remote
description: Instructions on how to setup your remotes with Home Assistant.
ha_release: 0.34
ha_domain: remote
ha_category:
  - Remote
ha_quality_scale: internal
ha_codeowners:
  - '@home-assistant/core'
ha_integration_type: entity
---

Keeps track of the remotes in your environment. Captures their state and allows you to control them.

- Maintains a state per remote and a combined state `all_remotes`.
- Registers actions `remote/turn_on`, `remote/turn_off`, `remote/toggle`, and `remote/send_command` to control remotes.

{% include integrations/building_block_integration.md %}

### Use the actions

Go to the **Developer Tools** and open the **Actions** tab. From the **Actions** dropdown, choose `remote/turn_on`, `remote/turn_off`, or `remote/toggle`. Under target, select the target device. If you are in YAML mode, enter something like the sample below into the **Data** field. Once you are done, select **Perform action**.

```json
{"entity_id":"remote.family_room"}
```

| Data attribute | Optional | Description                                     |
| -------------- | -------- | ----------------------------------------------- |
| `entity_id`    | yes      | Only act on a specific remote, else target all. |

See the platform documentation for each type of remote for more detailed examples.
