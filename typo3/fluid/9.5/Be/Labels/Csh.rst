.. include:: ../../../../../Includes.txt

=============
be.labels.csh
=============


View helper which returns CSH (context sensitive help) label with icon hover
Note: The CSH label will only work, if the current BE user has the "Context Sensitive Help mode"
set to something else than "Display no help information" in the Users settings
Note: This view helper is experimental!

= Examples =

<code title="Default">
<f:be.labels.csh />
</code>
<output>
CSH label as known from the TYPO3 backend.
</output>

<code title="Full configuration">
<f:be.labels.csh table="xMOD_csh_corebe" field="someCshKey" label="lang/Resources/Private/Language/locallang/header.languages" />
</code>
<output>
CSH label as known from the TYPO3 backend with some custom settings.
</output>

Arguments
=========


table (string)
--------------


Table name (&#039;_MOD_&#039;+module name). If not set, the current module name will be used

field (string)
--------------


Field name (CSH locallang main key)

label (string)
--------------


Language label which is wrapped with the CSH