.. include:: ../../../../Includes.txt

===============
widget.paginate
===============


This ViewHelper renders a Pagination of objects.

= Examples =

<code title="required arguments">
<f:widget.paginate objects="{blogs}" as="paginatedBlogs">
use {paginatedBlogs} as you used {blogs} before, most certainly inside
a <f:for> loop.
</f:widget.paginate>
</code>

<code title="full configuration">
<f:widget.paginate objects="{blogs}" as="paginatedBlogs" configuration="{itemsPerPage: 5, insertAbove: 1, insertBelow: 0, maximumNumberOfLinks: 10}">
use {paginatedBlogs} as you used {blogs} before, most certainly inside
a <f:for> loop.
</f:widget.paginate>
</code>

= Performance characteristics =

In the above examples, it looks like {blogs} contains all Blog objects, thus
you might wonder if all objects were fetched from the database.
However, the blogs are NOT fetched from the database until you actually use them,
so the paginate ViewHelper will adjust the query sent to the database and receive
only the small subset of objects.
So, there is no negative performance overhead in using the Paginate Widget.

Arguments
=========


customWidgetId (string)
-----------------------


extend the widget identifier with a custom widget id

objects (anySimpleType)
-----------------------


Object

as (string)
-----------


as

configuration (anySimpleType)
-----------------------------


Default: array (  &#039;itemsPerPage&#039; =&gt; 10,  &#039;insertAbove&#039; =&gt; false,  &#039;insertBelow&#039; =&gt; true,  &#039;maximumNumberOfLinks&#039; =&gt; 99,)

configuration