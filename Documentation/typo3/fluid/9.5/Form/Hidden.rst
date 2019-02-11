.. include:: ../../../../Includes.txt

===========
form.hidden
===========


Renders an <input type="hidden" ...> tag.

= Examples =

<code title="Example">
<f:form.hidden name="myHiddenValue" value="42" />
</code>
<output>
<input type="hidden" name="myHiddenValue" value="42" />
</output>

You can also use the "property" attribute if you have bound an object to the form.
See <f:form> for more documentation.

Arguments
=========


additionalAttributes (anySimpleType)
------------------------------------


Additional tag attributes. They will be added directly to the resulting HTML tag.

data (anySimpleType)
--------------------


Additional data-* attributes. They will each be added with a &quot;data-&quot; prefix.

name (string)
-------------


Name of input tag

value (anySimpleType)
---------------------


Value of input tag

property (string)
-----------------


Name of Object Property. If used in conjunction with &lt;f:form object=&quot;...&quot;&gt;, &quot;name&quot; and &quot;value&quot; properties will be ignored.

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