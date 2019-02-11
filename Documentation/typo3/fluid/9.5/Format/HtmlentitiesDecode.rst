.. include:: ../../../../Includes.txt

=========================
format.htmlentitiesDecode
=========================


Applies html_entity_decode() to a value

= Examples =

<code title="default notation">
<f:format.htmlentitiesDecode>{text}</f:format.htmlentitiesDecode>
</code>
<output>
Text with &amp; &quot; &lt; &gt; replaced by unescaped entities (html_entity_decode applied).
</output>

<code title="inline notation">
{text -> f:format.htmlentitiesDecode(encoding: 'ISO-8859-1')}
</code>
<output>
Text with &amp; &quot; &lt; &gt; replaced by unescaped entities (html_entity_decode applied).
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