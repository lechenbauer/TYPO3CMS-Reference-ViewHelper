.. include:: ../../../../Includes.txt

==============
form.textfield
==============


View Helper which creates a text field (<input type="text">).

= Examples =

<code title="Example">
<f:form.textfield name="myTextBox" value="default value" />
</code>
<output>
<input type="text" name="myTextBox" value="default value" />
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

autofocus (string)
------------------


Specifies that an input should automatically get focus when the page loads

disabled (string)
-----------------


Specifies that the input element should be disabled when the page loads

maxlength (anySimpleType)
-------------------------


The maxlength attribute of the input field (will not be validated)

readonly (string)
-----------------


The readonly attribute of the input field

size (anySimpleType)
--------------------


The size of the input field

placeholder (string)
--------------------


The placeholder of the textfield

pattern (string)
----------------


HTML5 validation pattern

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

required (anySimpleType)
------------------------


Default: false

If the field is required or not

type (string)
-------------


Default: &#039;text&#039;

The field type, e.g. &quot;text&quot;, &quot;email&quot;, &quot;url&quot; etc.