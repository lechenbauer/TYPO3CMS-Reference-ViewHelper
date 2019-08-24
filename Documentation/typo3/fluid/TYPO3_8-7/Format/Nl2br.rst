.. include:: ../../../../Includes.txt

.. _typo3-fluid-format-nl2br:

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


.. _format.nl2br_value:
value
-----

:aspect:`DataType`
   string

:aspect:`Required`
   true
:aspect:`Description`
   String to format
