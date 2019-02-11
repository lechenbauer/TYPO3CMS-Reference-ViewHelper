.. include:: ../../../../Includes.txt

===============
format.currency
===============


Formats a given float to a currency representation.

= Examples =

<code title="Defaults">
<f:format.currency>123.456</f:format.currency>
</code>
<output>
123,46
</output>

<code title="All parameters">
<f:format.currency currencySign="$" decimalSeparator="." thousandsSeparator="," prependCurrency="true" separateCurrency="false" decimals="2">54321</f:format.currency>
</code>
<output>
$54,321.00
</output>

<code title="Inline notation">
{someNumber -> f:format.currency(thousandsSeparator: ',', currencySign: '')}
</code>
<output>
54,321,00 
(depending on the value of {someNumber})
</output>

<code title="use dash for decimals without value">
<f:format.currency useDash="true">123.00</f:format.currency>
</code>
<output>
123,-
</output>

Arguments
=========


currencySign (string)
---------------------


The currency sign, eg $ or .

decimalSeparator (string)
-------------------------


Default: &#039;,&#039;

The separator for the decimal point.

thousandsSeparator (string)
---------------------------


Default: &#039;.&#039;

The thousands separator.

prependCurrency (anySimpleType)
-------------------------------


Default: false

Select if the currency sign should be prepended

separateCurrency (anySimpleType)
--------------------------------


Default: true

Separate the currency sign from the number by a single space, defaults to true due to backwards compatibility

decimals (anySimpleType)
------------------------


Default: 2

Set decimals places.

useDash (anySimpleType)
-----------------------


Default: false

Use the dash instead of decimal 00