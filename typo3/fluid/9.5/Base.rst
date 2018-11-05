.. include:: ../../../Includes.txt

====
base
====


View helper which creates a <base href="..."></base> tag. The Base URI is taken from the
current request.
In TYPO3 Flow, you should always include this ViewHelper to make the links work.

= Examples =

<code title="Example">
<f:base />
</code>
<output>
<base href="http://yourdomain.tld/" />
(depending on your domain)
</output>

Arguments
=========


This ViewHelper has no arguments.