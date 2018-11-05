.. include:: ../../../../Includes.txt

==========
form.radio
==========


View Helper which creates a simple radio button (<input type="radio">).

= Examples =

<code title="Example">
<f:form.radio name="myRadioButton" value="someValue" />
</code>
<output>
<input type="radio" name="myRadioButton" value="someValue" />
</output>

<code title="Preselect">
<f:form.radio name="myRadioButton" value="someValue" checked="{object.value} == 5" />
</code>
<output>
<input type="radio" name="myRadioButton" value="someValue" checked="checked" />
(depending on $object)
</output>

<code title="Bind to object property">
<f:form.radio property="newsletter" value="1" /> yes
<f:form.radio property="newsletter" value="0" /> no
</code>
<output>
<input type="radio" name="user[newsletter]" value="1" checked="checked" /> yes
<input type="radio" name="user[newsletter]" value="0" /> no
(depending on property "newsletter")
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

value (string)
--------------


Value of input tag. Required for radio buttons

property (string)
-----------------


Name of Object Property. If used in conjunction with &lt;f:form object=&quot;...&quot;&gt;, &quot;name&quot; and &quot;value&quot; properties will be ignored.

errorClass (string)
-------------------


Default: &#039;f3-form-error&#039;

CSS class to set if there are errors for this view helper

checked (anySimpleType)
-----------------------


Specifies that the input element should be preselected

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

disabled (string)
-----------------


Specifies that the input element should be disabled when the page loads