.. include:: ../../../../../Includes.txt

=====================
be.security.ifHasRole
=====================


This view helper implements an ifHasRole/else condition for BE users/groups.

= Examples =

<code title="Basic usage">
<f:be.security.ifHasRole role="Administrator">
This is being shown in case the current BE user belongs to a BE usergroup (aka role) titled "Administrator" (case sensitive)
</f:be.security.ifHasRole>
</code>
<output>
Everything inside the <f:ifHasRole> tag is being displayed if the logged in BE user belongs to the specified role.
</output>

<code title="Using the usergroup uid as role identifier">
<f:be.security.ifHasRole role="1">
This is being shown in case the current BE user belongs to a BE usergroup (aka role) with the uid "1"
</f:be.security.ifHasRole>
</code>
<output>
Everything inside the <f:ifHasRole> tag is being displayed if the logged in BE user belongs to the specified role.
</output>

<code title="IfRole / then / else">
<f:be.security.ifHasRole role="Administrator">
<f:then>
This is being shown in case you have the role.
</f:then>
<f:else>
This is being displayed in case you do not have the role.
</f:else>
</f:be.security.ifHasRole>
</code>
<output>
Everything inside the "then" tag is displayed if the logged in BE user belongs to the specified role.
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

role (string)
-------------


The usergroup (either the usergroup uid or its title).