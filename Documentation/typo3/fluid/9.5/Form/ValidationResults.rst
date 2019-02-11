.. include:: ../../../../Includes.txt

======================
form.validationResults
======================


Validation results view helper

= Examples =

<code title="Output error messages as a list">
<f:form.validationResults>
  <f:if condition="{validationResults.flattenedErrors}">
    <ul class="errors">
      <f:for each="{validationResults.flattenedErrors}" as="errors" key="propertyPath">
        <li>{propertyPath}
          <ul>
          <f:for each="{errors}" as="error">
            <li>{error.code}: {error}</li>
          </f:for>
          </ul>
        </li>
      </f:for>
    </ul>
  </f:if>
</f:form.validationResults>
</code>
<output>
<ul class="errors">
  <li>1234567890: Validation errors for argument "newBlog"</li>
</ul>
</output>

<code title="Output error messages for a single property">
<f:form.validationResults for="someProperty">
  <f:if condition="{validationResults.flattenedErrors}">
    <ul class="errors">
      <f:for each="{validationResults.errors}" as="error">
        <li>{error.code}: {error}</li>
      </f:for>
    </ul>
  </f:if>
</f:form.validationResults>
</code>
<output>
<ul class="errors">
  <li>1234567890: Some error message</li>
</ul>
</output>

Arguments
=========


for (string)
------------


The name of the error name (e.g. argument name or property name). This can also be a property path (like blog.title), and will then only display the validation errors of that property.

as (string)
-----------


Default: &#039;validationResults&#039;

The name of the variable to store the current error