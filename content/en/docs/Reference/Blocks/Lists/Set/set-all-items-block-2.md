---
title: "Set All Items"
linkTitle: "Set All Items"
description: "Sets all items in a List to a new value."
---

![Icon](/blocks/lists-set-block-icon.png)

# {{< param title >}}

<p class="namespace">(Cortex.Blocks.Lists.Set.SetAllItems`2)</p>

## Description

Sets all items in a [List][List Property] to a [New Value][NewValue Property].

## Examples

### Set all items in a List to a New Value

This example will set all items in `["Some Text", 1]` to `"New Value"`.

#### Properties

| Property           | Value                     | Notes                                    |
|--------------------|---------------------------|------------------------------------------|
| [List][List Property] | `($)List`, with value `["Some Text", 1]` | `($)List` is a variable of type [IList][]&lt;[dynamic][]&gt; |
| [New Value][NewValue Property] | `($)NewValue`, with value `"New Value"` | `($)NewValue` is a variable of type [String] |

#### Result

Setting all items in `["Some Text", 1]` to `"New Value"` results in the variable `($)List` being updated to the following:

```json
["New Value", "New Value"]
```

***

## Properties

### List

The [List][List Property] to set all items in.  

[List][List Property] can be any [IList][]&lt;[TItem][]&gt;, where [TItem][] represents the type of items in the [List][List Property].
  
| | |
|--------------------|---------------------------|
| Data Type | [IList][]&lt;[TItem][]&gt; |
| Property Type | [InputOutput][] |
| Default Value | `($)List` with value `[]` |

### New Value

The [New Value][NewValue Property] to set all items in [List][List Property] to.  
  
| | |
|--------------------|---------------------------|
| Data Type | [TItem][] |
| Property Type | [Input][] |
| Default Value | `($)NewValue` with value `null` |

## Exceptions

The exceptions thrown by the block can be found below:

| Name     | Description |
|----------|-------------|
| [CannotModifyReadOnlyListException][] | Thrown when [List][List Property] is read-only. |
| [InvalidPropertyValueException][] | Thrown when [New Value][NewValue Property] is `null` and [List][List Property] only accepts non-nullable value types. |
| [PropertyNullException][] | Thrown when [List][List Property] is `null`. |

## Remarks

### Empty List

If [List][List Property] is empty (i.e. `[]`) there is nothing to set, so no operation is performed.

### Defining lists using literal syntax

For information about how to define lists using literal syntax, see [List Literals][].

### Defining lists using expression syntax

For information about how to define lists using expression syntax, see [List Expressions][].

### Lists containing items of a single data type vs multiple data types

For information about the different types of lists, including those that can contain only a single type of item, and those that can contain multiple types of item, see [Lists][].

[List Property]: {{< ref "#list" >}}
[NewValue Property]: {{< ref "#new-value" >}}

[InputOutput]: {{< url "Cortex.Reference.Concepts.PropertyType.InputOutput" >}}
[Input]: {{< url "Cortex.Reference.Concepts.PropertyType.Input" >}}

[List Literals]: {{< url "Cortex.Reference.Concepts.LiteralVariablesExpressions.ListLiterals" >}}
[List Expressions]: {{< url "Cortex.Reference.Concepts.LiteralVariablesExpressions.ListExpressions" >}}
[Lists]: {{< url "Cortex.Reference.DataTypes.MostCommon.Lists" >}}

[TItem]: {{< url "Cortex.Reference.Concepts.Generics.MainDoc" >}}

[CannotModifyReadOnlyListException]: {{< url "Cortex.Reference.Exceptions.Lists.CannotModifyReadOnlyListException.MainDoc" >}}
[InvalidPropertyValueException]: {{< url "Cortex.Reference.Exceptions.Common.Property.InvalidPropertyValueException.MainDoc" >}}
[PropertyNullException]: {{< url "Cortex.Reference.Exceptions.Common.Property.PropertyNullException.MainDoc" >}}

[IList]: {{< url "Cortex.Reference.DataTypes.MostCommon.IList" >}}
[Dynamic]: {{< url "Cortex.Reference.DataTypes.MostCommon.Dynamic" >}}
[String]: {{< url "Cortex.Reference.DataTypes.MostCommon.String" >}}