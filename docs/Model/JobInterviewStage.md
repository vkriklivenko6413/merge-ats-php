# # JobInterviewStage

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [optional] [readonly]
**remote_id** | **string** | The third-party API ID of the matching object. | [optional]
**name** | **string** | The stage&#39;s name. | [optional]
**job** | **string** | This field is populated only if the stage is specific to a particular job. If the stage is generic, this field will not be populated. | [optional]
**remote_data** | [**\MergeATSClient\Model\RemoteData[]**](RemoteData.md) |  | [optional] [readonly]
**remote_was_deleted** | **bool** | Indicates whether or not this object has been deleted by third party webhooks. | [optional] [readonly]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
