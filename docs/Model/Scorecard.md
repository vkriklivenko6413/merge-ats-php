# # Scorecard

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [optional] [readonly]
**remote_id** | **string** | The third-party API ID of the matching object. | [optional]
**application** | **string** |  | [optional]
**interview** | **string** |  | [optional]
**interviewer** | **string** |  | [optional]
**remote_created_at** | [**\DateTime**](\DateTime.md) | When the third party&#39;s scorecard was created. | [optional]
**submitted_at** | [**\DateTime**](\DateTime.md) | When the scorecard was submitted. | [optional]
**overall_recommendation** | [**OverallRecommendationEnum**](OverallRecommendationEnum.md) | The inteviewer&#39;s recommendation. | [optional]
**remote_data** | [**\MergeATSClient\Model\RemoteData[]**](RemoteData.md) |  | [optional] [readonly]
**remote_was_deleted** | **bool** | Indicates whether or not this object has been deleted by third party webhooks. | [optional] [readonly]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
