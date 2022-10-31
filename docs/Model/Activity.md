# # Activity

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [optional] [readonly]
**remote_id** | **string** | The third-party API ID of the matching object. | [optional]
**user** | **string** |  | [optional]
**remote_created_at** | [**\DateTime**](\DateTime.md) | When the third party&#39;s activity was created. | [optional]
**activity_type** | [**ActivityTypeEnum**](ActivityTypeEnum.md) | The activity&#39;s type. | [optional]
**subject** | **string** | The activity&#39;s subject. | [optional]
**body** | **string** | The activity&#39;s body. | [optional]
**visibility** | [**VisibilityEnum**](VisibilityEnum.md) | The activity&#39;s visibility. | [optional]
**remote_data** | [**\MergeATSClient\Model\RemoteData[]**](RemoteData.md) |  | [optional] [readonly]
**remote_was_deleted** | **bool** | Indicates whether or not this object has been deleted by third party webhooks. | [optional] [readonly]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
