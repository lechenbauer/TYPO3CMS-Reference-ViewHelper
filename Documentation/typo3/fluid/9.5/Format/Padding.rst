.. include:: ../../../../Includes.txt

==============
format.padding
==============


Formats a string using PHPs str_pad function.

= Examples =

<code title="Defaults">
<f:format.padding padLength="10">TYPO3</f:format.padding>
</code>
<output>
TYPO3     (note the trailing whitespace)
<output>

<code title="Specify padding string">
<f:format.padding padLength="10" padString="-=">TYPO3</f:format.padding>
</code>
<output>
TYPO3-=-=-
</output>

<code title="Specify padding type">
<f:format.padding padLength="10" padString="-" padType="both">TYPO3</f:format.padding>
</code>
<output>
--TYPO3---
</output>

Arguments
=========


value (string)
--------------


string to format

padLength (anySimpleType)
-------------------------


Length of the resulting string. If the value of pad_length is negative or less than the length of the input string, no padding takes place.

padString (string)
------------------


Default: &#039; &#039;

The padding string

padType (string)
----------------


Default: &#039;right&#039;

Append the padding at this site (Possible values: right,left,both. Default: right)