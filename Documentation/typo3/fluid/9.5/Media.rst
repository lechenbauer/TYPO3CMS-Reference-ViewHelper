.. include:: ../../../Includes.txt

=====
media
=====


Render a given media file with the correct html tag.

It asks the RendererRegister for the correct Renderer class and if not found it falls
back to the ImageViewHelper as that is the "Renderer" class for images in Fluid context.

= Examples =

<code title="Image Object">
    <f:media file="{file}" width="400" height="375" />
</code>
<output>
    <img alt="alt set in image record" src="fileadmin/_processed_/323223424.png" width="396" height="375" />
</output>

<code title="MP4 Video Object">
    <f:media file="{file}" width="400" height="375" />
</code>
<output>
    <video width="400" height="375" controls><source src="fileadmin/user_upload/my-video.mp4" type="video/mp4"></video>
</output>

<code title="MP4 Video Object with loop and autoplay option set">
    <f:media file="{file}" width="400" height="375" additionalConfig="{loop: '1', autoplay: '1'}" />
</code>
<output>
    <video width="400" height="375" controls loop><source src="fileadmin/user_upload/my-video.mp4" type="video/mp4"></video>
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

file (anySimpleType)
--------------------


File

additionalConfig (anySimpleType)
--------------------------------


Default: array ()

This array can hold additional configuration that is passed though to the Renderer object

width (string)
--------------


This can be a numeric value representing the fixed width of in pixels. But you can also perform simple calculations by adding &quot;m&quot; or &quot;c&quot; to the value. See imgResource.width for possible options.

height (string)
---------------


This can be a numeric value representing the fixed height in pixels. But you can also perform simple calculations by adding &quot;m&quot; or &quot;c&quot; to the value. See imgResource.width for possible options.

cropVariant (string)
--------------------


Default: &#039;default&#039;

select a cropping variant, in case multiple croppings have been specified or stored in FileReference