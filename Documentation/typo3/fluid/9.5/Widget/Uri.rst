.. include:: ../../../../Includes.txt

==========
widget.uri
==========


A view helper for creating URIs to extbase actions within widgets.

= Examples =

<code title="URI to the show-action of the current controller">
<f:widget.uri action="show" />
</code>
<output>
index.php?id=123&tx_myextension_plugin[widgetIdentifier][action]=show&tx_myextension_plugin[widgetIdentifier][controller]=Standard&cHash=xyz
(depending on the current page, widget and your TS configuration)
</output>

Arguments
=========


useCacheHash (anySimpleType)
----------------------------


Default: false

True whether the cache hash should be appended to the URL

addQueryStringMethod (string)
-----------------------------


Method to be used for query string

action (string)
---------------


Target action

arguments (anySimpleType)
-------------------------


Default: array ()

Arguments

section (string)
----------------


The anchor to be added to the URI

format (string)
---------------


The requested format, e.g. &quot;.html

ajax (anySimpleType)
--------------------


Default: false

TRUE if the URI should be to an AJAX widget, FALSE otherwise.