.. include:: ../../../../Includes.txt

=====================
form.uploadedResource
=====================


This ViewHelper makes the specified Image object available for its
childNodes.
In case the form is redisplayed because of validation errors, a previously
uploaded image will be correctly used.

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

as (string)
-----------




accept (anySimpleType)
----------------------


Default: array ()

Values for the accept attribute