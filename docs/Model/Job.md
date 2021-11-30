# # Job

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [optional] [readonly]
**remote_id** | **string** | The third-party API ID of the matching object. | [optional]
**name** | **string** | The job&#39;s name. | [optional]
**description** | **string** | The job&#39;s description. | [optional]
**code** | **string** | The job&#39;s code. Typically an additional identifier used to reference the particular job that is displayed on the ATS. | [optional]
**status** | **string** |  | [optional] [readonly]
**remote_created_at** | [**\DateTime**](\DateTime.md) | When the third party&#39;s job was created. | [optional]
**remote_updated_at** | [**\DateTime**](\DateTime.md) | When the third party&#39;s job was updated. | [optional]
**confidential** | **bool** | Whether the job is confidential. | [optional]
**departments** | **string[]** | IDs of &#x60;Department&#x60; objects for this &#x60;Job&#x60;. | [optional]
**offices** | **string[]** | IDs of &#x60;Office&#x60; objects for this &#x60;Job&#x60;. | [optional]
**hiring_managers** | **string[]** | IDs of &#x60;RemoteUser&#x60; objects that serve as hiring managers for this &#x60;Job&#x60;. | [optional]
**remote_data** | [**\MergeATSClient\Model\RemoteData[]**](RemoteData.md) |  | [optional] [readonly]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
