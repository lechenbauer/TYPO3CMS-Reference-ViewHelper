.. include:: ../../../Includes.txt

====
form
====


Form view helper. Generates a <form> Tag.

= Basic usage =

Use <f:form> to output an HTML <form> tag which is targeted at the specified action, in the current controller and package.
It will submit the form data via a POST request. If you want to change this, use method="get" as an argument.
<code title="Example">
<f:form action="...">...</f:form>
</code>

= A complex form with a specified encoding type =

<code title="Form with enctype set">
<f:form action=".." controller="..." package="..." enctype="multipart/form-data">...</f:form>
</code>

= A Form which should render a domain object =

<code title="Binding a domain object to a form">
<f:form action="..." name="customer" object="{customer}">
<f:form.hidden property="id" />
<f:form.textbox property="name" />
</f:form>
</code>
This automatically inserts the value of {customer.name} inside the textbox and adjusts the name of the textbox accordingly.

Arguments
=========


additionalAttributes (anySimpleType)
------------------------------------


Additional tag attributes. They will be added directly to the resulting HTML tag.

data (anySimpleType)
--------------------


Additional data-* attributes. They will each be added with a &quot;data-&quot; prefix.

action (string)
---------------


Target action

arguments (anySimpleType)
-------------------------


Default: array ()

Arguments

controller (string)
-------------------


Target controller

extensionName (string)
----------------------


Target Extension Name (without &quot;tx_&quot; prefix and no underscores). If NULL the current extension name is used

pluginName (string)
-------------------


Target plugin. If empty, the current plugin name is used

pageUid (anySimpleType)
-----------------------


Target page uid

object (anySimpleType)
----------------------


Object to use for the form. Use in conjunction with the &quot;property&quot; attribute on the sub tags

pageType (anySimpleType)
------------------------


Default: 0

Target page type

noCache (anySimpleType)
-----------------------


Default: false

set this to disable caching for the target page. You should not need this.

noCacheHash (anySimpleType)
---------------------------


Default: false

set this to suppress the cHash query parameter created by TypoLink. You should not need this.

section (string)
----------------


The anchor to be added to the action URI (only active if $actionUri is not set)

format (string)
---------------


The requested format (e.g. &quot;.html&quot;) of the target page (only active if $actionUri is not set)

additionalParams (anySimpleType)
--------------------------------


Default: array ()

additional action URI query parameters that won&#039;t be prefixed like $arguments (overrule $arguments) (only active if $actionUri is not set)

absolute (anySimpleType)
------------------------


Default: false

If set, an absolute action URI is rendered (only active if $actionUri is not set)

addQueryString (anySimpleType)
------------------------------


Default: false

If set, the current query parameters will be kept in the action URI (only active if $actionUri is not set)

argumentsToBeExcludedFromQueryString (anySimpleType)
----------------------------------------------------


Default: array ()

arguments to be removed from the action URI. Only active if $addQueryString = TRUE and $actionUri is not set

addQueryStringMethod (string)
-----------------------------


Default: &#039;GET&#039;

Method to use when keeping query parameters (GET or POST, only active if $actionUri is not set

fieldNamePrefix (string)
------------------------


Prefix that will be added to all field names within this form. If not set the prefix will be tx_yourExtension_plugin

actionUri (string)
------------------


can be used to overwrite the &quot;action&quot; attribute of the form tag

objectName (string)
-------------------


name of the object that is bound to this form. If this argument is not specified, the name attribute of this form is used to determine the FormObjectName

hiddenFieldClassName (string)
-----------------------------


hiddenFieldClassName

enctype (string)
----------------


MIME type with which the form is submitted

method (string)
---------------


Transfer type (GET or POST)

name (string)
-------------


Name of form

onreset (string)
----------------


JavaScript: On reset of the form

onsubmit (string)
-----------------


JavaScript: On submit of the form

target (string)
---------------


Target attribute of the form

novalidate (anySimpleType)
--------------------------


Indicate that the form is not to be validated on submit.

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