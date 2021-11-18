# # ScheduledInterview

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [optional] [readonly]
**remote_id** | **string** | The third-party API ID of the matching object. | [optional]
**application** | **string** | The application being interviewed. | [optional]
**job_interview_stage** | **string** | The stage of the interview. | [optional]
**organizer** | **string** | The user organizing the interview. | [optional]
**interviewers** | **string[]** | Array of &#x60;RemoteUser&#x60; IDs. | [optional]
**location** | **string** | The interview&#39;s location. | [optional]
**start_at** | [**\DateTime**](\DateTime.md) | When the interview was started. | [optional]
**end_at** | [**\DateTime**](\DateTime.md) | When the interview was ended. | [optional]
**remote_created_at** | [**\DateTime**](\DateTime.md) | When the third party&#39;s interview was created. | [optional]
**remote_updated_at** | [**\DateTime**](\DateTime.md) | When the third party&#39;s interview was updated. | [optional]
**status** | **string** |  | [optional] [readonly]
**remote_data** | [**\MergeHRISClient\Model\RemoteData[]**](RemoteData.md) |  | [optional] [readonly]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
