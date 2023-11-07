---
title: Comparison Map (Data Type)
date: 2023-11-08
---
# Comparison Map

[Data Type](../data_types.md).

Either a singular or an [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of an [Object](https://origins.readthedocs.io/en/latest/types/data_types/object/) with both a `comparison` field and a `compare_to` field.

### Inner Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`comparison` | [Comparison](https://origins.readthedocs.io/en/latest/types/data_types/comparison/) | | How the value should be compared. 
`compare_to` | A Numerical Type |  | The value that is compared.

### Examples:
```json
[
    {
        "comparison": ">",
        "compare_to": 2
    },
    {
        "comparison": "<",
        "compare_to": 10
    }
]
```
This example checks for if a value is greater than 2 and less than 10.