.. include:: ../../../../Includes.txt

=============
link.typolink
=============


A ViewHelper to create links from fields supported by the link wizard

== Example ==

{link} contains "19 _blank - "testtitle with whitespace" &X=y"

<code title="minimal usage">
<f:link.typolink parameter="{link}">
Linktext
</f:link.typolink>
<output>
<a href="index.php?id=19&X=y" title="testtitle with whitespace" target="_blank">
Linktext
</a>
</output>
</code>

<code title="Full parameter usage">
<f:link.typolink parameter="{link}" target="_blank" class="ico-class" title="some title" additionalParams="&u=b" additionalAttributes="{type:'button'}" useCacheHash="true">
Linktext
</f:link.typolink>
</code>
<output>
<a href="index.php?id=19&X=y&u=b" title="some title" target="_blank" class="ico-class" type="button">
Linktext
</a>
</output>

Arguments
=========


parameter (string)
------------------


stdWrap.typolink style parameter string

target (string)
---------------




class (string)
--------------




title (string)
--------------




additionalParams (string)
-------------------------




additionalAttributes (anySimpleType)
------------------------------------


Default: array ()



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