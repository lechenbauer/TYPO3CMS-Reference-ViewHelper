.. include:: ../../../Includes.txt

.. _typo3-fluid-translate:

=========
translate
=========


Translate a key from locallang. The files are loaded from the folder
"Resources/Private/Language/".

== Examples ==

<code title="Translate key">
<f:translate key="key1" />
</code>
<output>
value of key "key1" in the current website language
</output>

<code title="Keep HTML tags">
<f:format.raw><f:translate key="htmlKey" /></f:format.raw>
</code>
<output>
value of key "htmlKey" in the current website language, no htmlspecialchars applied
</output>

<code title="Translate key from custom locallang file">
<f:translate key="LLL:EXT:myext/Resources/Private/Language/locallang.xlf:key1" />
</code>
<output>
value of key "key1" in the current website language
</output>

<code title="Inline notation with arguments and default value">
{f:translate(key: 'argumentsKey', arguments: {0: 'dog', 1: 'fox'}, default: 'default value')}
</code>
<output>
value of key "argumentsKey" in the current website language
with "%1" and "%2" are replaced by "dog" and "fox" (printf)
if the key is not found, the output is "default value"
</output>

<code title="Inline notation with extension name">
{f:translate(key: 'someKey', extensionName: 'SomeExtensionName')}
</code>
<output>
value of key "someKey" in the current website language
the locallang file of extension "some_extension_name" will be used
</output>

<code title="Translate id as in TYPO3 Flow">
<f:translate id="key1" />
</code>
<output>
value of id "key1" in the current website language
</output>

Arguments
=========


.. _translate_key:
key
---

:aspect:`DataType`
   string

:aspect:`Required`
   true
:aspect:`Description`
   Translation Key

.. _translate_id:
id
--

:aspect:`DataType`
   string

:aspect:`Required`
   true
:aspect:`Description`
   Translation Key compatible to TYPO3 Flow

.. _translate_default:
default
-------

:aspect:`DataType`
   string

:aspect:`Required`
   true
:aspect:`Description`
   If the given locallang key could not be found, this value is used. If this argument is not set, child nodes will be used to render the default

.. _translate_htmlescape:
htmlEscape
----------

:aspect:`DataType`
   mixed

:aspect:`Required`
   true
:aspect:`Description`
   TRUE if the result should be htmlescaped. This won't have an effect for the default value

.. _translate_arguments:
arguments
---------

:aspect:`DataType`
   mixed

:aspect:`Required`
   true
:aspect:`Description`
   Arguments to be replaced in the resulting string

.. _translate_extensionname:
extensionName
-------------

:aspect:`DataType`
   string

:aspect:`Required`
   true
:aspect:`Description`
   UpperCamelCased extension key (for example BlogExample)
