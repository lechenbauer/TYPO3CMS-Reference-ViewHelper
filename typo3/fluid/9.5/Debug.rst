.. include:: ../../../Includes.txt

=====
debug
=====


This ViewHelper generates a HTML dump of the tagged variable.

= Examples =

<code title="Simple">
<f:debug>{testVariables.array}</f:debug>
</code>
<output>
foobarbazfoo
</output>

<code title="All Features">
<f:debug title="My Title" maxDepth="5" blacklistedClassNames="{0:'Tx_BlogExample_Domain_Model_Administrator'}" plainText="true" ansiColors="false" inline="true" blacklistedPropertyNames="{0:'posts'}">{blogs}</f:debug>
</code>
<output>
[A HTML view of the var_dump]
</output>

Arguments
=========


title (string)
--------------


optional custom title for the debug output

maxDepth (anySimpleType)
------------------------


Default: 8

Sets the max recursion depth of the dump (defaults to 8). De- or increase the number according to your needs and memory limit.

plainText (anySimpleType)
-------------------------


Default: false

If TRUE, the dump is in plain text, if FALSE the debug output is in HTML format.

ansiColors (anySimpleType)
--------------------------


Default: false

If TRUE, ANSI color codes is added to the plaintext output, if FALSE (default) the plaintext debug output not colored.

inline (anySimpleType)
----------------------


Default: false

if TRUE, the dump is rendered at the position of the &lt;f:debug&gt; tag. If FALSE (default), the dump is displayed at the top of the page.

blacklistedClassNames (anySimpleType)
-------------------------------------


An array of class names (RegEx) to be filtered. Default is an array of some common class names.

blacklistedPropertyNames (anySimpleType)
----------------------------------------


An array of property names and/or array keys (RegEx) to be filtered. Default is an array of some common property names.