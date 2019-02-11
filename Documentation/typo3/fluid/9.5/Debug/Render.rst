.. include:: ../../../../Includes.txt

============
debug.render
============


Debuggable version of f:render - performs the same
rendering operation but wraps the output with HTML
that can be inspected with the admin panel in FE.

Replaces `f:render` when the admin panel decides
(see ViewHelperResolver class). Also possible to use
explicitly by using `f:debug.render` instead of the
normal `f:render` statement.

Arguments
=========


debug (boolean)
---------------


Default: true

If true, the admin panel shows debug information if activated,

section (string)
----------------


Section to render - combine with partial to render section in partial

partial (string)
----------------


Partial to render, with or without section

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