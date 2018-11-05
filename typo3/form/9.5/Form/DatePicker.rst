.. include:: ../../../../Includes.txt

===============
form.datePicker
===============


Display a jQuery date picker.

Note: Requires jQuery UI to be included on the page.

Scope: frontend

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

size (anySimpleType)
--------------------


The size of the input field

placeholder (string)
--------------------


Specifies a short hint that describes the expected value of an input element

errorClass (string)
-------------------


Default: &#039;f3-form-error&#039;

CSS class to set if there are errors for this view helper

initialDate (string)
--------------------


Initial date (@see http://www.php.net/manual/en/datetime.formats.php for supported formats)

enableDatePicker (anySimpleType)
--------------------------------


Default: true

Enable the Datepicker

previewMode (anySimpleType)
---------------------------


Default: false

Preview mde flag

dateFormat (string)
-------------------


Default: &#039;Y-m-d&#039;

The date format

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