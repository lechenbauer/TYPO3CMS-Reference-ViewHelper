.. include:: ../../../../Includes.txt

.. _typo3-fluid-format-currency:

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

Arguments
=========


.. _format.currency_currencysign:
currencySign
------------

:aspect:`DataType`
   string

:aspect:`Required`
   true
:aspect:`Description`
   The currency sign, eg $ or .

.. _format.currency_decimalseparator:
decimalSeparator
----------------

:aspect:`DataType`
   string

:aspect:`Default`
   ','

:aspect:`Required`
   true
:aspect:`Description`
   The separator for the decimal point.

.. _format.currency_thousandsseparator:
thousandsSeparator
------------------

:aspect:`DataType`
   string

:aspect:`Default`
   '.'

:aspect:`Required`
   true
:aspect:`Description`
   The thousands separator.

.. _format.currency_prependcurrency:
prependCurrency
---------------

:aspect:`DataType`
   mixed

:aspect:`Required`
   true
:aspect:`Description`
   Select if the currency sign should be prepended

.. _format.currency_separatecurrency:
separateCurrency
----------------

:aspect:`DataType`
   mixed

:aspect:`Default`
   true

:aspect:`Required`
   true
:aspect:`Description`
   Separate the currency sign from the number by a single space, defaults to true due to backwards compatibility

.. _format.currency_decimals:
decimals
--------

:aspect:`DataType`
   mixed

:aspect:`Default`
   2

:aspect:`Required`
   true
:aspect:`Description`
   Set decimals places.
