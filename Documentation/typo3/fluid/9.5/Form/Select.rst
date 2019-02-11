.. include:: ../../../../Includes.txt

===========
form.select
===========


This view helper generates a <select> dropdown list for the use with a form.

= Basic usage =

The most straightforward way is to supply an associative array as the "options" parameter.
The array key is used as option key, and the value is used as human-readable name.

<code title="Basic usage">
<f:form.select name="paymentOptions" options="{payPal: 'PayPal International Services', visa: 'VISA Card'}" />
</code>

= Pre-select a value =

To pre-select a value, set "value" to the option key which should be selected.
<code title="Default value">
<f:form.select name="paymentOptions" options="{payPal: 'PayPal International Services', visa: 'VISA Card'}" value="visa" />
</code>
Generates a dropdown box like above, except that "VISA Card" is selected.

If the select box is a multi-select box (multiple="1"), then "value" can be an array as well.

= Custom options and option group rendering =

Child nodes can be used to create a completely custom set of ``<option>`` and ``<optgroup>`` tags in a way compatible with
the HMAC generation. To do so, leave out the ``options`` argument and use child ViewHelpers:
<code title="Custom options and optgroup">
<f:form.select name="myproperty">
    <f:form.select.option value="1">Option one</f:form.select.option>
    <f:form.select.option value="2">Option two</f:form.select.option>
    <f:form.select.optgroup>
        <f:form.select.option value="3">Grouped option one</f:form.select.option>
        <f:form.select.option value="4">Grouped option twi</f:form.select.option>
    </f:form.select.optgroup>
</f:form.select>
</code>
Note: do not use vanilla ``<option>`` or ``<optgroup>`` tags! They will invalidate the HMAC generation!

= Usage on domain objects =

If you want to output domain objects, you can just pass them as array into the "options" parameter.
To define what domain object value should be used as option key, use the "optionValueField" variable. Same goes for optionLabelField.
If neither is given, the Identifier (UID/uid) and the __toString() method are tried as fallbacks.

If the optionValueField variable is set, the getter named after that value is used to retrieve the option key.
If the optionLabelField variable is set, the getter named after that value is used to retrieve the option value.

If the prependOptionLabel variable is set, an option item is added in first position, bearing an empty string or -
If provided, the value of the prependOptionValue variable as value.

<code title="Domain objects">
<f:form.select name="users" options="{userArray}" optionValueField="id" optionLabelField="firstName" />
</code>
In the above example, the userArray is an array of "User" domain objects, with no array key specified.

So, in the above example, the method $user->getId() is called to retrieve the key, and $user->getFirstName() to retrieve the displayed value of each entry.

The "value" property now expects a domain object, and tests for object equivalence.

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

size (string)
-------------


Size of input field

disabled (string)
-----------------


Specifies that the input element should be disabled when the page loads

options (anySimpleType)
-----------------------


Associative array with internal IDs as key, and the values are displayed in the select box. Can be combined with or replaced by child f:form.select.* nodes.

optionsAfterContent (boolean)
-----------------------------


Default: false

If true, places auto-generated option tags after those rendered in the tag content. If false, automatic options come first.

optionValueField (string)
-------------------------


If specified, will call the appropriate getter on each object to determine the value.

optionLabelField (string)
-------------------------


If specified, will call the appropriate getter on each object to determine the label.

sortByOptionLabel (boolean)
---------------------------


Default: false

If true, List will be sorted by label.

selectAllByDefault (boolean)
----------------------------


Default: false

If specified options are selected if none was set before.

errorClass (string)
-------------------


Default: &#039;f3-form-error&#039;

CSS class to set if there are errors for this view helper

prependOptionLabel (string)
---------------------------


If specified, will provide an option at first position with the specified label.

prependOptionValue (string)
---------------------------


If specified, will provide an option at first position with the specified value.

multiple (boolean)
------------------


Default: false

If set multiple options may be selected.

required (boolean)
------------------


Default: false

If set no empty value is allowed.