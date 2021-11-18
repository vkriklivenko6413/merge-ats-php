# # Activity

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [optional] [readonly]
**remote_id** | **string** | The third-party API ID of the matching object. | [optional]
**user** | **string** | The user the performed the action. | [optional]
**remote_created_at** | [**\DateTime**](\DateTime.md) | When the third party&#39;s activity was created. | [optional]
**activity_type** | **string** |  | [optional] [readonly]
**subject** | **string** | The activity&#39;s subject. | [optional]
**body** | **string** | The activity&#39;s body. | [optional]
**visibility** | **string** |  | [optional] [readonly]
**remote_data** | [**\MergeHRISClient\Model\RemoteData[]**](RemoteData.md) |  | [optional] [readonly]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
