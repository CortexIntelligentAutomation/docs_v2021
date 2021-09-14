---
title: "Get Items At Index"
linkTitle: "Get Items At Index"
description: "Gets a count of items starting at the specified index of a List."
---

![Icon](/blocks/lists-get-block-icon.png)

# {{< param title >}}

<p class="namespace">(Cortex.Blocks.Lists.Get.GetItemsAtIndexBlock`2)</p>

## Description

Gets the specified [Count][Count Property] of [Items][Items Property] starting at the given [Index][Index Property] of a [List][List Property].

## Examples

### Get Count of Items at the first Index (i.e. `0`) of a List

This example will get `2` items at index `0` of `["Some Text", 1, "Some More Text", 2]`.

#### Properties

| Property           | Value                     | Notes                                    |
|--------------------|---------------------------|------------------------------------------|
| [List][List Property] | `($)List`, with value `["Some Text", 1, "Some More Text", 2]` | `($)List` is a variable of type [IList][]&lt;[dynamic][]&gt; |
| [Index][Index Property] | `($)Index`, with value `0` | `($)Index` is a variable of type [Int32][] |
| [Count][Count Property] | `($)Count`, with value `2` | `($)Count` is a variable of type [Int32][] |
| [Items][Items Property] | `($)Items`, with no value | `($)Items` is a variable that will be set to an [IList][]&lt;[dynamic][]&gt; value |

#### Result

Getting `2` items at index `0` of `["Some Text", 1, "Some More Text", 2]` results in the variable `($)Items` being updated to the following:

```json
["Some More", 1]
```

***

## Properties

### List

The [List][List Property] to get the [Items][Items Property] from.  

[List][List Property] can be any [IList][]&lt;[TItem][]&gt;, where [TItem][] represents the type of items in the [List][List Property].
  
| | |
|--------------------|---------------------------|
| Data Type | [IList][]&lt;[TItem][]&gt; |
| Property Type | [Input][] |
| Default Value | `($)List` with value `[]` |

### Index

The [Index][Index Property] to get the [Count][Count Property] of [Items][Items Property] at.  This is an inclusive index, which means the item at the specified index will be included.

Valid values are between and including `0` and the total count of items in the [List][List Property] - `1`.

For information about what an index is, please see [Indexes][].  

| | |
|--------------------|---------------------------|
| Data Type | [Int32][] |
| Property Type | [Input][] |
| Default Value | `($)Index` with value `0` |

### Count

The [Count][Count Property] of [Items][Items Property] to get.

| | |
|--------------------|---------------------------|
| Data Type | [Int32][] |
| Property Type | [Input][] |
| Default Value | `($)Count` with value `0` |

### Items

The [Items][Items Property] at the specified [Index][Index Property] of [List][List Property].

[Items][Items Property] will be in the same order they are defined in [List][List Property].
  
| | |
|--------------------|---------------------------|
| Data Type | [IList][]&lt;[TItem][]&gt; |
| Property Type | [Output][] |
| Default Value | `($)Items` with no value |

## Exceptions

The exceptions thrown by the block can be found below:

| Name     | Description |
|----------|----------|
| [PropertyNullException][] | Thrown when [List][List Property] is `null`. |
| [PropertyValueOutOfRangeException][] | Thrown when [Index][Index Property] is less than `0` or greater than the count of items in [List][List Property] - `1`. |
| | Thrown when [Index][Index Property] + [Count][Count Property] is greater than the count of items in the [List][List Property] - `1`. |

## Remarks

### Index is inclusive

The [Index][Index Property] is an inclusive [index][Indexes], which means the item at the index will be included in [Items][Items Property].

### Negative Count

If [Count][Count Property] is negative, [Items][Items Property] contains all items after and including the item at the specified [Index][Index Property] in the [List][List Property].

### Zero Count

If [Count][Count Property] is `0`, [Items][Items Property] is set to an empty list (i.e. `[]`).

### Defining lists using literal syntax

For information about how to define lists using literal syntax, see [List Literals][].

### Defining lists using expression syntax

For information about how to define lists using expression syntax, see [List Expressions][].

### Lists containing items of a single data type vs multiple data types

For information about the different types of lists, including those that can contain only a single type of item, and those that can contain multiple types of item, see [Lists][].

[List Property]: {{< ref "#list" >}}
[Index Property]: {{< ref "#index" >}}
[Count Property]: {{< ref "#count" >}}
[Items Property]: {{< ref "#items" >}}

[Indexes]: {{< url "Cortex.Reference.Concepts.Indexes.MainDoc" >}}

[Input]: {{< url "Cortex.Reference.Concepts.PropertyType.Input" >}}
[Output]: {{< url "Cortex.Reference.Concepts.PropertyType.Output" >}}

[List Literals]: {{< url "Cortex.Reference.Concepts.LiteralVariablesExpressions.ListLiterals" >}}
[List Expressions]: {{< url "Cortex.Reference.Concepts.LiteralVariablesExpressions.ListExpressions" >}}
[Lists]: {{< url "Cortex.Reference.DataTypes.MostCommon.Lists" >}}

[TItem]: {{< url "Cortex.Reference.Concepts.Generics.MainDoc" >}}

[PropertyNullException]: {{< url "Cortex.Reference.Exceptions.Common.Property.PropertyNullException.MainDoc" >}}
[PropertyValueOutOfRangeException]: {{< url "Cortex.Reference.Exceptions.Common.Property.PropertyValueOutOfRangeException.MainDoc" >}}

[IList]: {{< url "Cortex.Reference.DataTypes.MostCommon.IList" >}}
[Dynamic]: {{< url "Cortex.Reference.DataTypes.MostCommon.Dynamic" >}}
[Int32]: {{< url "Cortex.Reference.DataTypes.MostCommon.Int32" >}}