.. include:: ../../../../Includes.txt

=======
be.link
=======


A view helper for creating URIs to modules.
= Examples =
<code title="URI to the web_ts module on page 92">
<f:be.link route="web_ts" parameters="{id: 92}">Go to web_ts</f:be.link>
</code>
<output>
<a href="/typo3/index.php?route=%2module%2web_ts%2&moduleToken=b6e9c9f?id=92">Go to web_ts</a>
</output>

Arguments
=========


additionalAttributes (anySimpleType)
------------------------------------


Additional tag attributes. They will be added directly to the resulting HTML tag.

data (anySimpleType)
--------------------


Additional data-* attributes. They will each be added with a &quot;data-&quot; prefix.

route (string)
--------------


The name of the route

parameters (anySimpleType)
--------------------------


Default: array ()

An array of parameters

referenceType (string)
----------------------


Default: &#039;absolute&#039;

The type of reference to be generated (one of the constants)

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