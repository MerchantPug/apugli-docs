---
title: Packet (Entity Action Type)
date: 2022-03-04
---

# Packet

[Meta Action Type](../meta_action_types.md)

Executes an action on a specified side, opposite to the one which the action is ran on.

Type ID: `apugli:packet`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`side` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/) | | Determines the side at which the packet will be sent to. Accepts either `"client"` or `"server"`
`action` | [Bi-entity or Entity Action](https://origins.readthedocs.io/en/latest/types/action_types/) | The action to run inside the packet. The type of this action must match where the packet action is being ran.

### Examples
```json
"entity_action": {
    "type": "toomanyorigins:packet",
    "side": "SERVER",
    "action": {
        "type": "origins:exhaust",
        "amount": 0.1
    }
}
```
If ran on the client, this example action will exhaust the player for a value of `0.1` on the server.