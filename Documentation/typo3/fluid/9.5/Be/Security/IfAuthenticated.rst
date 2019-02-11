.. include:: ../../../../../Includes.txt

===========================
be.security.ifAuthenticated
===========================


This view helper implements an ifAuthenticated/else condition for BE users/groups.

= Examples =

<code title="Basic usage">
<f:be.security.ifAuthenticated>
This is being shown whenever a BE user is logged in
</f:be.security.ifAuthenticated>
</code>
<output>
Everything inside the <f:be.ifAuthenticated> tag is being displayed if you are authenticated with any BE user account.
</output>

<code title="IfAuthenticated / then / else">
<f:be.security.ifAuthenticated>
<f:then>
This is being shown in case you have access.
</f:then>
<f:else>
This is being displayed in case you do not have access.
</f:else>
</f:be.security.ifAuthenticated>
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