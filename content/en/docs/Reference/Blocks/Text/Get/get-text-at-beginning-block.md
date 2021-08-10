---
title: "Get Text At Beginning"
linkTitle: "Get Text At Beginning"
description: "Gets a length of text from the beginning of a given text."
---

![Icon](/blocks/text-get-block-icon.png)

# {{< param title >}}

<p class="namespace">(Cortex.Blocks.Text.Get.GetTextAtBeginningBlock)</p>

## Description

Gets a [Length][Length Property] of [text][TextAtBeginning Property] from the beginning of a given [Text][Text Property].

## Examples

### Get a Length of text from the beginning of a given Text

This example will get the first `3` characters from the beginning of `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"`.

#### Properties

| Property           | Value                     | Notes                                    |
|--------------------|---------------------------|------------------------------------------|
| [Text][Text Property] | `($)Text`, with value `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` | `($)Text` is a variable of type [String][] |
| [Length][Length Property] | `($)Length`, with value `3` | `($)Length` is a variable of type [Int32][] |
| [Text At Beginning][TextAtBeginning Property] | `($)TextAtBeginning`, with no value | `($)TextAtBeginning` is a variable that will be set to a [String][] |

#### Result

Getting the first `3` characters from the beginning of `"ABCDEFGHIJKLMNOPQRSTUVWXYZ"` results in the variable `($)TextAtBeginning` being updated to the following:

```json
"ABC"
```

***

## Properties

### Text

The [Text][Text Property] to get the [Text At Beginning][TextAtBeginning Property] from.  
  
| | |
|--------------------|---------------------------|
| Data Type | [String][] |
| Property Type | [Input][] |
| Default Value | `($)Text` with value `""` |

### Length

The [Length][Length Property] of text to get.

| | |
|--------------------|---------------------------|
| Data Type | [Int32][] |
| Property Type | [Input][] |
| Default Value | `($)Length` with value `-1` |

### Text At Beginning

The [Length][Length Property] of text at the beginning of [Text][Text Property].  
  
| | |
|--------------------|---------------------------|
| Data Type | [String][] |
| Property Type | [Output][] |
| Default Value | `($)TextAtBeginning` with no value |

## Exceptions

The exceptions thrown by the block can be found below:

| Name     | Description |
|----------|----------|
| [PropertyValueOutOfRangeException][] | Thrown when the [Text][Text Property] property is `null` or empty (i.e. `""`). |
| | Thrown when the [Length][Length Property] property is greater than the length of [Text][Text Property]. |

## Remarks

### Negative Length

If [Length][Length Property] is negative, the variable specified in the [Text At Beginning][TextAtBeginning Property] property will be set to the value of [Text][Text Property].

### Zero Length

If [Length][Length Property] is `0`, the variable specified in the [Text At Beginning][TextAtBeginning Property] property will be set to empty (i.e. `""`).

[Text Property]: {{< ref "#text" >}}
[Length Property]: {{< ref "#length" >}}
[TextAtBeginning Property]: {{< ref "#text-at-beginning" >}}

[Input]: {{< url "Cortex.Reference.Concepts.PropertyType.Input" >}}
[Output]: {{< url "Cortex.Reference.Concepts.PropertyType.Output" >}}

[PropertyValueOutOfRangeException]: {{< url "Cortex.Reference.Exceptions.Common.Property.PropertyValueOutOfRangeException.MainDoc" >}}

[String]: {{< url "Cortex.Reference.DataTypes.MostCommon.String" >}}
[Int32]: {{< url "Cortex.Reference.DataTypes.MostCommon.Int32" >}}