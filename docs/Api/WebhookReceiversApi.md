# MergeATSClient\WebhookReceiversApi

All URIs are relative to https://api.merge.dev/api/ats/v1.

Method | HTTP request | Description
------------- | ------------- | -------------
[**webhookReceiversCreate()**](WebhookReceiversApi.md#webhookReceiversCreate) | **POST** /webhook-receivers | 
[**webhookReceiversList()**](WebhookReceiversApi.md#webhookReceiversList) | **GET** /webhook-receivers | 


## `webhookReceiversCreate()`

```php
webhookReceiversCreate($x_account_token, $webhook_receiver_request): \MergeATSClient\Model\WebhookReceiver
```



Creates a `WebhookReceiver` object with the given values.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: tokenAuth
$config = MergeATSClient\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = MergeATSClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new MergeATSClient\Api\WebhookReceiversApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_account_token = 'x_account_token_example'; // string | Token identifying the end user.
$webhook_receiver_request = new \MergeATSClient\Model\WebhookReceiverRequest(); // \MergeATSClient\Model\WebhookReceiverRequest

try {
    $result = $apiInstance->webhookReceiversCreate($x_account_token, $webhook_receiver_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhookReceiversApi->webhookReceiversCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_account_token** | **string**| Token identifying the end user. |
 **webhook_receiver_request** | [**\MergeATSClient\Model\WebhookReceiverRequest**](../Model/WebhookReceiverRequest.md)|  |

### Return type

[**\MergeATSClient\Model\WebhookReceiver**](../Model/WebhookReceiver.md)

### Authorization

[tokenAuth](../../README.md#tokenAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`, `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `webhookReceiversList()`

```php
webhookReceiversList($x_account_token): \MergeATSClient\Model\WebhookReceiver[]
```



Returns a list of `WebhookReceiver` objects.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: tokenAuth
$config = MergeATSClient\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = MergeATSClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new MergeATSClient\Api\WebhookReceiversApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_account_token = 'x_account_token_example'; // string | Token identifying the end user.

try {
    $result = $apiInstance->webhookReceiversList($x_account_token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhookReceiversApi->webhookReceiversList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_account_token** | **string**| Token identifying the end user. |

### Return type

[**\MergeATSClient\Model\WebhookReceiver[]**](../Model/WebhookReceiver.md)

### Authorization

[tokenAuth](../../README.md#tokenAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
