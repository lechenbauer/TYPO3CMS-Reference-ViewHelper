.. include:: ../../../../Includes.txt

======
be.uri
======


A view helper for creating URIs to modules.
= Examples =
<code title="URI to the web_ts module on page 92">
<f:be.uri route="web_ts" parameters="{id: 92}"/>
</code>
<output>
/typo3/index.php?M=web_ts&moduleToken=b6e9c9f?id=92
</output>

 <code title="Inline notation">
{f:be.uri(route: 'web_ts', parameters: '{id: 92}')}
</code>
<output>
/typo3/index.php?route=%2module%2web_ts%2&moduleToken=b6e9c9f?id=92
</output>

Arguments
=========


route (string)
--------------


The name of the route

parameters (anySimpleType)
--------------------------


Default: array ()

An array of parameters

referenceType (string)
----------------------


Default: &#039;absolute&#039;

The type of reference to be generated (one of the constants)