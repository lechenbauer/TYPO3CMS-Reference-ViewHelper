.. include:: ../../../Includes.txt

=============
flashMessages
=============


View helper which renders the flash messages (if there are any) as an unsorted list.

In case you need custom Flash Message HTML output, please write your own ViewHelper for the moment.


= Examples =

<code title="Simple">
<f:flashMessages />
</code>
<output>
A list of flash messages.
</output>

<code title="TYPO3 core style">
<f:flashMessages />
</code>
<output>
<div class="typo3-messages">
 <div class="alert alert-info">
     <div class="media">
         <div class="media-left">
             <span class="fa-stack fa-lg">
                 <i class="fa fa-circle fa-stack-2x"></i>
                 <i class="fa fa-info fa-stack-1x"></i>
             </span>
         </div>
         <div class="media-body">
             <h4 class="alert-title">Info - Title for Info message</h4>
             <p class="alert-message">Message text here.</p>
         </div>
     </div>
 </div>
</div>
</output>
<code title="Output flash messages as a description list">
<f:flashMessages as="flashMessages">
	<dl class="messages">
	<f:for each="{flashMessages}" as="flashMessage">
		<dt>{flashMessage.code}</dt>
		<dd>{flashMessage.message}</dd>
	</f:for>
	</dl>
</f:flashMessages>
</code>
<output>
<dl class="messages">
	<dt>1013</dt>
	<dd>Some Warning Message.</dd>
</dl>
</output>

<code title="Using a specific queue">
<f:flashMessages queueIdentifier="myQueue" />
</code>

Arguments
=========


queueIdentifier (string)
------------------------


Flash-message queue to use

as (string)
-----------


The name of the current flashMessage variable for rendering inside