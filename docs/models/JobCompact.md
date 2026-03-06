# AsanaApiClient.Model.JobCompact
A *job* is an object representing a process that handles asynchronous work.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Gid** | **string** | Globally unique identifier of the resource, as a string. | [optional] [readonly] 
**ResourceType** | **string** | The base type of this resource. | [optional] [readonly] 
**ResourceSubtype** | **string** | The subtype of this resource. Different subtypes retain many of the same fields and behavior, but may render differently in Asana or represent resources with different semantic meaning. | [optional] [readonly] 
**Status** | **string** | The current status of this job. | [optional] [readonly] 
**NewPortfolio** | [**PortfolioCompact**](PortfolioCompact.md) |  | [optional] 
**NewProject** | [**ProjectCompact**](ProjectCompact.md) |  | [optional] 
**NewTask** | [**JobCompactNewTask**](JobCompactNewTask.md) |  | [optional] 
**NewProjectTemplate** | [**ProjectTemplateCompact**](ProjectTemplateCompact.md) |  | [optional] 
**NewGraphExport** | [**GraphExportCompact**](GraphExportCompact.md) |  | [optional] 
**NewResourceExport** | [**ResourceExportCompact**](ResourceExportCompact.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

