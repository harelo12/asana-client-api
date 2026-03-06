# AsanaApiClient.Model.StatusUpdateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Text** | **string** | The text content of the status update. | 
**StatusType** | **string** | The type associated with the status update. This represents the current state of the object this object is on.  The valid values for &#x60;status_type&#x60; depend on the parent of the status update: - Projects: &#x60;on_track&#x60;, &#x60;at_risk&#x60;, &#x60;off_track&#x60;, &#x60;on_hold&#x60;, &#x60;complete&#x60;, &#x60;dropped&#x60;. - Portfolios: &#x60;on_track&#x60;, &#x60;at_risk&#x60;, &#x60;off_track&#x60;, &#x60;on_hold&#x60;, &#x60;complete&#x60;, &#x60;dropped&#x60;. - Goals: &#x60;on_track&#x60;, &#x60;at_risk&#x60;, &#x60;off_track&#x60;, &#x60;achieved&#x60;, &#x60;partial&#x60;, &#x60;missed&#x60;, &#x60;dropped&#x60;. | 
**Parent** | **string** | The id of parent to send this status update to. This can be a project, goal or portfolio. | 
**Gid** | **string** | Globally unique identifier of the resource, as a string. | [optional] [readonly] 
**ResourceType** | **string** | The base type of this resource. | [optional] [readonly] 
**Title** | **string** | The title of the status update. | [optional] 
**ResourceSubtype** | **string** | The subtype of this resource. Different subtypes retain many of the same fields and behavior, but may render differently in Asana or represent resources with different semantic meaning. The &#x60;resource_subtype&#x60;s for &#x60;status&#x60; objects represent the type of their parent. | [optional] [readonly] 
**HtmlText** | **string** | [Opt In](/docs/inputoutput-options). The text content of the status update with formatting as HTML. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

