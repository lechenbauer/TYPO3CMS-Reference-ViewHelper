.. include:: ../../../../Includes.txt

===========
format.crop
===========


Use this view helper to crop the text between its opening and closing tags.

= Examples =

<code title="Defaults">
<f:format.crop maxCharacters="10">This is some very long text</f:format.crop>
</code>
<output>
This is
</output>

<code title="Custom suffix">
<f:format.crop maxCharacters="17" append="&nbsp;[more]">This is some very long text</f:format.crop>
</code>
<output>
This is some&nbsp;[more]
</output>

<code title="Don't respect word boundaries">
<f:format.crop maxCharacters="10" respectWordBoundaries="false">This is some very long text</f:format.crop>
</code>
<output>
This is so
</output>

<code title="Don't respect HTML tags">
<f:format.crop maxCharacters="28" respectWordBoundaries="false" respectHtml="false">This is some text with <strong>HTML</strong> tags</f:format.crop>
</code>
<output>
This is some text with <stro
</output>

<code title="Inline notation">
{someLongText -> f:format.crop(maxCharacters: 10)}
</code>
<output>
someLongText cropped after 10 characters
(depending on the value of {someLongText})
</output>

Arguments
=========


maxCharacters (anySimpleType)
-----------------------------


Place where to truncate the string

append (string)
---------------


Default: &#039;&amp;hellip;&#039;

What to append, if truncation happened

respectWordBoundaries (anySimpleType)
-------------------------------------


Default: true

If TRUE and division is in the middle of a word, the remains of that word is removed.

respectHtml (anySimpleType)
---------------------------


Default: true

If TRUE the cropped string will respect HTML tags and entities. Technically that means, that cropHTML() is called rather than crop()