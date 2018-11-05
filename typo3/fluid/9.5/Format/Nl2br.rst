.. include:: ../../../../Includes.txt

============
format.nl2br
============


Wrapper for PHPs nl2br function.

= Examples =

<code title="Example">
<f:format.nl2br>{text_with_linebreaks}</f:format.nl2br>
</code>
<output>
text with line breaks replaced by <br />
</output>

<code title="Inline notation">
{text_with_linebreaks -> f:format.nl2br()}
</code>
<output>
text with line breaks replaced by <br />
</output>

Arguments
=========


value (string)
--------------


string to format