.. include:: ../../../../Includes.txt

===========
format.date
===========


Formats an object implementing \DateTimeInterface.

= Examples =

<code title="Defaults">
<f:format.date>{dateObject}</f:format.date>
</code>
<output>
1980-12-13
(depending on the current date)
</output>

<code title="Custom date format">
<f:format.date format="H:i">{dateObject}</f:format.date>
</code>
<output>
01:23
(depending on the current time)
</output>

<code title="Relative date with given time">
<f:format.date format="Y" base="{dateObject}">-1 year</f:format.date>
</code>
<output>
2016
(assuming dateObject is in 2017)
</output>

<code title="strtotime string">
<f:format.date format="d.m.Y - H:i:s">+1 week 2 days 4 hours 2 seconds</f:format.date>
</code>
<output>
13.12.1980 - 21:03:42
(depending on the current time, see http://www.php.net/manual/en/function.strtotime.php)
</output>

<code title="Localized dates using strftime date format">
<f:format.date format="%d. %B %Y">{dateObject}</f:format.date>
</code>
<output>
13. Dezember 1980
(depending on the current date and defined locale. In the example you see the 1980-12-13 in a german locale)
</output>

<code title="Inline notation">
{f:format.date(date: dateObject)}
</code>
<output>
1980-12-13
(depending on the value of {dateObject})
</output>

<code title="Inline notation (2nd variant)">
{dateObject -> f:format.date()}
</code>
<output>
1980-12-13
(depending on the value of {dateObject})
</output>

Arguments
=========


date (anySimpleType)
--------------------


Either an object implementing DateTimeInterface or a string that is accepted by DateTime constructor

format (string)
---------------


Format String which is taken to format the Date/Time

base (anySimpleType)
--------------------


A base time (an object implementing DateTimeInterface or a string) used if $date is a relative date specification. Defaults to current time.