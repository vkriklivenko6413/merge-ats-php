# # ScheduledInterview

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [optional] [readonly]
**remote_id** | **string** | The third-party API ID of the matching object. | [optional]
**application** | **string** |  | [optional]
**job_interview_stage** | **string** |  | [optional]
**organizer** | **string** |  | [optional]
**interviewers** | **string[]** | Array of &#x60;RemoteUser&#x60; IDs. | [optional]
**location** | **string** | The interview&#39;s location. | [optional]
**start_at** | [**\DateTime**](\DateTime.md) | When the interview was started. | [optional]
**end_at** | [**\DateTime**](\DateTime.md) | When the interview was ended. | [optional]
**remote_created_at** | [**\DateTime**](\DateTime.md) | When the third party&#39;s interview was created. | [optional]
**remote_updated_at** | [**\DateTime**](\DateTime.md) | When the third party&#39;s interview was updated. | [optional]
**status** | [**ScheduledInterviewStatusEnum**](ScheduledInterviewStatusEnum.md) | The interview&#39;s status. | [optional]
**remote_data** | [**\MergeATSClient\Model\RemoteData[]**](RemoteData.md) |  | [optional] [readonly]
**remote_was_deleted** | **bool** | Indicates whether or not this object has been deleted by third party webhooks. | [optional] [readonly]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
