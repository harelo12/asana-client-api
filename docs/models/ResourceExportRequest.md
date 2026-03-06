# AsanaApiClient.Model.ResourceExportRequest
A *resource_export* request starts a job to bulk export objects for one or more resources.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Workspace** | **string** | Gid of a workspace. | [optional] 
**ExportRequestParameters** | [**List&lt;ResourceExportRequestParameter&gt;**](ResourceExportRequestParameter.md) | An object containing the parameters for the export request. The keys of this object are the GIDs of the resources to be exported. The values are objects with additional parameters for each resource. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

