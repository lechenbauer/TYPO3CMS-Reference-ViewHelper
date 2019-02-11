.. include:: ../../../../Includes.txt

===========
form.button
===========


Creates a button.

= Examples =

<code title="Defaults">
<f:form.button>Send Mail</f:form.button>
</code>
<output>
<button type="submit" name="" value="">Send Mail</button>
</output>

<code title="Disabled cancel button with some HTML5 attributes">
<f:form.button type="reset" name="buttonName" value="buttonValue" disabled="disabled" formmethod="post" formnovalidate="formnovalidate">Cancel</f:form.button>
</code>
<output>
<button disabled="disabled" formmethod="post" formnovalidate="formnovalidate" type="reset" name="myForm[buttonName]" value="buttonValue">Cancel</button>
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


Specifies that a button should automatically get focus when the page loads

disabled (string)
-----------------


Specifies that the input element should be disabled when the page loads

form (string)
-------------


Specifies one or more forms the button belongs to

formaction (string)
-------------------


Specifies where to send the form-data when a form is submitted. Only for type=&quot;submit&quot;

formenctype (string)
--------------------


Specifies how form-data should be encoded before sending it to a server. Only for type=&quot;submit&quot; (e.g. &quot;application/x-www-form-urlencoded&quot;, &quot;multipart/form-data&quot; or &quot;text/plain&quot;)

formmethod (string)
-------------------


Specifies how to send the form-data (which HTTP method to use). Only for type=&quot;submit&quot; (e.g. &quot;get&quot; or &quot;post&quot;)

formnovalidate (string)
-----------------------


Specifies that the form-data should not be validated on submission. Only for type=&quot;submit&quot;

formtarget (string)
-------------------


Specifies where to display the response after submitting the form. Only for type=&quot;submit&quot; (e.g. &quot;_blank&quot;, &quot;_self&quot;, &quot;_parent&quot;, &quot;_top&quot;, &quot;framename&quot;)

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

type (string)
-------------


Default: &#039;submit&#039;

Specifies the type of button (e.g. &quot;button&quot;, &quot;reset&quot; or &quot;submit&quot;)