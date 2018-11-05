.. include:: ../../../../Includes.txt

=============
form.textarea
=============


Textarea view helper.
The value of the text area needs to be set via the "value" attribute, as with all other form ViewHelpers.

= Examples =

<code title="Example">
<f:form.textarea name="myTextArea" value="This is shown inside the textarea" />
</code>
<output>
<textarea name="myTextArea">This is shown inside the textarea</textarea>
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


Specifies that a text area should automatically get focus when the page loads

rows (anySimpleType)
--------------------


The number of rows of a text area

cols (anySimpleType)
--------------------


The number of columns of a text area

disabled (string)
-----------------


Specifies that the input element should be disabled when the page loads

placeholder (string)
--------------------


The placeholder of the textarea

errorClass (string)
-------------------


Default: &#039;f3-form-error&#039;

CSS class to set if there are errors for this view helper

readonly (string)
-----------------


The readonly attribute of the textarea

required (anySimpleType)
------------------------


Default: false

Specifies whether the textarea is required

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