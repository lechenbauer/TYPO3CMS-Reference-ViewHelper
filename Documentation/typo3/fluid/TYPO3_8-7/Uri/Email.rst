.. include:: ../../../../Includes.txt

.. _typo3-fluid-uri-email:

=========
uri.email
=========


Email URI view helper.
Generates an email URI incorporating TYPO3s spamProtectEmailAddresses-settings.

= Examples

<code title="basic email URI">
</code>
<output>
javascript:linkTo_UnCryptMailto('ocknvq,hqqBdct0vnf');
(depending on your spamProtectEmailAddresses-settings)
</output>

Arguments
=========


.. _uri.email_email:
email
-----

:aspect:`DataType`
   string

:aspect:`Required`
   true
:aspect:`Description`
   The email address to be turned into a URI
