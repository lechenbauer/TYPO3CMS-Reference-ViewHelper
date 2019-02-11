.. include:: ../../../../../Includes.txt

============================
be.menus.actionMenuItemGroup
============================


View helper which groups options of an option tag.

= Example =

	<f:be.menus.actionMenu>
		<f:be.menus.actionMenuItem label="Default: Welcome" controller="Default" action="index" />
		<f:be.menus.actionMenuItem label="Community: get in touch" controller="Community" action="index" />

		<f:be.menus.actionMenuItemGroup label="Information">
			<f:be.menus.actionMenuItem label="PHP Information" controller="Information" action="listPhpInfo" />
			<f:be.menus.actionMenuItem label="Documentation" controller="Information" action="documentation" />
			<f:be.menus.actionMenuItem label="Hooks" controller="Information" action="hooks" />
			<f:be.menus.actionMenuItem label="Signals" controller="Information" action="signals" />
			<f:be.menus.actionMenuItem label="XClasses" controller="Information" action="xclass" />
		</f:be.menus.actionMenuItemGroup>
	</f:be.menus.actionMenu>

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

label (string)
--------------


label