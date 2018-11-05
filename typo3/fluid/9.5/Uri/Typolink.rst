.. include:: ../../../../Includes.txt

============
uri.typolink
============


A ViewHelper to create uris from fields supported by the link wizard

== Example ==

{link} contains "19 - - - &X=y"
Please note that due to the nature of typolink you have to provide a
full set of parameters if you use the parameter only. Target, class
and title will be discarded.

<code title="minimal usage">
<f:uri.typolink parameter="{link}" />
<output>
index.php?id=19&X=y
</output>
</code>

<code title="Full parameter usage">
<f:uri.typolink parameter="{link}" additionalParams="&u=b" useCacheHash="true" />
</code>
<output>
index.php?id=19&X=y&u=b
</output>

Arguments
=========


parameter (string)
------------------


stdWrap.typolink style parameter string

additionalParams (string)
-------------------------


stdWrap.typolink additionalParams

useCacheHash (anySimpleType)
----------------------------


Default: false



addQueryString (anySimpleType)
------------------------------


Default: false



addQueryStringMethod (string)
-----------------------------


Default: &#039;GET&#039;



addQueryStringExclude (string)
------------------------------




absolute (anySimpleType)
------------------------


Default: false

Ensure the resulting URL is an absolute URL