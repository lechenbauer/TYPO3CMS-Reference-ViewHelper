.. include:: ../../../../Includes.txt

============
uri.resource
============


A view helper for creating URIs to resources.

= Examples =

<code title="Defaults">
<link href="{f:uri.resource(path:'css/stylesheet.css')}" rel="stylesheet" />
</code>
<output>
<link href="Resources/Packages/MyPackage/stylesheet.css" rel="stylesheet" />
(depending on current package)
</output>

Arguments
=========


path (string)
-------------


The path and filename of the resource (relative to Public resource directory of the extension).

extensionName (string)
----------------------


Target extension name. If not set, the current extension name will be used

absolute (anySimpleType)
------------------------


Default: false

If set, an absolute URI is rendered