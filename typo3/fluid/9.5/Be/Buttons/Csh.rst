.. include:: ../../../../../Includes.txt

==============
be.buttons.csh
==============


View helper which returns CSH (context sensitive help) button with icon
Note: The CSH button will only work, if the current BE user has the "Context Sensitive Help mode"
set to something else than "Display no help information" in the Users settings
Note: This view helper is experimental!

= Examples =

<code title="Default">
<f:be.buttons.csh />
</code>
<output>
CSH button as known from the TYPO3 backend.
</output>

<code title="Full configuration">
<f:be.buttons.csh table="xMOD_csh_corebe" field="someCshKey" />
</code>
<output>
CSH button as known from the TYPO3 backend with some custom settings.
</output>

<code title="Full configuration with content">
<f:be.buttons.csh table="xMOD_csh_corebe" field="someCshKey">
  some text to link
</f:be.buttons.csh>
</code>
<output>
A link with text "some text to link" to link the help
</output>

Arguments
=========


table (string)
--------------


Table name (&#039;_MOD_&#039;+module name). If not set, the current module name will be used

field (string)
--------------


Field name (CSH locallang main key)

wrap (string)
-------------


Markup to wrap around the CSH, split by &quot;|&quot;