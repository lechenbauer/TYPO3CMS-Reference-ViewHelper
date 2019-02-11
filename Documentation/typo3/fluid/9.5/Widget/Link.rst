.. include:: ../../../../Includes.txt

===========
widget.link
===========


A view helper for creating Links to extbase actions within widets.

= Examples =

<code title="URI to the show-action of the current controller">
<f:widget.link action="show">link</f:widget.link>
</code>
<output>
<a href="index.php?id=123&tx_myextension_plugin[widgetIdentifier][action]=show&tx_myextension_plugin[widgetIdentifier][controller]=Standard&cHash=xyz">link</a>
(depending on the current page, widget and your TS configuration)
</output>

Arguments
=========


additionalAttributes (anySimpleType)
------------------------------------


Additional tag attributes. They will be added directly to the resulting HTML tag.

data (anySimpleType)
--------------------


Additional data-* attributes. They will each be added with a &quot;data-&quot; prefix.

class (string)
--------------


CSS class(es) for this element

dir (string)
------------


Text direction for this HTML element. Allowed strings: &quot;ltr&quot; (left to right), &quot;rtl&quot; (right to left)

id (string)
-----------


Unique (in this file) identifier for this HTML element.

lang (string)
-------------


Language for this element. Use short names specified in RFC 1766

style (string)
--------------


Individual CSS styles for this element

title (string)
--------------


Tooltip text of element

accesskey (string)
------------------


Keyboard shortcut to access this element

tabindex (integer)
------------------


Specifies the tab order of this element

onclick (string)
----------------


JavaScript evaluated for the onclick event

name (string)
-------------


Specifies the name of an anchor

rel (string)
------------


Specifies the relationship between the current document and the linked document

rev (string)
------------


Specifies the relationship between the linked document and the current document

target (string)
---------------


Specifies where to open the linked document

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