.. include:: ../../../Includes.txt

====
else
====


Else-Branch of a condition. Only has an effect inside of "If". See the If-ViewHelper for documentation.

= Examples =

<code title="Output content if condition is not met">
<f:if condition="{someCondition}">
  <f:else>
    condition was not true
  </f:else>
</f:if>
</code>
<output>
Everything inside the "else" tag is displayed if the condition evaluates to FALSE.
Otherwise nothing is outputted in this example.
</output>

Arguments
=========


if (boolean)
------------


Condition expression conforming to Fluid boolean rules