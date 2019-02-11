.. include:: ../../../Includes.txt

======
render
======


Class RenderViewHelper

Arguments
=========


section (string)
----------------


Section to render - combine with partial to render section in partial

partial (string)
----------------


Partial to render, with or without section

delegate (string)
-----------------


Optional PHP class name of a permanent, included-in-app ParsedTemplateInterface implementation to override partial/section

renderable (anySimpleType)
--------------------------


Instance of a RenderableInterface implementation to be rendered

arguments (anySimpleType)
-------------------------


Default: array ()

Array of variables to be transferred. Use {_all} for all variables

optional (boolean)
------------------


Default: false

If TRUE, considers the *section* optional. Partial never is.

default (anySimpleType)
-----------------------


Value (usually string) to be displayed if the section or partial does not exist

contentAs (string)
------------------


If used, renders the child content and adds it as a template variable with this name for use in the partial/section

debug (boolean)
---------------


Default: true

If true, the admin panel shows debug information if activated,