.. include:: ../../../../Includes.txt

.. _typo3-extensionmanager-be-trigger:

==========
be.trigger
==========


Special view helper for the BE module of the Extension Manager. Loads JS code for triggering
refresh events.

= Examples =

<code title="Simple">
<em:be.container triggers="{triggers}" />
</code>
<output>
Writes some JS inline code
</output>

Arguments
=========


.. _be.trigger_triggers:
triggers
--------

:aspect:`DataType`
   mixed

:aspect:`Default`
   array ()

:aspect:`Required`
   true
:aspect:`Description`
   Defined triggers to be forwarded to client (e.g. refreshing backend widgets)
