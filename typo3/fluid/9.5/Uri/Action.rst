.. include:: ../../../../Includes.txt

==========
uri.action
==========


A view helper for creating URIs to extbase actions.

= Examples =

<code title="URI to the show-action of the current controller">
<f:uri.action action="show" />
</code>
<output>
index.php?id=123&tx_myextension_plugin[action]=show&tx_myextension_plugin[controller]=Standard&cHash=xyz
(depending on the current page and your TS configuration)
</output>

Arguments
=========


action (string)
---------------


Target action

arguments (anySimpleType)
-------------------------


Default: array ()

Arguments

controller (string)
-------------------


Target controller. If NULL current controllerName is used

extensionName (string)
----------------------


Target Extension Name (without &quot;tx_&quot; prefix and no underscores). If NULL the current extension name is used

pluginName (string)
-------------------


Target plugin. If empty, the current plugin name is used

pageUid (anySimpleType)
-----------------------


Target page. See TypoLink destination

pageType (anySimpleType)
------------------------


Default: 0

Type of the target page. See typolink.parameter

noCache (anySimpleType)
-----------------------


Default: false

Set this to disable caching for the target page. You should not need this.

noCacheHash (anySimpleType)
---------------------------


Default: false

Set this to suppress the cHash query parameter created by TypoLink. You should not need this.

section (string)
----------------


The anchor to be added to the URI

format (string)
---------------


The requested format, e.g. &quot;.html

linkAccessRestrictedPages (anySimpleType)
-----------------------------------------


Default: false

If set, links pointing to access restricted pages will still link to the page even though the page cannot be accessed.

additionalParams (anySimpleType)
--------------------------------


Default: array ()

additional query parameters that won&#039;t be prefixed like $arguments (overrule $arguments)

absolute (anySimpleType)
------------------------


Default: false

If set, an absolute URI is rendered

addQueryString (anySimpleType)
------------------------------


Default: false

If set, the current query parameters will be kept in the URI

argumentsToBeExcludedFromQueryString (anySimpleType)
----------------------------------------------------


Default: array ()

arguments to be removed from the URI. Only active if $addQueryString = TRUE

addQueryStringMethod (string)
-----------------------------


Set which parameters will be kept. Only active if $addQueryString = TRUE