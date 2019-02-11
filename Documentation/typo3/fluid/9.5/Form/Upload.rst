.. include:: ../../../../Includes.txt

===========
form.upload
===========


A view helper which generates an <input type="file"> HTML element.
Make sure to set enctype="multipart/form-data" on the form!

= Examples =

<code title="Example">
<f:form.upload name="file" />
</code>
<output>
<input type="file" name="file" />
</output>

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

disabled (string)
-----------------


Specifies that the input element should be disabled when the page loads

multiple (string)
-----------------


Specifies that the file input element should allow multiple selection of files

errorClass (string)
-------------------


Default: &#039;f3-form-error&#039;

CSS class to set if there are errors for this view helper

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