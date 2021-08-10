---
title: "Get Text Before Index"
linkTitle: "Get Text Before Index"
description: "Gets a length of text before a specified index of a given text."
---

![Icon](/blocks/text-get-block-icon.png)

# {{< param title >}}

<p class="namespace">(Cortex.Blocks.Text.Get.GetTextBeforeIndexBlock)</p>

## Description

Gets a [Length][Length Property] of [text][TextBeforeIndex Property] before a specified [Index][Index Property] of a given [Text][Text Property].

## Examples

### Get a Length of text before a specified Index of a given Text

This example will get `3` characters before index `3` of `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"`.

#### Properties

| Property           | Value                     | Notes                                    |
|--------------------|---------------------------|------------------------------------------|
| [Text][Text Property] | `($)Text`, with value `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` | `($)Text` is a variable of type [String][] |
| [Index][Index Property] | `($)Index`, with value `3` | `($)Index` is a variable of type [Int32][] |
| [Length][Length Property] | `($)Length`, with value `3` | `($)Length` is a variable of type [Int32][] |
| [Text Before Index][TextBeforeIndex Property] | `($)TextBeforeIndex`, with no value | `($)TextBeforeIndex` is a variable that will be set to a [String][] |

#### Result

`"D"` is at index `3` in `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"`. Therefore, getting `3` characters before index `3` results in the variable `($)TextBeforeIndex` being updated to the following:

```json
"ABC"
```

***

## Properties

### Text

The [Text][Text Property] to get the [Text Before Index][TextBeforeIndex Property] from.
  
| | |
|--------------------|---------------------------|
| Data Type | [String][] |
| Property Type | [Input][] |
| Default Value | `($)Text` with value `""` |

### Index

The [Index][Index Property] to get the text before. This is an exclusive index, which means the character at the specified index won't be included.

For information about what an index is, please see [Indexes][].

| | |
|--------------------|---------------------------|
| Data Type | [Int32][] |
| Property Type | [Input][] |
| Default Value | `($)Index` with value `0` |

### Length

The [Length][Length Property] of text to get.

| | |
|--------------------|---------------------------|
| Data Type | [Int32][] |
| Property Type | [Input][] |
| Default Value | `($)Length` with value `-1` |

### Text Before Index

The [Length][Length Property] of text before the [Index][Index Property] of [Text][Text Property].

| | |
|--------------------|---------------------------|
| Data Type | [String][] |
| Property Type | [Output][] |
| Default Value | `($)TextBeforeIndex` with no value |

## Exceptions

The exceptions thrown by the block can be found below:

| Name     | Description |
|----------|----------|
| [PropertyValueOutOfRangeException][] | Thrown when the [Text][Text Property] property is `null` or empty (i.e. `""`). |
| | Thrown when the [Index][Index Property] property is less than `1` or greater than the length of [Text][Text Property] - 1. |
| | Thrown when the [Index][Index Property] property - a positive [Length][Length Property] property is less than 1. |

## Remarks

### Get all text before Index

A negative [Length][Length Property] can be used to get all text before the [Index][Index Property] of [Text][Text Property].

### Index is exclusive

The [Index][Index Property] property is an exclusive [index][Indexes], which means the character at the index will not be included in the retrieved [text][TextBeforeIndex Property].

### Zero Length

If [Length][Length Property] is `0`, the variable specified in the [Text Before Index][TextBeforeIndex Property] property will be set to empty (i.e. `""`).

[Text Property]: {{< ref "#text" >}}
[Index Property]: {{< ref "#index" >}}
[Length Property]: {{< ref "#length" >}}
[TextBeforeIndex Property]: {{< ref "#text-before-index" >}}

[Indexes]: {{< url "Cortex.Reference.Concepts.Indexes.MainDoc" >}}
[Input]: {{< url "Cortex.Reference.Concepts.PropertyType.Input" >}}
[Output]: {{< url "Cortex.Reference.Concepts.PropertyType.Output" >}}

[PropertyValueOutOfRangeException]: {{< url "Cortex.Reference.Exceptions.Common.Property.PropertyValueOutOfRangeException.MainDoc" >}}

[String]: {{< url "Cortex.Reference.DataTypes.MostCommon.String" >}}
[Int32]: {{< url "Cortex.Reference.DataTypes.MostCommon.Int32" >}}