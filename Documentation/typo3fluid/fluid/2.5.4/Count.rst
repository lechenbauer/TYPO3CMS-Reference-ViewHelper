.. include:: ../../../Includes.txt

=====
count
=====


This ViewHelper counts elements of the specified array or countable object.

= Examples =

<code title="Count array elements">
<f:count subject="{0:1, 1:2, 2:3, 3:4}" />
</code>
<output>
4
</output>

<code title="inline notation">
{objects -> f:count()}
</code>
<output>
10 (depending on the number of items in {objects})
</output>

Arguments
=========


subject (anySimpleType)
-----------------------


Countable subject, array or \Countable