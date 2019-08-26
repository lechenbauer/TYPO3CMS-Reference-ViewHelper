.. include:: ../../../../Includes.txt

.. _typo3-fluid-uri-image:

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


.. _uri.image_src:
src
---

:aspect:`DataType`
   string

:aspect:`Required`
   true
:aspect:`Description`
   Src

.. _uri.image_treatidasreference:
treatIdAsReference
------------------

:aspect:`DataType`
   mixed

:aspect:`Required`
   true
:aspect:`Description`
   Given src argument is a sys_file_reference record

.. _uri.image_image:
image
-----

:aspect:`DataType`
   mixed

:aspect:`Required`
   true
:aspect:`Description`
   Image

.. _uri.image_crop:
crop
----

:aspect:`DataType`
   mixed

:aspect:`Required`
   true
:aspect:`Description`
   Overrule cropping of image (setting to FALSE disables the cropping set in FileReference)

.. _uri.image_cropvariant:
cropVariant
-----------

:aspect:`DataType`
   string

:aspect:`Default`
   'default'

:aspect:`Required`
   true
:aspect:`Description`
   Select a cropping variant, in case multiple croppings have been specified or stored in FileReference

.. _uri.image_width:
width
-----

:aspect:`DataType`
   string

:aspect:`Required`
   true
:aspect:`Description`
   Width of the image. This can be a numeric value representing the fixed width of the image in pixels. But you can also perform simple calculations by adding "m" or "c" to the value. See imgResource.width for possible options.

.. _uri.image_height:
height
------

:aspect:`DataType`
   string

:aspect:`Required`
   true
:aspect:`Description`
   Height of the image. This can be a numeric value representing the fixed height of the image in pixels. But you can also perform simple calculations by adding "m" or "c" to the value. See imgResource.width for possible options.

.. _uri.image_minwidth:
minWidth
--------

:aspect:`DataType`
   mixed

:aspect:`Required`
   true
:aspect:`Description`
   Minimum width of the image

.. _uri.image_minheight:
minHeight
---------

:aspect:`DataType`
   mixed

:aspect:`Required`
   true
:aspect:`Description`
   Minimum height of the image

.. _uri.image_maxwidth:
maxWidth
--------

:aspect:`DataType`
   mixed

:aspect:`Required`
   true
:aspect:`Description`
   Maximum width of the image

.. _uri.image_maxheight:
maxHeight
---------

:aspect:`DataType`
   mixed

:aspect:`Required`
   true
:aspect:`Description`
   Maximum height of the image

.. _uri.image_absolute:
absolute
--------

:aspect:`DataType`
   mixed

:aspect:`Required`
   true
:aspect:`Description`
   Force absolute URL
