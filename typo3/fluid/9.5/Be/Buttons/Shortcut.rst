.. include:: ../../../../../Includes.txt

===================
be.buttons.shortcut
===================


View helper which returns shortcut button with icon
Note: This view helper is experimental!

= Examples =

<code title="Default">
<f:be.buttons.shortcut />
</code>
<output>
Shortcut button as known from the TYPO3 backend.
By default the current page id, module name and all module arguments will be stored
</output>

<code title="Explicitly set parameters to be stored in the shortcut">
<f:be.buttons.shortcut getVars="{0: 'route', 1: 'myOwnPrefix'}" setVars="{0: 'function'}" />
</code>
<output>
Shortcut button as known from the TYPO3 backend.
This time only the specified GET parameters and SET[]-settings will be stored.
Note:
Normally you won't need to set getVars & setVars parameters in Extbase modules
</output>

Arguments
=========


getVars (anySimpleType)
-----------------------


Default: array ()

List of GET variables to store. By default the current id, module and all module arguments will be stored

setVars (anySimpleType)
-----------------------


Default: array ()

List of SET[] variables to store. See DocumentTemplate::makeShortcutIcon(). Normally won&#039;t be used by Extbase modules