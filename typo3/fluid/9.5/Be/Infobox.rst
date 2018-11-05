.. include:: ../../../../Includes.txt

==========
be.infobox
==========


View helper for rendering a styled content infobox markup.

= States =

The Infobox provides different context sensitive states that
can be used to provide an additional visual feedback to the
to the user to underline the meaning of the information.

Possible values are in range from -2 to 2. Please choose a
meaningful value from the following list.

-2: Notices (Default)
-1: Information
0: Positive feedback
1: Warnings
2: Error

= Examples =

<code title="Simple">
<f:be.infobox title="Message title">your box content</f:be.infobox>
</code>

<code title="All options">
<f:be.infobox title="Message title" message="your box content" state="-2" iconName="check" disableIcon="true" />
</code>

Arguments
=========


message (string)
----------------


The message of the info box, if NULL tag content is used

title (string)
--------------


The title of the info box

state (anySimpleType)
---------------------


Default: -2

The state of the box, InfoboxViewHelper::STATE_*

iconName (string)
-----------------


The icon name from font awesome, NULL sets default icon

disableIcon (anySimpleType)
---------------------------


Default: false

If set to TRUE, the icon is not rendered.