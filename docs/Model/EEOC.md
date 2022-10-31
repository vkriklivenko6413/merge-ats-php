# # EEOC

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [optional] [readonly]
**remote_id** | **string** | The third-party API ID of the matching object. | [optional]
**candidate** | **string** |  | [optional]
**submitted_at** | [**\DateTime**](\DateTime.md) | When the information was submitted. | [optional]
**race** | [**RaceEnum**](RaceEnum.md) | The candidate&#39;s race. | [optional]
**gender** | [**GenderEnum**](GenderEnum.md) | The candidate&#39;s gender. | [optional]
**veteran_status** | [**VeteranStatusEnum**](VeteranStatusEnum.md) | The candidate&#39;s veteran status. | [optional]
**disability_status** | [**DisabilityStatusEnum**](DisabilityStatusEnum.md) | The candidate&#39;s disability status. | [optional]
**remote_data** | [**\MergeATSClient\Model\RemoteData[]**](RemoteData.md) |  | [optional] [readonly]
**remote_was_deleted** | **bool** | Indicates whether or not this object has been deleted by third party webhooks. | [optional] [readonly]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
