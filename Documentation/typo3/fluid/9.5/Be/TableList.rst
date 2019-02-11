.. include:: ../../../../Includes.txt

============
be.tableList
============


View helper which renders a record list as known from the TYPO3 list module
Note: This feature is experimental!

= Examples =

<code title="Minimal">
<f:be.tableList tableName="fe_users" />
</code>
<output>
List of all "Website user" records stored in the configured storage PID.
Records will be editable, if the current BE user has got edit rights for the table "fe_users".
Only the title column (username) will be shown.
Context menu is active.
</output>

<code title="Full">
<f:be.tableList tableName="fe_users" fieldList="{0: 'name', 1: 'email'}" storagePid="1" levels="2" filter='foo' recordsPerPage="10" sortField="name" sortDescending="true" readOnly="true" enableClickMenu="false" clickTitleMode="info" />
</code>
<output>
List of "Website user" records with a text property of "foo" stored on PID 1 and two levels down.
Clicking on a username will open the TYPO3 info popup for the respective record
</output>

Arguments
=========


tableName (string)
------------------


name of the database table

fieldList (anySimpleType)
-------------------------


Default: array ()

list of fields to be displayed. If empty, only the title column (configured in $TCA[$tableName][&#039;ctrl&#039;][&#039;title&#039;]) is shown

storagePid (anySimpleType)
--------------------------


by default, records are fetched from the storage PID configured in persistence.storagePid. With this argument, the storage PID can be overwritten

levels (anySimpleType)
----------------------


Default: 0

corresponds to the level selector of the TYPO3 list module. By default only records from the current storagePid are fetched

filter (string)
---------------


corresponds to the &quot;Search String&quot; textbox of the TYPO3 list module. If not empty, only records matching the string will be fetched

recordsPerPage (anySimpleType)
------------------------------


Default: 0

amount of records to be displayed at once. Defaults to $TCA[$tableName][&#039;interface&#039;][&#039;maxSingleDBListItems&#039;] or (if that&#039;s not set) to 100

sortField (string)
------------------


table field to sort the results by

sortDescending (anySimpleType)
------------------------------


Default: false

if TRUE records will be sorted in descending order

readOnly (anySimpleType)
------------------------


Default: false

if TRUE, the edit icons won&#039;t be shown. Otherwise edit icons will be shown, if the current BE user has edit rights for the specified table!

enableClickMenu (anySimpleType)
-------------------------------


Default: true

enables context menu

clickTitleMode (string)
-----------------------


one of &quot;edit&quot;, &quot;show&quot; (only pages, tt_content), &quot;info