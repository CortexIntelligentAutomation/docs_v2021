---
title: "If Null Exit Right"
linkTitle: "If Null Exit Right"
description: "Checks if a given value is `null`; if so the flow execution exits via the block's right port, otherwise it exits via the bottom port."
---

![Icon](/blocks/decisions-if-true-exit-right-block-icon.png)

# {{< param title >}}

<p class="namespace">(Cortex.Blocks.Decisions.If.IfNullExitRightBlock`1)</p>

## Description

Checks if a given [Value][Value Property] is `null`; if so the flow execution exits via the block's right port (green tick), otherwise it exits via the bottom port (red cross).

For information about `null`, please see [Null and Nullable Types][].

## Examples

### Value is null

This example will check if `null` is `null`.

#### Properties

| Property           | Value                     | Notes                                    |
|--------------------|---------------------------|------------------------------------------|
| [Value][Value Property] | `($)Value`, with value `null` | `($)Value` is a variable of type [String][] |

#### Result

`null` is `null`, so the flow execution exits via the block's right port (green tick).

***

### Value is not null

This example will check if `"The quick brown fox jumps over the lazy dog"` is `null`.

#### Properties

| Property           | Value                     | Notes                                    |
|--------------------|---------------------------|------------------------------------------|
| [Value][Value Property] | `($)Value`, with value `"The quick brown fox jumps over the lazy dog"` | `($)Value` is a variable of type [String][] |

#### Result

`"The quick brown fox jumps over the lazy dog"` is not `null`, so the flow execution exits via the block's bottom port (red cross).

***

## Properties

### Value

The [Value][Value Property] to check is `null`.

For information about `null`, please see [Null and Nullable Types][].

| | |
|--------------------|---------------------------|
| Data Type | [TValue][] |
| Property Type | [Input][] |
| Default Value | `($)Value` with value `null` |

## Exceptions

The exceptions thrown by the block can be found below:

| Name     | Description |
|----------|----------|
| [PropertyNotNullableException][] | Thrown when [Value][Value Property] is given a non-nullable value type. |

## Remarks

### Null and Nullable Types

For information about `null`, please see [Null and Nullable Types][].

[Value Property]: {{< ref "#value" >}}

[Input]: {{< url "Cortex.Reference.Concepts.PropertyType.Input" >}}

[TValue]: {{< url "Cortex.Reference.Concepts.Generics.MainDoc" >}}
[Null and Nullable Types]: {{< url "Cortex.Reference.Concepts.NullAndNullableTypes.MainDoc" >}}

[PropertyNotNullableException]: {{< url "Cortex.Reference.Exceptions.Decisions.PropertyNotNullableException.MainDoc" >}}

[String]: {{< url "Cortex.Reference.DataTypes.MostCommon.String" >}}