# AsanaApiClient.Model.ResourceExportRequestParameter

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ResourceType** | **string** | The type of the resource to be exported. This can be a task, team, or message. | [optional] 
**Filters** | [**ResourceExportFilters**](ResourceExportFilters.md) |  | [optional] 
**Fields** | **List&lt;string&gt;** | An array of fields to include for the resource type. If not provided, all non-optional fields for the resource type will be included. This conforms to the fields optional parameter available for all Asana endpoints which is documented [here](https://developers.asana.com/docs/inputoutput-options) | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

