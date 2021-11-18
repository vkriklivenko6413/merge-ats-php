# # ApplicationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**remote_id** | **string** | The third-party API ID of the matching object. | [optional]
**candidate** | **string** | The candidate applying. | [optional]
**job** | **string** | The job being applied for. | [optional]
**applied_at** | [**\DateTime**](\DateTime.md) | When the application was submitted. | [optional]
**rejected_at** | [**\DateTime**](\DateTime.md) | When the application was rejected. | [optional]
**source** | **string** | The application&#39;s source. | [optional]
**credited_to** | **string** | The user credited for this application. | [optional]
**current_stage** | **string** | The application&#39;s current stage. | [optional]
**reject_reason** | **string** | The application&#39;s reason for rejection. | [optional]
**custom_fields** | **array<string,mixed>** | Custom fields configured for a given model. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
