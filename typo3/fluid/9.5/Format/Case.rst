.. include:: ../../../../Includes.txt

===========
format.case
===========


Modifies the case of an input string to upper- or lowercase or capitalization.
The default transformation will be uppercase as in ``mb_convert_case`` [1].

Possible modes are:

``lower``
  Transforms the input string to its lowercase representation

``upper``
  Transforms the input string to its uppercase representation

``capital``
  Transforms the input string to its first letter upper-cased, i.e. capitalization

``uncapital``
  Transforms the input string to its first letter lower-cased, i.e. uncapitalization

``capitalWords``
  Not supported yet: Transforms the input string to each containing word being capitalized

Note that the behavior will be the same as in the appropriate PHP function ``mb_convert_case`` [1];
especially regarding locale and multibyte behavior.


= Examples =

<code title="Example">
<f:format.case>Some Text with miXed case</f:format.case>
</code>
<output>
SOME TEXT WITH MIXED CASE
</output>

<code title="Example with given mode">
<f:format.case mode="capital">someString</f:format.case>
</code>
<output>
SomeString
</output>

Arguments
=========


value (string)
--------------


The input value. If not given, the evaluated child nodes will be used.

mode (string)
-------------


Default: &#039;upper&#039;

The case to apply, must be one of this&#039; CASE_* constants. Defaults to uppercase application.