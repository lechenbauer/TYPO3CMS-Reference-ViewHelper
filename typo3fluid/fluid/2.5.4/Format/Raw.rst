.. include:: ../../../../Includes.txt

==========
format.raw
==========


Outputs an argument/value without any escaping. Is normally used to output
an ObjectAccessor which should not be escaped, but output as-is.

PAY SPECIAL ATTENTION TO SECURITY HERE (especially Cross Site Scripting),
as the output is NOT SANITIZED!

= Examples =

<code title="Child nodes">
<f:format.raw>{string}</f:format.raw>
</code>
<output>
(Content of {string} without any conversion/escaping)
</output>

<code title="Value attribute">
<f:format.raw value="{string}" />
</code>
<output>
(Content of {string} without any conversion/escaping)
</output>

<code title="Inline notation">
{string -> f:format.raw()}
</code>
<output>
(Content of {string} without any conversion/escaping)
</output>

Arguments
=========


value (anySimpleType)
---------------------


The value to output