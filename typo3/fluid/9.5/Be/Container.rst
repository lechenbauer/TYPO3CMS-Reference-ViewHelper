.. include:: ../../../../Includes.txt

============
be.container
============


View helper which allows you to create extbase based modules in the style of TYPO3 default modules.

= Examples =

<code title="Simple">
<f:be.container>your module content</f:be.container>
</code>
<output>
"your module content" wrapped with proper head & body tags.
Default backend CSS styles and JavaScript will be included
</output>

<code title="All options">
<f:be.container pageTitle="foo" includeCssFiles="{0: '{f:uri.resource(path:\'Css/Styles.css\')}'}" includeJsFiles="{0: '{f:uri.resource(path:\'JavaScript/Library1.js\')}', 1: '{f:uri.resource(path:\'JavaScript/Library2.js\')}'}" addJsInlineLabels="{0: 'label1', 1: 'label2'}">your module content</f:be.container>
</code>
<output>
"your module content" wrapped with proper head & body tags.
Custom CSS file EXT:your_extension/Resources/Public/Css/styles.css and
JavaScript files EXT:your_extension/Resources/Public/JavaScript/Library1.js and EXT:your_extension/Resources/Public/JavaScript/Library2.js
will be loaded, plus some inline labels for usage in JS code.
</output>

Arguments
=========


pageTitle (string)
------------------


Title tag of the module. Not required by default, as BE modules are shown in a frame

includeCssFiles (anySimpleType)
-------------------------------


List of custom CSS file to be loaded

includeJsFiles (anySimpleType)
------------------------------


List of custom JavaScript file to be loaded

addJsInlineLabels (anySimpleType)
---------------------------------


Custom labels to add to JavaScript inline labels

includeRequireJsModules (anySimpleType)
---------------------------------------


List of RequireJS modules to be loaded