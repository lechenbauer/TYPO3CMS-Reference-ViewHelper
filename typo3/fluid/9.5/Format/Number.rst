.. include:: ../../../../Includes.txt

=============
format.number
=============


Formats a number with custom precision, decimal point and grouped thousands.


= Examples =

<code title="Defaults">
<f:format.number>423423.234</f:format.number>
</code>
<output>
423,423.20
</output>

<code title="With all parameters">
<f:format.number decimals="1" decimalSeparator="," thousandsSeparator=".">423423.234</f:format.number>
</code>
<output>
423.423,2
</output>

Arguments
=========


decimals (anySimpleType)
------------------------


Default: &#039;2&#039;

The number of digits after the decimal point

decimalSeparator (string)
-------------------------


Default: &#039;.&#039;

The decimal point character

thousandsSeparator (string)
---------------------------


Default: &#039;,&#039;

The character for grouping the thousand digits