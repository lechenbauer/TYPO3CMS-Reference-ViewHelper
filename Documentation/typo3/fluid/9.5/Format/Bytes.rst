.. include:: ../../../../Includes.txt

============
format.bytes
============


Formats an integer with a byte count into human-readable form.

= Examples =

<code title="Defaults">
{fileSize -> f:format.bytes()}
</code>
<output>
123 KB
// depending on the value of {fileSize}
</output>

<code title="Defaults">
{fileSize -> f:format.bytes(decimals: 2, decimalSeparator: '.', thousandsSeparator: ',')}
</code>
<output>
1,023.00 B
// depending on the value of {fileSize}
</output>

You may provide an own set of units, like this: B,KB,MB,GB,TB,PB,EB,ZB,YB
<code title="custom units">
{fileSize -> f:format.bytes(units: '{f:translate(\'viewhelper.format.bytes.units\', \'fluid\')}'
</code>
<output>
123 KB
// depending on the value of {fileSize}
</output>

Arguments
=========


value (anySimpleType)
---------------------


The incoming data to convert, or NULL if VH children should be used

decimals (anySimpleType)
------------------------


Default: 0

The number of digits after the decimal point

decimalSeparator (string)
-------------------------


Default: &#039;.&#039;

The decimal point character

thousandsSeparator (string)
---------------------------


Default: &#039;,&#039;

The character for grouping the thousand digits

units (string)
--------------


comma separated list of available units, default is LocalizationUtility::translate(&#039;viewhelper.format.bytes.units&#039;, &#039;fluid&#039;)