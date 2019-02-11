.. include:: ../../../../Includes.txt

============
uri.external
============


A view helper for creating URIs to external targets.
Currently the specified URI is simply passed through.

= Examples =

<code>
<f:uri.external uri="http://www.typo3.org" />
</code>
<output>
http://www.typo3.org
</output>

<code title="custom default scheme">
<f:uri.external uri="typo3.org" defaultScheme="ftp" />
</code>
<output>
ftp://typo3.org
</output>

Arguments
=========


uri (string)
------------


target URI

defaultScheme (string)
----------------------


Default: &#039;http&#039;

scheme the href attribute will be prefixed with if specified $uri does not contain a scheme already