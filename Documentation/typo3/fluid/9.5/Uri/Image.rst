.. include:: ../../../../Includes.txt

=========
uri.image
=========


Resizes a given image (if required) and returns its relative path.

= Examples =

<code title="Default">
<f:uri.image src="EXT:myext/Resources/Public/typo3_logo.png" />
</code>
<output>
typo3conf/ext/myext/Resources/Public/typo3_logo.png
or (in BE mode):
../typo3conf/ext/myext/Resources/Public/typo3_logo.png
</output>

<code title="Image Object">
<f:uri.image image="{imageObject}" />
</code>
<output>
fileadmin/images/image.png
or (in BE mode):
fileadmin/images/image.png
</output>

<code title="Inline notation">
{f:uri.image(src: 'EXT:myext/Resources/Public/typo3_logo.png', minWidth: 30, maxWidth: 40)}
</code>
<output>
typo3temp/assets/images/[b4c0e7ed5c].png
(depending on your TYPO3s encryption key)
</output>

<code title="non existing image">
<f:uri.image src="NonExistingImage.png" />
</code>
<output>
Could not get image resource for "NonExistingImage.png".
</output>

Arguments
=========


src (string)
------------


src

treatIdAsReference (anySimpleType)
----------------------------------


Default: false

given src argument is a sys_file_reference record

image (anySimpleType)
---------------------


image

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


minimum height of the image

maxWidth (anySimpleType)
------------------------


maximum width of the image

maxHeight (anySimpleType)
-------------------------


maximum height of the image

absolute (anySimpleType)
------------------------


Default: false

Force absolute URL