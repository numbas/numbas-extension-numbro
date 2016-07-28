# Numbro extension for Numbas

[numbro.js](http://numbrojs.com/) provides functions to format numbers and currency amounts.

It uses its own format specification language, which is defined by example. See [the numbro.js docs](http://numbrojs.com/format.html) for examples of what's possible.

At the moment, numbro keeps the language setting in a global variable, which makes it difficult to provide formatting functions which take a language/culture parameter without affecting other calls to numbro.

To set the language/culture for a question, call `numbro.culture` in the question preamble, e.g. `numbro.culture('nb-NO')`.

## JME functions

### `format(n,format)`

Format the number `n` following the given format.

**Example**: `format(1234.5,'0,0.00')` → `"1,234.50"`

### `formatcurrency(n,format)`

Format `n` as a currency amount, following the given format.

**Example**: `formatcurrency(12345,'0a')` → `$12k` (when the language is the default value, `en-US`)

### `formatcurrency(n,format,currencySymbol)`

Format `n` as a currency amount, following the given format and with the given currency symbol.

**Example**: `formatcurrency(12345,'0a','£')`  → `£12k`

# Licence

numbro.js is © 2014 Adam Draper, © 2015 Företagsplatsen AB, and released under the MIT licence.

This extension is © 2016 Newcastle University.
