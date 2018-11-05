.. include:: ../../../../Includes.txt

=======================
format.htmlspecialchars
=======================


Applies htmlspecialchars() escaping to a value


= Examples =

<code title="default notation">
<f:format.htmlspecialchars>{text}</f:format.htmlspecialchars>
</code>
<output>
Text with & " ' < > * replaced by HTML entities (htmlspecialchars applied).
</output>

<code title="inline notation">
{text -> f:format.htmlspecialchars(encoding: 'ISO-8859-1')}
</code>
<output>
Text with & " ' < > * replaced by HTML entities (htmlspecialchars applied).
</output>

Arguments
=========


value (string)
--------------


Value to format

keepQuotes (boolean)
--------------------


Default: false

If TRUE quotes will not be replaced (ENT_NOQUOTES)

encoding (string)
-----------------


Default: &#039;UTF-8&#039;

Encoding

doubleEncode (boolean)
----------------------


Default: true

If FALSE html entities will not be encoded