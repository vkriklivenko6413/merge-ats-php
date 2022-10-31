# # Application

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [optional] [readonly]
**remote_id** | **string** | The third-party API ID of the matching object. | [optional]
**candidate** | **string** |  | [optional]
**job** | **string** |  | [optional]
**applied_at** | [**\DateTime**](\DateTime.md) | When the application was submitted. | [optional]
**rejected_at** | [**\DateTime**](\DateTime.md) | When the application was rejected. | [optional]
**source** | **string** | The application&#39;s source. | [optional]
**credited_to** | **string** |  | [optional]
**current_stage** | **string** |  | [optional]
**reject_reason** | **string** |  | [optional]
**remote_data** | [**\MergeATSClient\Model\RemoteData[]**](RemoteData.md) |  | [optional] [readonly]
**custom_fields** | **array<string,mixed>** | Custom fields configured for a given model. | [optional]
**remote_was_deleted** | **bool** |  | [optional] [readonly]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
