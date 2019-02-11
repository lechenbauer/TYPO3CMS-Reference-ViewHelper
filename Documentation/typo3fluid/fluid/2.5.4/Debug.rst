.. include:: ../../../Includes.txt

=====
debug
=====


<code title="inline notation and custom title">
{object -> f:debug(title: 'Custom title')}
</code>
<output>
all properties of {object} nicely highlighted (with custom title)
</output>

<code title="only output the type">
{object -> f:debug(typeOnly: true)}
</code>
<output>
the type or class name of {object}
</output>

Note: This view helper is only meant to be used during development

Arguments
=========


typeOnly (boolean)
------------------


Default: false

If TRUE, debugs only the type of variables

levels (integer)
----------------


Default: 5

Levels to render when rendering nested objects/arrays

html (boolean)
--------------


Default: false

Render HTML. If FALSE, output is indented plaintext