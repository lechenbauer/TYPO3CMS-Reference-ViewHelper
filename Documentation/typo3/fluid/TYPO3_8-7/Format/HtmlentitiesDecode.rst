.. include:: ../../../../Includes.txt

.. _typo3-fluid-format-htmlentitiesdecode:

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


.. _format.htmlentitiesdecode_value:
value
-----

:aspect:`DataType`
   string

:aspect:`Required`
   true
:aspect:`Description`
   String to format

.. _format.htmlentitiesdecode_keepquotes:
keepQuotes
----------

:aspect:`DataType`
   mixed

:aspect:`Required`
   true
:aspect:`Description`
   If TRUE, single and double quotes won't be replaced (sets ENT_NOQUOTES flag).

.. _format.htmlentitiesdecode_encoding:
encoding
--------

:aspect:`DataType`
   string

:aspect:`Required`
   true
:aspect:`Description`
