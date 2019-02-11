.. include:: ../../../../Includes.txt

========================
security.ifAuthenticated
========================


This view helper implements an ifAuthenticated/else condition for FE users/groups.

= Examples =

<code title="Basic usage">
<f:security.ifAuthenticated>
This is being shown whenever a FE user is logged in
</f:security.ifAuthenticated>
</code>
<output>
Everything inside the <f:ifAuthenticated> tag is being displayed if you are authenticated with any FE user account.
</output>

<code title="IfAuthenticated / then / else">
<f:security.ifAuthenticated>
<f:then>
This is being shown in case you have access.
</f:then>
<f:else>
This is being displayed in case you do not have access.
</f:else>
</f:security.ifAuthenticated>
</code>
<output>
Everything inside the "then" tag is displayed if you have access.
Otherwise, everything inside the "else"-tag is displayed.
</output>

Arguments
=========


then (anySimpleType)
--------------------


Value to be returned if the condition if met.

else (anySimpleType)
--------------------


Value to be returned if the condition if not met.

condition (boolean)
-------------------


Default: false

Condition expression conforming to Fluid boolean rules