---
title: "Remove Items At End"
linkTitle: "Remove Items At End"
description: "Removes a count of items from the end of a List."
---

![Icon](/blocks/lists-remove-block-icon.png)

# {{< param title >}}

<p class="namespace">(Cortex.Blocks.Lists.RemoveItem.RemoveItemsAtEndBlock`2)</p>

## Description

Removes the specified [Count][Count Property] of items from the end of a [List][List Property].

## Examples

### Remove Count of items from the end of a List

This example will remove `2` items from the end of `["Some Text", 1, "Some More Text", 2]`.

#### Properties

| Property           | Value                     | Notes                                    |
|--------------------|---------------------------|------------------------------------------|
| [List][List Property] | `($)List`, with value `["Some Text", 1, "Some More Text", 2]` | `($)List` is a variable of type [IList][]&lt;[dynamic][]&gt; |
| [Count][Count Property] | `($)Count`, with value `2` | `($)Count` is a variable of type [Int32][] |

#### Result

Removing `2` items from the end of `["Some Text", 1, "Some More Text", 2]` results in the variable `($)List` being updated to the following:

```json
["Some Text", 1]
```

***

## Properties

### List

The [List][List Property] where the items are removed from.  

[List][List Property] can be any [IList][]&lt;[TItem][]&gt;, where [TItem][] represents the type of items that can be removed from the [List][List Property].
  
| | |
|--------------------|---------------------------|
| Data Type | [IList][]&lt;[TItem][]&gt; |
| Property Type | [InputOutput][] |
| Default Value | `($)List` with value `[]` |

### Count

The [Count][Count Property] of items to remove.

| | |
|--------------------|---------------------------|
| Data Type | [Int32][] |
| Property Type | [Input][] |
| Default Value | `($)Count` with value `0` |

## Exceptions

The exceptions thrown by the block can be found below:

| Name     | Description |
|----------|----------|
| [CannotModifyReadOnlyListException][] | Thrown when [List][List Property] is read-only. |
| [PropertyNullException][] | Thrown when [List][List Property] is `null`. |
| [PropertyValueOutOfRangeException][] | Thrown when [Count][Count Property] is greater than the count of items in the [List][List Property] - `1`. |

## Remarks

### Negative Count

If [Count][Count Property] is negative all items in the [List][List Property] are removed.

### Zero Count

If [Count][Count Property] is `0` there is nothing to remove, so no operation is performed.

### Defining lists using literal syntax

For information about how to define lists using literal syntax, see [List Literals][].

### Defining lists using expression syntax

For information about how to define lists using expression syntax, see [List Expressions][].

### Lists containing items of a single data type vs multiple data types

For information about the different types of lists, including those that can contain only a single type of item, and those that can contain multiple types of item, see [Lists][].

[List Property]: {{< ref "#list" >}}
[Count Property]: {{< ref "#count" >}}

[InputOutput]: {{< url "Cortex.Reference.Concepts.PropertyType.InputOutput" >}}
[Input]: {{< url "Cortex.Reference.Concepts.PropertyType.Input" >}}

[List Literals]: {{< url "Cortex.Reference.Concepts.LiteralVariablesExpressions.ListLiterals" >}}
[List Expressions]: {{< url "Cortex.Reference.Concepts.LiteralVariablesExpressions.ListExpressions" >}}
[Lists]: {{< url "Cortex.Reference.DataTypes.MostCommon.Lists" >}}

[TItem]: {{< url "Cortex.Reference.Concepts.Generics.MainDoc" >}}

[CannotModifyReadOnlyListException]: {{< url "Cortex.Reference.Exceptions.Lists.CannotModifyReadOnlyListException.MainDoc" >}}
[PropertyNullException]: {{< url "Cortex.Reference.Exceptions.Common.Property.PropertyNullException.MainDoc" >}}
[PropertyValueOutOfRangeException]: {{< url "Cortex.Reference.Exceptions.Common.Property.PropertyValueOutOfRangeException.MainDoc" >}}

[IList]: {{< url "Cortex.Reference.DataTypes.MostCommon.IList" >}}
[Dynamic]: {{< url "Cortex.Reference.DataTypes.MostCommon.Dynamic" >}}
[Int32]: {{< url "Cortex.Reference.DataTypes.MostCommon.Int32" >}}