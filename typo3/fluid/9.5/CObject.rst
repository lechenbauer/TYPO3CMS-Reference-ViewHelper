.. include:: ../../../Includes.txt

=======
cObject
=======


This ViewHelper renders CObjects from the global TypoScript configuration.
NOTE: You have to ensure proper escaping (htmlspecialchars/intval/etc.) on your own!

= Examples =

<code title="Render lib object">
<f:cObject typoscriptObjectPath="lib.someLibObject" />
</code>
<output>
rendered lib.someLibObject
</output>

<code title="Specify cObject data & current value">
<f:cObject typoscriptObjectPath="lib.customHeader" data="{article}" currentValueKey="title" />
</code>
<output>
rendered lib.customHeader. data and current value will be available in TypoScript
</output>

<code title="inline notation">
{article -> f:cObject(typoscriptObjectPath: 'lib.customHeader')}
</code>
<output>
rendered lib.customHeader. data will be available in TypoScript
</output>

Arguments
=========


data (anySimpleType)
--------------------


the data to be used for rendering the cObject. Can be an object, array or string. If this argument is not set, child nodes will be used

typoscriptObjectPath (string)
-----------------------------


the TypoScript setup path of the TypoScript object to render

currentValueKey (string)
------------------------


currentValueKey

table (string)
--------------


the table name associated with &quot;data&quot; argument. Typically tt_content or one of your custom tables. This argument should be set if rendering a FILES cObject where file references are used, or if the data argument is a database record.