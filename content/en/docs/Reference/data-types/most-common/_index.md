---
title: "Most Commonly Used"
linkTitle: "Most Commonly Used"
description: "Describes the most commonly used data types."
---

## Data Types

A data type specifies the type and size of variable values.

The most commonly used data types are categorised and listed below:

| Category | Data Type                 | Size                              | Description |
|----------|---------------------------|-----------------------------------|-------------|
| All | Object | Varies | Any data type can be used where an Object data type is required. Once a variable contains an object data type, if it needs to be used as it's original data type it must be cast back to that data type (e.g. `(Int32)ObjectVariableContainingAnInteger`). |
| | Dynamic | Varies | Any data type can be used where a Dynamic data type is required. Dynamic is similar to object, except no cast is needed to use the variable as it's original data type. |
| Collections | IEnumerable&lt;T&gt; | Varies depending on the number of items it contains | Any data type representing a collection of items that can iterated or looped over. T indicates the data type of the items contained in the collection. List&lt;T&gt; is the most common example. |
| | IList&lt;T&gt; | Varies depending on the number of items it contains | Any data type representing a list of items where each item can be individually accessed by it's index in the list. T indicates the data type of the items contained in the list. List&lt;T&gt; is the most common example. |
| | List&lt;T&gt; | Varies depending on the number of items it contains | A list of items. T indicates the data type of the items contained in the list. |
| | IDictionary&lt;K,&nbsp;V&gt; | Varies depending on the number of items it contains | Any data type representing a dictionary containing items which can be accessed by a key. K indicates the data type of the key used to access the items contained in the dictionary, and V indicates the data type of the item's value. |
| | Dictionary&lt;K,&nbsp;V&gt; | Varies depending on the number of items it contains | A dictionary of items. K indicates the data type of the key used to access the items contained in the dictionary, and V indicates the data type of the item's value. |
| | Structure | Varies depending on the number of items it contains | TODO |
| Conditional&nbsp;Logic | Boolean | 1 bit | A logical value of `true` or `false` |
| Databases | DataTable | Varies depending on number of items it contains | TODO |
|Dates&nbsp;&&nbsp;Time | DateTime | 8 bytes | A value representing a date and time between `00:00:00.0000000 UTC, January 1, 0001` and `23:59:59.9999999 UTC, December 31, 9999`, in the Gregorian calendar |
| | TimeSpan | 8 bytes | A value representing a time interval (duration of time or elapsed time) that is measured as a positive or negative number of days, hours, minutes, seconds, and fractions of a second. |
| Numbers | Int16 | 2 bytes | A whole number from `-32768` through `32767` |
| | Int32 | 4 bytes | A whole number from `-2,147,483,648` through `2,147,483,647` |
| | Int64 | 8 bytes | A whole number from `-9,223,372,036,854,775` through `9,223,372,036,854,775,807` |
| | Single | 4 bytes | A fractional, or very large or small number from `-3.402823e38` to `3.402823e38` |
| | Double | 8 bytes | A fractional, or very large or small number from `-1.79769313486232e308` to `1.79769313486232e308` |
| Text | String | Varies depending on the number of characters it contains | A sequence of characters, surrounded by double quotes (e.g. `"This is a string"`) |
| | Char | 2 bytes | A character or letter surrounded by single quotes (e.g. `'a'` or `'!'`) |
| | StringComparison | 4 bytes | TODO |
| | CultureInfo | Varies | TODO |

### All

#### Object

TODO

#### Dynamic

TODO

### Collections

#### IEnumerable&lt;T&gt;

TODO

#### IList&lt;T&gt;

TODO

#### List&lt;T&gt;

TODO

#### IDictionary&lt;K,&nbsp;V&gt;

TODO

#### Dictionary&lt;K,&nbsp;V&gt;

TODO

#### Structure

TODO

### Conditional Logic

#### Boolean

TODO

### Databases

#### DataTable

TODO

### Dates & Times

#### DateTime

TODO

#### TimeSpan

TODO

### Numbers

#### Int16

TODO

#### Int32

TODO

#### Int64

TODO

#### Single

TODO

#### Double

TODO

### Text

#### String

TODO

#### Char

TODO

#### StringComparison

TODO

#### CultureInfo

TODO

##### InvariantCulture

TODO

TODO: variable link, on page links, glossary, concept links etc.