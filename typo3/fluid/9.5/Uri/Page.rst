.. include:: ../../../../Includes.txt

========
uri.page
========


A view helper for creating URIs to TYPO3 pages.

= Examples =

<code title="URI to the current page">
<f:uri.page>page link</f:uri.page>
</code>
<output>
index.php?id=123
(depending on the current page and your TS configuration)
</output>

<code title="query parameters">
<f:uri.page pageUid="1" additionalParams="{foo: 'bar'}" />
</code>
<output>
index.php?id=1&foo=bar
(depending on your TS configuration)
</output>

<code title="query parameters for extensions">
<f:uri.page pageUid="1" additionalParams="{extension_key: {foo: 'bar'}}" />
</code>
<output>
index.php?id=1&extension_key[foo]=bar
(depending on your TS configuration)
</output>

Arguments
=========


pageUid (anySimpleType)
-----------------------


target PID

additionalParams (anySimpleType)
--------------------------------


Default: array ()

query parameters to be attached to the resulting URI

pageType (anySimpleType)
------------------------


Default: 0

type of the target page. See typolink.parameter

noCache (anySimpleType)
-----------------------


Default: false

set this to disable caching for the target page. You should not need this.

noCacheHash (anySimpleType)
---------------------------


Default: false

set this to suppress the cHash query parameter created by TypoLink. You should not need this.

section (string)
----------------


the anchor to be added to the URI

linkAccessRestrictedPages (anySimpleType)
-----------------------------------------


Default: false

If set, links pointing to access restricted pages will still link to the page even though the page cannot be accessed.

absolute (anySimpleType)
------------------------


Default: false

If set, the URI of the rendered link is absolute

addQueryString (anySimpleType)
------------------------------


Default: false

If set, the current query parameters will be kept in the URI

argumentsToBeExcludedFromQueryString (anySimpleType)
----------------------------------------------------


Default: array ()

arguments to be removed from the URI. Only active if $addQueryString = TRUE

addQueryStringMethod (string)
-----------------------------


Set which parameters will be kept. Only active if $addQueryString = TRUE