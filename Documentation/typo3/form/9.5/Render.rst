.. include:: ../../../Includes.txt

======
render
======


Main Entry Point to render a Form into a Fluid Template

Usage
=====

<pre>
{namespace formvh=TYPO3\CMS\Form\ViewHelpers}
<formvh:render factoryClass="NameOfYourCustomFactoryClass" />
</pre>


Scope: frontend

Arguments
=========


persistenceIdentifier (string)
------------------------------


The persistence identifier for the form.

factoryClass (string)
---------------------


Default: &#039;TYPO3\\CMS\\Form\\Domain\\Factory\\ArrayFormFactory&#039;

The fully qualified class name of the factory

prototypeName (string)
----------------------


Name of the prototype to use

overrideConfiguration (anySimpleType)
-------------------------------------


Default: array ()

factory specific configuration