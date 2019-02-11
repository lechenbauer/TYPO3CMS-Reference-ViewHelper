.. include:: ../../../Includes.txt

=====
image
=====


Resizes a given image (if required) and renders the respective img tag

= Examples =

<code title="Default">
<f:image src="EXT:myext/Resources/Public/typo3_logo.png" alt="alt text" />
</code>
<output>
<img alt="alt text" src="typo3conf/ext/myext/Resources/Public/typo3_logo.png" width="396" height="375" />
or (in BE mode):
<img alt="alt text" src="../typo3conf/ext/viewhelpertest/Resources/Public/typo3_logo.png" width="396" height="375" />
</output>

<code title="Image Object">
<f:image image="{imageObject}" />
</code>
<output>
<img alt="alt set in image record" src="fileadmin/_processed_/323223424.png" width="396" height="375" />
</output>

<code title="Inline notation">
{f:image(src: 'EXT:viewhelpertest/Resources/Public/typo3_logo.png', alt: 'alt text', minWidth: 30, maxWidth: 40)}
</code>
<output>
<img alt="alt text" src="../typo3temp/assets/images/f13d79a526.png" width="40" height="38" />
(depending on your TYPO3s encryption key)
</output>

<code title="Other resource type (e.g. PDF)">
<f:image src="fileadmin/user_upload/example.pdf" alt="foo" />
</code>
<output>
If your graphics processing library is set up correctly then it will output a thumbnail of the first page of your PDF document.
<img src="fileadmin/_processed_/1/2/csm_example_aabbcc112233.gif" width="200" height="284" alt="foo">
</output>

<code title="Non-existent image">
<f:image src="NonExistingImage.png" alt="foo" />
</code>
<output>
Could not get image resource for "NonExistingImage.png".
</output>

Arguments
=========


additionalAttributes (anySimpleType)
------------------------------------


Additional tag attributes. They will be added directly to the resulting HTML tag.

data (anySimpleType)
--------------------


Additional data-* attributes. They will each be added with a &quot;data-&quot; prefix.

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

alt (string)
------------


Specifies an alternate text for an image

ismap (string)
--------------


Specifies an image as a server-side image-map. Rarely used. Look at usemap instead

longdesc (string)
-----------------


Specifies the URL to a document that contains a long description of an image

usemap (string)
---------------


Specifies an image as a client-side image-map

src (string)
------------


a path to a file, a combined FAL identifier or an uid (int). If $treatIdAsReference is set, the integer is considered the uid of the sys_file_reference record. If you already got a FAL object, consider using the $image parameter instead

treatIdAsReference (anySimpleType)
----------------------------------


given src argument is a sys_file_reference record

image (anySimpleType)
---------------------


a FAL object

crop (anySimpleType)
--------------------


overrule cropping of image (setting to FALSE disables the cropping set in FileReference)

cropVariant (string)
--------------------


Default: &#039;default&#039;

select a cropping variant, in case multiple croppings have been specified or stored in FileReference

width (string)
--------------


width of the image. This can be a numeric value representing the fixed width of the image in pixels. But you can also perform simple calculations by adding &quot;m&quot; or &quot;c&quot; to the value. See imgResource.width for possible options.

height (string)
---------------


height of the image. This can be a numeric value representing the fixed height of the image in pixels. But you can also perform simple calculations by adding &quot;m&quot; or &quot;c&quot; to the value. See imgResource.width for possible options.

minWidth (anySimpleType)
------------------------


minimum width of the image

minHeight (anySimpleType)
-------------------------


minimum width of the image

maxWidth (anySimpleType)
------------------------


minimum width of the image

maxHeight (anySimpleType)
-------------------------


minimum width of the image

absolute (anySimpleType)
------------------------


Default: false

Force absolute URL