# AsanaApiClient.Model.ProjectTemplateInstantiateProjectRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** | The name of the new project. | 
**Team** | **string** | *Optional*. Sets the team of the new project. If the project template exists in an _organization_, you may specify a value for &#x60;team&#x60;. If no value is provided then it defaults to the same team as the project template. | [optional] 
**Public** | **bool** | *Deprecated:* new integrations use &#x60;privacy_setting&#x60; instead. | [optional] 
**PrivacySetting** | **string** | The privacy setting of the project. *Note: Administrators in your organization may restrict the values of &#x60;privacy_setting&#x60;.* The value &#x60;private_to_team&#x60; is deprecated. Use &#x60;POST /memberships&#x60; to share a project with a team after creation. | [optional] 
**IsStrict** | **bool** | *Optional*. If set to &#x60;true&#x60;, the endpoint returns an \&quot;Unprocessable Entity\&quot; error if you fail to provide a calendar date value for any date variable. If set to &#x60;false&#x60;, a default date is used for each unfulfilled date variable (e.g., the current date is used as the Start Date of a project). | [optional] 
**RequestedDates** | [**List&lt;DateVariableRequest&gt;**](DateVariableRequest.md) | *Conditional*. Array of mappings of date variables to calendar dates. This property is required in the instantiation request if the project template includes dates (e.g., a start date on a task). | [optional] 
**RequestedRoles** | [**List&lt;RequestedRoleRequest&gt;**](RequestedRoleRequest.md) | Array of mappings of template roles to user ids | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

