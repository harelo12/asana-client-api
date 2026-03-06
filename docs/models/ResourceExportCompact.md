# AsanaApiClient.Model.ResourceExportCompact
A *resource_export* object represents a request to bulk export objects for one or more resources.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Gid** | **string** | Globally unique identifier of the resource, as a string. | [optional] [readonly] 
**ResourceType** | **string** | The base type of this resource. | [optional] [readonly] 
**CreatedAt** | **DateTime** | The time at which the resource export object was created. | [optional] [readonly] 
**DownloadUrl** | **string** | Download this URL to retrieve the full export in [JSON Lines](https://jsonlines.org/) format. It will be compressed in a gzip (.gz) container.  *Note: May be null if the export is still in progress or failed.* | [optional] [readonly] 
**CompletedAt** | **DateTime** | The time at which this resource was completed. This will be null if the export is still in progress. | [optional] [readonly] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

