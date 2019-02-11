.. include:: ../../../../Includes.txt

===========
format.json
===========


Wrapper for PHPs json_encode function.

= Examples =

<code title="encoding a view variable">
{someArray -> f:format.json()}
</code>
<output>
["array","values"]
// depending on the value of {someArray}
</output>

<code title="associative array">
{f:format.json(value: {foo: 'bar', bar: 'baz'})}
</code>
<output>
{"foo":"bar","bar":"baz"}
</output>

<code title="non-associative array with forced object">
{f:format.json(value: {0: 'bar', 1: 'baz'}, forceObject: true)}
</code>
<output>
{"0":"bar","1":"baz"}
</output>

Arguments
=========


value (anySimpleType)
---------------------


The incoming data to convert, or null if VH children should be used

forceObject (anySimpleType)
---------------------------


Default: false

Outputs an JSON object rather than an array