.. include:: ../../../../../Includes.txt

===================
be.menus.actionMenu
===================


View helper which returns a select box, that can be used to switch between
multiple actions and controllers and looks similar to TYPO3s funcMenu.
Note: This view helper is experimental!

= Examples =

<code title="Simple">
<f:be.menus.actionMenu>
<f:be.menus.actionMenuItem label="Overview" controller="Blog" action="index" />
<f:be.menus.actionMenuItem label="Create new Blog" controller="Blog" action="new" />
<f:be.menus.actionMenuItem label="List Posts" controller="Post" action="index" arguments="{blog: blog}" />
</f:be.menus.actionMenu>
</code>
<output>
Selectbox with the options "Overview", "Create new Blog" and "List Posts"
</output>

<code title="Localized">
<f:be.menus.actionMenu>
<f:be.menus.actionMenuItem label="{f:translate(key:'overview')}" controller="Blog" action="index" />
<f:be.menus.actionMenuItem label="{f:translate(key:'create_blog')}" controller="Blog" action="new" />
</f:be.menus.actionMenu>
</code>
<output>
localized selectbox
<output>

Arguments
=========


additionalAttributes (anySimpleType)
------------------------------------


Additional tag attributes. They will be added directly to the resulting HTML tag.

data (anySimpleType)
--------------------


Additional data-* attributes. They will each be added with a &quot;data-&quot; prefix.

defaultController (string)
--------------------------


defaultController