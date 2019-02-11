.. include:: ../../../../Includes.txt

=============
link.external
=============


A view helper for creating links to external targets.

= Examples =

<code>
<f:link.external uri="http://www.typo3.org" target="_blank">external link</f:link.external>
</code>
<output>
<a href="http://www.typo3.org" target="_blank">external link</a>
</output>

<code title="custom default scheme">
<f:link.external uri="typo3.org" defaultScheme="ftp">external ftp link</f:link.external>
</code>
<output>
<a href="ftp://typo3.org">external ftp link</a>
</output>

Arguments
=========


additionalAttributes (anySimpleType)
------------------------------------


Additional tag attributes. They will be added directly to the resulting HTML tag.

data (anySimpleType)
--------------------


Additional data-* attributes. They will each be added with a &quot;data-&quot; prefix.

uri (string)
------------


The URI that will be put in the href attribute of the rendered link tag

defaultScheme (string)
----------------------


Default: &#039;http&#039;

Scheme the href attribute will be prefixed with if specified $uri does not contain a scheme already

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