# AsanaApiClient.Model.CustomFieldCompact
Custom Fields store the metadata that is used in order to add user-specified information to tasks in Asana. Be sure to reference the [custom fields](/reference/custom-fields) developer documentation for more information about how custom fields relate to various resources in Asana.  Users in Asana can [lock custom fields](https://asana.com/guide/help/premium/custom-fields#gl-lock-fields), which will make them read-only when accessed by other users. Attempting to edit a locked custom field will return HTTP error code `403 Forbidden`.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Gid** | **string** | Globally unique identifier of the resource, as a string. | [optional] [readonly] 
**ResourceType** | **string** | The base type of this resource. | [optional] [readonly] 
**Name** | **string** | The name of the custom field. | [optional] 
**Type** | **string** | *Deprecated: new integrations should prefer the resource_subtype field.* The type of the custom field. Must be one of the given values.  | [optional] [readonly] 
**EnumOptions** | [**List&lt;EnumOption&gt;**](EnumOption.md) | *Conditional*. Only relevant for custom fields of type &#x60;enum&#x60; or &#x60;multi_enum&#x60;. This array specifies the possible values which an &#x60;enum&#x60; custom field can adopt. To modify the enum options, refer to [working with enum options](/reference/createenumoptionforcustomfield). | [optional] 
**Enabled** | **bool** | *Conditional*. This field applies only to [custom field values](/docs/custom-fields-guide#/accessing-custom-field-values-on-tasks-or-projects) and is not available for [custom field definitions](/docs/custom-fields-guide#/accessing-custom-field-definitions). Determines if the custom field is enabled or not. For more details, see the [Custom Fields documentation](/docs/custom-fields-guide#/enabled-and-disabled-values). | [optional] [readonly] 
**RepresentationType** | **string** | This field tells the type of the custom field. | [optional] [readonly] 
**IdPrefix** | **string** | This field is the unique custom ID string for the custom field. | [optional] 
**InputRestrictions** | **List&lt;string&gt;** | *Conditional*. Only relevant for custom fields of type &#x60;reference&#x60;. This array of strings reflects the allowed types of objects that can be written to a &#x60;reference&#x60; custom field value. | [optional] 
**IsFormulaField** | **bool** | *Conditional*. This flag describes whether a custom field is a formula custom field. | [optional] 
**DateValue** | [**CustomFieldCompactDateValue**](CustomFieldCompactDateValue.md) |  | [optional] 
**EnumValue** | [**CustomFieldCompactEnumValue**](CustomFieldCompactEnumValue.md) |  | [optional] 
**MultiEnumValues** | [**List&lt;EnumOption&gt;**](EnumOption.md) | *Conditional*. Only relevant for custom fields of type &#x60;multi_enum&#x60;. This object is the chosen values of a &#x60;multi_enum&#x60; custom field. | [optional] 
**NumberValue** | **decimal** | *Conditional*. This number is the value of a &#x60;number&#x60; custom field. | [optional] 
**TextValue** | **string** | *Conditional*. This string is the value of a &#x60;text&#x60; custom field. | [optional] 
**DisplayValue** | **string** | A string representation for the value of the custom field. Integrations that don&#39;t require the underlying type should use this field to read values. Using this field will future-proof an app against new custom field types. | [optional] [readonly] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

