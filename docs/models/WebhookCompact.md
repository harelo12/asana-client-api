# AsanaApiClient.Model.WebhookCompact
Webhook objects represent the state of an active subscription for a server to be updated with information from Asana. This schema represents the subscription itself, not the objects that are sent to the server. For information on those please refer to the [event](/reference/events) schema.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Gid** | **string** | Globally unique identifier of the resource, as a string. | [optional] [readonly] 
**ResourceType** | **string** | The base type of this resource. | [optional] [readonly] 
**Active** | **bool** | If true, the webhook will send events - if false it is considered inactive and will not generate events. | [optional] [readonly] 
**Resource** | [**AsanaNamedResource**](AsanaNamedResource.md) |  | [optional] 
**Target** | **string** | The URL to receive the HTTP POST. | [optional] [readonly] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

