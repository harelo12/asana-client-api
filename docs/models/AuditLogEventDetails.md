# AsanaApiClient.Model.AuditLogEventDetails
Event specific details. The schema will vary depending on the `event_type`.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**OldValue** | **string** | The previous value of the field that was modified in the audited event. | [optional] 
**NewValue** | **string** | The new value after the modification in the audited event. | [optional] 
**Group** | **Dictionary&lt;string, Object&gt;** | The division or organizational unit where the event occurred. Primarily used to scope role change events (e.g., &#x60;user_division_admin_role_changed&#x60;), but may appear in other contexts involving group-level changes. | [optional] 
**SamlResponse** | **string** | The response received from the IdP when a user logs in with SAML SSO. Present on &#x60;user_login_failed&#x60; and &#x60;user_login_succeeded&#x60; events. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

