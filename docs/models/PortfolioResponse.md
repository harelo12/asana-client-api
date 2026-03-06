# AsanaApiClient.Model.PortfolioResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Gid** | **string** | Globally unique identifier of the resource, as a string. | [optional] [readonly] 
**ResourceType** | **string** | The base type of this resource. | [optional] [readonly] 
**Name** | **string** | The name of the portfolio. | [optional] 
**Archived** | **bool** | [Opt In](/docs/inputoutput-options). True if the portfolio is archived, false if not. Archived portfolios do not show in the UI by default and may be treated differently for queries. | [optional] 
**Color** | **string** | Color of the portfolio. | [optional] 
**StartOn** | **DateOnly** | The day on which work for this portfolio begins, or null if the portfolio has no start date. This takes a date with &#x60;YYYY-MM-DD&#x60; format. *Note: &#x60;due_on&#x60; must be present in the request when setting or unsetting the &#x60;start_on&#x60; parameter. Additionally, &#x60;start_on&#x60; and &#x60;due_on&#x60; cannot be the same date.* | [optional] 
**DueOn** | **DateOnly** | The day on which this portfolio is due. This takes a date with format YYYY-MM-DD. | [optional] 
**DefaultAccessLevel** | **string** | The default access level when inviting new members to the portfolio | [optional] 
**CreatedAt** | **DateTime** | The time at which this resource was created. | [optional] [readonly] 
**CreatedBy** | [**UserCompact**](UserCompact.md) |  | [optional] 
**CustomFieldSettings** | [**List&lt;CustomFieldSettingResponse&gt;**](CustomFieldSettingResponse.md) | Array of custom field definitions that are enabled for the portfolio. These represent which custom fields are available to be used on items within the portfolio, but do not include any values. | [optional] 
**CurrentStatusUpdate** | [**StatusUpdateCompact**](StatusUpdateCompact.md) | The latest &#x60;status_update&#x60; posted to this portfolio. | [optional] 
**CustomFields** | [**List&lt;CustomFieldCompact&gt;**](CustomFieldCompact.md) | Array of custom field values applied directly to the portfolio itself. These represent the values set on the portfolio, not the fields available for items in the portfolio. | [optional] 
**Members** | [**List&lt;UserCompact&gt;**](UserCompact.md) |  | [optional] [readonly] 
**Owner** | [**UserCompact**](UserCompact.md) |  | [optional] 
**Workspace** | [**PortfolioResponseAllOfWorkspace**](PortfolioResponseAllOfWorkspace.md) |  | [optional] 
**PermalinkUrl** | **string** | A url that points directly to the object within Asana. | [optional] [readonly] 
**Public** | **bool** | True if the portfolio is public to its workspace members. | [optional] 
**PrivacySetting** | **string** | The privacy setting of the portfolio. *Note: Administrators in your organization may restrict the values of &#x60;privacy_setting&#x60;.* | [optional] 
**ProjectTemplates** | [**List&lt;ProjectTemplateCompact&gt;**](ProjectTemplateCompact.md) | Array of project templates that are in the portfolio | [optional] [readonly] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

