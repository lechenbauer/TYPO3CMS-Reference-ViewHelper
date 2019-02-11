.. include:: ../../../../Includes.txt

================
format.stripTags
================


Removes tags from the given string (applying PHPs strip_tags() function)


= Examples =

<code title="default notation">
<f:format.stripTags>Some Text with <b>Tags</b> and an &Uuml;mlaut.</f:format.stripTags>
</code>
<output>
Some Text with Tags and an &Uuml;mlaut. (strip_tags() applied. Note: encoded entities are not decoded)
</output>

<code title="default notation with allowedTags">
<f:format.stripTags allowedTags="<p><span><div><script>"><p>paragraph</p><span>span</span><div>divider</div><iframe>iframe</iframe><script>script</script></f:format.stripTags>
</code>
<output>
<p>paragraph</p><span>span</span><div>divider</div>iframe<script>script</script>
</output>

<code title="inline notation">
{text -> f:format.stripTags()}
</code>
<output>
Text without tags (strip_tags() applied)
</output>

<code title="inline notation with allowedTags">
{text -> f:format.stripTags(allowedTags: "<p><span><div><script>")}
</code>
<output>
Text with p, span, div and script Tags inside, all other tags are removed
</output>

Arguments
=========


value (string)
--------------


string to format

allowedTags (string)
--------------------


Optional string of allowed tags as required by PHPs strip_tags() f
unction