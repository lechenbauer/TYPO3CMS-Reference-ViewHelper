.. include:: ../../../../Includes.txt

.. _typo3-install-format-crop:

===========
format.crop
===========


Simplified crop view helper that does not need a frontend environment

= Examples =

<code title="Defaults">
<f:format.crop maxCharacters="10">This is some very long text</f:format.crop>
</code>
<output>
This is...
</output>

<code title="Inline notation">
{someLongText -> f:format.crop(maxCharacters: 10)}
</code>
<output>
someLongText cropped after 10 characters...
(depending on the value of {someLongText})
</output>

Arguments
=========


.. _format.crop_maxcharacters:
maxCharacters
-------------

:aspect:`DataType`
   mixed

:aspect:`Required`
   true
:aspect:`Description`
