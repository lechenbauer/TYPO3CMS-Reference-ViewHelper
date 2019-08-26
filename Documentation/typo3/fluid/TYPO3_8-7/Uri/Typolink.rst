.. include:: ../../../../Includes.txt

.. _typo3-fluid-uri-typolink:

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


.. _uri.typolink_parameter:
parameter
---------

:aspect:`DataType`
   string

:aspect:`Required`
   true
:aspect:`Description`
   StdWrap.typolink style parameter string

.. _uri.typolink_additionalparams:
additionalParams
----------------

:aspect:`DataType`
   string

:aspect:`Required`
   true
:aspect:`Description`
   StdWrap.typolink additionalParams

.. _uri.typolink_usecachehash:
useCacheHash
------------

:aspect:`DataType`
   mixed

:aspect:`Required`
   true
:aspect:`Description`


.. _uri.typolink_addquerystring:
addQueryString
--------------

:aspect:`DataType`
   mixed

:aspect:`Required`
   true
:aspect:`Description`


.. _uri.typolink_addquerystringmethod:
addQueryStringMethod
--------------------

:aspect:`DataType`
   string

:aspect:`Default`
   'GET'

:aspect:`Required`
   true
:aspect:`Description`


.. _uri.typolink_addquerystringexclude:
addQueryStringExclude
---------------------

:aspect:`DataType`
   string

:aspect:`Required`
   true
:aspect:`Description`


.. _uri.typolink_absolute:
absolute
--------

:aspect:`DataType`
   mixed

:aspect:`Required`
   true
:aspect:`Description`
   Ensure the resulting URL is an absolute URL
