.. include:: ../../../../Includes.txt

===================
format.htmlentities
===================


Applies htmlentities() escaping to a value

= Examples =

<code title="default notation">
<f:format.htmlentities>{text}</f:format.htmlentities>
</code>
<output>
Text with & " ' < > * replaced by HTML entities (htmlentities applied).
</output>

<code title="inline notation">
{text -> f:format.htmlentities(encoding: 'ISO-8859-1')}
</code>
<output>
Text with & " ' < > * replaced by HTML entities (htmlentities applied).
</output>

Arguments
=========


value (string)
--------------


string to format

keepQuotes (anySimpleType)
--------------------------


Default: false

If TRUE, single and double quotes won&#039;t be replaced (sets ENT_NOQUOTES flag).

encoding (string)
-----------------




doubleEncode (anySimpleType)
----------------------------


Default: true

If FALSE existing html entities won&#039;t be encoded, the default is to convert everything.