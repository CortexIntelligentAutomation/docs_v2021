---
title: "Throw New Flow Exception"
linkTitle: "Throw New Flow Exception"
description: "Throws a new FlowException with the specified message, category, error code, details, inner exception and help link."
---

![Icon](/blocks/exceptions-throw-block-icon.png)

# {{< param title >}}

<p class="namespace">(Cortex.Blocks.Exceptions.Throw.ThrowNewFlowExceptionBlock)</p>

## Description

Throws a new [FlowException][] with the specified [Message][Message Property], [Category][Category Property], [Error Code][ErrorCode Property], [Details][Details Property], [Inner Exception][InnerException Property] and [Help Link][HelpLink Property].

All properties are optional, and if not supplied will be set to the following default values:

| Property           | Default Value                     |
|--------------------|-----------------------------------|
| [Message][Message Property] | `"Exception of type 'Cortex.Exceptions.FlowException' was thrown."` |
| [Category][Category Property] | `null` |
| [Error Code][ErrorCode Property] | `0` |
| [Details][Details Property] | `null`|
| [InnerException][InnerException Property] | `null` |
| [HelpLink][HelpLink Property] | `https://v2022.docs.cortex-ia.com/docs/reference/exceptions/flowexception` |

## Examples

### Throw new FlowException with full configuration

This example will throw a new [FlowException][] with all properties configured.

#### Properties

| Property           | Value                     | Notes                                    |
|--------------------|---------------------------|------------------------------------------|
| [Message][Message Property] | `($)Message`, with value `"Custom Message"` | `($)Message` is a variable of type [String][] |
| [Category][Category Property] | `($)Category`, with value `"Custom Category"` | `($)Category` is a variable of type [String][] |
| [Error Code][ErrorCode Property] | `($)ErrorCode`, with value `100` | `($)ErrorCode` is a variable of type [Int32][] |
| [Details][Details Property] | `($)Details`, with value `{"DetailsKey1" : "DetailsValue1", "DetailsKey2" : "DetailsValue2"}` | `($)Details` is a variable of type [IDictionary][]&lt;[String][], [String][]&gt; |
| [InnerException][InnerException Property] | `($)InnerException`, with value `($)Exception` containing another [FlowException][] with default properties | `($)InnerException` is a variable of type [FlowException][] |
| [HelpLink][HelpLink Property] | `($)HelpLink`, with value `"http://customdomain.com/customurl"` | `($)HelpLink` is a variable of type [String][] |

#### Result

Throwing a new [FlowException][] with properties configured as above will result in the following exception:

![Icon](/images/flow-exception-full-configuration.png)<br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/>

***

### Throw new FlowException with no configuration

This example will throw a new [FlowException][] with no configuration.

#### Properties

No properties are configured for this example.

#### Result

Throwing a new [FlowException][] without configuring any of the block's properties will result in the following exception:

![Icon](/images/flow-exception-no-configuration.png)<br/><br/><br/><br/><br/><br/>

***

## Properties

### Message

A [Message][Message Property] describing the exception that occurred.

If [Message][Message Property] is not provided or is set to `null`, it will default to `"Exception of type 'Cortex.Exceptions.FlowException' was thrown."`.

| | |
|--------------------|---------------------------|
| Data Type | [String][] |
| Property Type | [Input][] |
| Default Value | `($)Message` with value `null` |

### Category

A [Category][Category Property] that can be used to categorise similar types of exception that has occurred (e.g. an `AuthenticationError` category may be set for exceptions relating to authentication issues). This can then be used for future decision making in the flow, or to assist in troubleshooting and reporting.

| | |
|--------------------|---------------------------|
| Data Type | [String][] |
| Property Type | [Input][] |
| Default Value | `($)Category` with value `null` |

### Error Code

An [Error Code][ErrorCode Property] that can be used to uniquely identify the type of exception (e.g. There may be multiple exceptions with the same `AuthenticationError` category set, such as `InvalidCredentials`, `TokenExpired`. In this case each exception can be assigned its own unique [Error Code][ErrorCode Property]; `AuthenticationError` = `100` and `InvalidCredentials` = `101`). This can then be used for future decision making in the flow, or to assist in troubleshooting and reporting.

If [Error Code][ErrorCode Property] is not provided, it will default to `0`.

| | |
|--------------------|---------------------------|
| Data Type | [Int32][] |
| Property Type | [Input][] |
| Default Value | `($)ErrorCode` with value `0` |

### Details

[Details][Details Property] can be used to provide more detailed information about the exception. It can be any type of [Object][]. This can then be used for future decision making in the flow, or to assist in troubleshooting and reporting.

| | |
|--------------------|---------------------------|
| Data Type | [Dynamic][] |
| Property Type | [Input][] |
| Default Value | `($)Details` with value `null` |

### Inner Exception

[Inner Exception][InnerException Property] can be used to include another [exception][] within the thrown exception (e.g. If the [FlowException][] has been thrown as a result of handling another [exception][], then the handled [exception][] can be included within the [FlowException][] to add traceability).

| | |
|--------------------|---------------------------|
| Data Type | [Exception][] |
| Property Type | [Input][] |
| Default Value | `($)InnerException` with value `null` |

### Help Link

A [Help Link][HelpLink Property] can be specified where further information can be found about the exception being thrown.

If [Help Link][HelpLink Property] is not provided or is set to `null`, it will default to a link to the [FlowException][] page; please note this page will not provide any guidance on how to fix the solution specific [exception][].

| | |
|--------------------|---------------------------|
| Data Type | [String][] |
| Property Type | [Input][] |
| Default Value | `($)HelpLink` with value `null` |

## Exceptions

No exceptions are thrown by the block.

## Remarks

### Null Message

If [Message][Message Property] is not provided or is set to `null`, it will default to `"Exception of type 'Cortex.Exceptions.FlowException' was thrown."`.

### Null Help Link

If [Help Link][HelpLink Property] is not provided or is set to `null`, it will default to a link to the [FlowException][] page, please note this page will not provide any guidance on how to fix the solution specific [exception][].

[Message Property]: {{< ref "#message" >}}
[Category Property]: {{< ref "#category" >}}
[ErrorCode Property]: {{< ref "#error-code" >}}
[Details Property]: {{< ref "#details" >}}
[InnerException Property]: {{< ref "#inner-exception" >}}
[HelpLink Property]: {{< ref "#help-link" >}}

[Input]: {{< url "Cortex.Reference.Concepts.PropertyType.Input" >}}

[Object]: {{< url "Cortex.Reference.DataTypes.MostCommon.Object" >}}
[IDictionary]: {{< url "Cortex.Reference.DataTypes.MostCommon.IDictionary" >}}
[String]: {{< url "Cortex.Reference.DataTypes.MostCommon.String" >}}
[Int32]: {{< url "Cortex.Reference.DataTypes.MostCommon.Int32" >}}
[Dynamic]: {{< url "Cortex.Reference.DataTypes.MostCommon.Dynamic" >}}
[Exception]: {{< url "Cortex.Reference.DataTypes.MostCommon.Exception" >}}
[FlowException]: {{< url "Cortex.Reference.Exceptions.FlowException.MainDoc" >}}