---
title: Modify Scale (Power Type)
date: 2022-11-14
---

# Modify Scale

[Power Type](../power_types.md).

Modifies the entity's Pehkui scale(s).

Type ID: `apugli:modify_scale`

!!! caution

    This power will only work if the [Pehkui](https://modrinth.com/mod/pehkui/) mod is installed.

    Please don't use Apugli exclusively for this power type. Scale changes are perfectly viable by just using commands and the sort. More information on scale changing in Apoli can be found [here](https://gist.github.com/MerchantPug/1ab00a122399f77873239e1cda854dd9).


Field | Type | Default | Description
------|------|---------|------------
`scale_type` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | *optional* | If set, this scale type will be modified.
`scale_types` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Identifiers](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | *optional* | If set, these scale types will be modified.
`modifier` | [Attribute Modifier](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, this modifier that will apply to the scale value.
`modifiers` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Attribute Modifiers](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, these modifiers that will apply to the scale value.
`delay` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `0` | If set, this delay will be applied to scale changes.

### Example
```json
{
  "type": "apugli:modify_scale",
  "delay": 40,
  "scale_types": [
    "pehkui:width",
    "pehkui:height",
    "pehkui:drops"
  ],
  "modifiers": {
    "operation": "multiply_total_multiplicative",
    "value": 0.25
  }
}
```
This power will increase the entity's `pehkui:width`, `pehkui:height` and `pehkui:drops` scale by 125%. Scale changes will interpolate from the scale value prior and will take 40 ticks to completely apply.