# # Scorecard

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [optional] [readonly]
**remote_id** | **string** | The third-party API ID of the matching object. | [optional]
**application** | **string** | The application being scored. | [optional]
**interview** | **string** | The interview being scored. | [optional]
**interviewer** | **string** | The interviewer doing the scoring. | [optional]
**remote_created_at** | [**\DateTime**](\DateTime.md) | When the third party&#39;s scorecard was created. | [optional]
**submitted_at** | [**\DateTime**](\DateTime.md) | When the scorecard was submitted. | [optional]
**overall_recommendation** | **string** |  | [optional] [readonly]
**remote_data** | [**\MergeATSClient\Model\RemoteData[]**](RemoteData.md) |  | [optional] [readonly]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
