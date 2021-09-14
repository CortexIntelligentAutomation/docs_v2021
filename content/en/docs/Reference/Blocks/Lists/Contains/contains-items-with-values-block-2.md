---
title: "Contains Items With Values"
linkTitle: "Contains Items With Values"
description: "Checks if a List contains at least one item matching each of the specified values."
---

![Icon](/blocks/lists-contains-block-icon.png)

# {{< param title >}}

<p class="namespace">(Cortex.Blocks.Lists.Contains.ContainsItemsWithValuesBlock`2)</p>

## Description

Checks if [List][List Property] contains at least one item matching each of the specified [Values][Values Property].

## Examples

### List contains items with Values

This example will check whether `[1, 2, 3, 3, 2, 1]` contains at least one item matching each of the values in `[1, 2, 3]`.

#### Properties

| Property           | Value                     | Notes                                    |
|--------------------|---------------------------|------------------------------------------|
| [List][List Property] | `($)List`, with value `[1, 2, 3, 3, 2, 1]` | `($)List` is a variable of type [IList][]&lt;[Int32][]&gt; |
| [Values][Values Property] | `($)Values`, with value `[1, 2, 3]` | `($)Values` is a variable of type [IEnumerable][]&lt;[Int32][]&gt; |
| [Contains Items][ContainsItems Property] | `($)ContainsItems`, with no value | `($)ContainsItems` is a variable that will be set to a [Boolean][] value |

#### Result

`[1, 2, 3, 3, 2, 1]` contains at least one item matching each of the values in `[1, 2, 3]`; it contains two items with the value `1`, two items with the value `2` and two items with the value `3`. Therefore, the variable `($)ContainsItems` will be updated to the following:

```json
true
```

***

### List does not contain items with Values

This example will check whether `[1, 2, 3, 3, 2, 1]` contains at least one item matching each of the values in `[1, 2, 3, 10]`.

#### Properties

| Property           | Value                     | Notes                                    |
|--------------------|---------------------------|------------------------------------------|
| [List][List Property] | `($)List`, with value `[1, 2, 3, 3, 2, 1]` | `($)List` is a variable of type [IList][]&lt;[Int32][]&gt; |
| [Values][Values Property] | `($)Values`, with value `[1, 2, 3, 10]` | `($)Values` is a variable of type [IEnumerable][]&lt;[Int32][]&gt; |
| [Contains Items][ContainsItems Property] | `($)ContainsItems`, with no value | `($)ContainsItems` is a variable that will be set to a [Boolean][] value |

#### Result

`[1, 2, 3, 3, 2, 1]` does not contain at least one item matching each of the values in `[1, 2, 3, 10]`; it contains two items with the value `1`, two items with the value `2` and two items with the value `3`, but no items with the value `10`. Therefore, the variable `($)ContainsItems` will be updated to the following:

```json
false
```

***

## Properties

### List

The [List][List Property] to check whether it contains at least one item matching each of the specified [Values][Values Property].

Items are considered matching if they have a value matching one of the specified [Values][Values Property].

[List][List Property] can be any [IList][]&lt;[TItem][]&gt;, where [TItem][] represents the type of items in the [List][List Property].
  
| | |
|--------------------|---------------------------|
| Data Type | [IList][]&lt;[TItem][]&gt; |
| Property Type | [Input][] |
| Default Value | `($)List` with value `[]` |

### Values

The [Values][Values Property] to check for matching items.

For information and examples of how it is determined whether an item matches a specified value, please see [Object Equality][].

| | |
|--------------------|---------------------------|
| Data Type | [IEnumerable][]&lt;[TItem][]&gt; |
| Property Type | [Input][] |
| Default Value | `($)Values` with value `[]` |

### Contains Items

The result of the contains items check.

If [List][List Property] contains at least one item matching each of the specified [Values][Values Property], the specified variable will be set to `true`, otherwise it will be set to `false`.

| | |
|--------------------|---------------------------|
| Data Type | [Boolean][] |
| Property Type | [Output][] |
| Default Value | `($)ContainsItems` with no value |

## Exceptions

The exceptions thrown by the block can be found below:

| Name     | Description |
|----------|----------|
| [PropertyNullException][] | Thrown when [List][List Property] or [Values][Values Property] are `null`. |

## Remarks

### Object Equality

For information and examples of how it is determined whether an item matches a specified value, please see [Object Equality][].

### Empty List

If [List][List Property] is empty (i.e. `[]`), the variable specified in the [Contains Items][ContainsItems Property] property is set to `false`.

### Empty Values

If [Values][Values Property] is empty (i.e. `[]`), the variable specified in the [Contains Items][ContainsItems Property] property is set to `false`.

### Defining lists using literal syntax

For information about how to define lists using literal syntax, see [List Literals][].

### Defining lists using expression syntax

For information about how to define lists using expression syntax, see [List Expressions][].

### Lists containing items of a single data type vs multiple data types

For information about the different types of lists, including those that can contain only a single type of item, and those that can contain multiple types of item, see [Lists][].

[List Property]: {{< ref "#list" >}}
[Values Property]: {{< ref "#values" >}}
[ContainsItems Property]: {{< ref "#contains-items" >}}

[Input]: {{< url "Cortex.Reference.Concepts.PropertyType.Input" >}}
[Output]: {{< url "Cortex.Reference.Concepts.PropertyType.Output" >}}

[List Literals]: {{< url "Cortex.Reference.Concepts.LiteralVariablesExpressions.ListLiterals" >}}
[List Expressions]: {{< url "Cortex.Reference.Concepts.LiteralVariablesExpressions.ListExpressions" >}}
[Lists]: {{< url "Cortex.Reference.DataTypes.MostCommon.Lists" >}}

[TItem]: {{< url "Cortex.Reference.Concepts.Generics.MainDoc" >}}

[Object Equality]: {{< url "Cortex.Reference.Concepts.ObjectEquality.MainDoc" >}}

[PropertyNullException]: {{< url "Cortex.Reference.Exceptions.Common.Property.PropertyNullException.MainDoc" >}}

[IList]: {{< url "Cortex.Reference.DataTypes.MostCommon.IList" >}}
[IEnumerable]: {{< url "Cortex.Reference.DataTypes.MostCommon.IEnumerable" >}}
[Boolean]: {{< url "Cortex.Reference.DataTypes.MostCommon.Boolean" >}}
[Int32]: {{< url "Cortex.Reference.DataTypes.MostCommon.Int32" >}}