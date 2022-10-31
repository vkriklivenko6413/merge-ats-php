# # Offer

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [optional] [readonly]
**remote_id** | **string** | The third-party API ID of the matching object. | [optional]
**application** | **string** |  | [optional]
**creator** | **string** |  | [optional]
**remote_created_at** | [**\DateTime**](\DateTime.md) | When the third party&#39;s offer was created. | [optional]
**closed_at** | [**\DateTime**](\DateTime.md) | When the offer was closed. | [optional]
**sent_at** | [**\DateTime**](\DateTime.md) | When the offer was sent. | [optional]
**start_date** | [**\DateTime**](\DateTime.md) | The employment start date on the offer. | [optional]
**status** | [**OfferStatusEnum**](OfferStatusEnum.md) | The offer&#39;s status. | [optional]
**remote_data** | [**\MergeATSClient\Model\RemoteData[]**](RemoteData.md) |  | [optional] [readonly]
**remote_was_deleted** | **bool** | Indicates whether or not this object has been deleted by third party webhooks. | [optional] [readonly]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
