.. include:: ../../../Includes.txt

=====
cycle
=====


This ViewHelper cycles through the specified values.
This can be often used to specify CSS classes for example.
**Note:** To achieve the "zebra class" effect in a loop you can also use the "iteration" argument of the **for** ViewHelper.

= Examples =

<code title="Simple">
<f:for each="{0:1, 1:2, 2:3, 3:4}" as="foo"><f:cycle values="{0: 'foo', 1: 'bar', 2: 'baz'}" as="cycle">{cycle}</f:cycle></f:for>
</code>
<output>
foobarbazfoo
</output>

<code title="Alternating CSS class">
<ul>
  <f:for each="{0:1, 1:2, 2:3, 3:4}" as="foo">
    <f:cycle values="{0: 'odd', 1: 'even'}" as="zebraClass">
      <li class="{zebraClass}">{foo}</li>
    </f:cycle>
  </f:for>
</ul>
</code>
<output>
<ul>
  <li class="odd">1</li>
  <li class="even">2</li>
  <li class="odd">3</li>
  <li class="even">4</li>
</ul>
</output>

Note: The above examples could also be achieved using the "iteration" argument of the ForViewHelper

Arguments
=========


values (anySimpleType)
----------------------


The array or object implementing \ArrayAccess (for example \SplObjectStorage) to iterated over

as (anySimpleType)
------------------


The name of the iteration variable