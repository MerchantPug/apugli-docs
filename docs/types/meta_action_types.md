---
title: Meta Action Types
date: 2023-08-22
---

# Meta Action Types
Meta Action Types are independent of the type they operate on. They basically combine or modify other action types. The actions which are modified have to be of the type the field of the meta action type requires. For example, if you have a field which requires an [Entity Action Type](./entity_action_types.md) and you insert a [Delay (Meta Action Type)](https://origins.readthedocs.io/en/latest/types/meta_action_types/delay/), the action type you need to provide inside that meta action type will have to be an [Entity Action Type](./entity_action_types.md) as well.

## Apugli

### Bi-entity and Entity
- [Packet](packet)