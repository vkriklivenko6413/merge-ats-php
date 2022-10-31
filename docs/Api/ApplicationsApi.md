# MergeATSClient\ApplicationsApi

All URIs are relative to https://api.merge.dev/api/ats/v1.

Method | HTTP request | Description
------------- | ------------- | -------------
[**applicationsChangeStageCreate()**](ApplicationsApi.md#applicationsChangeStageCreate) | **POST** /applications/{id}/change-stage | 
[**applicationsCreate()**](ApplicationsApi.md#applicationsCreate) | **POST** /applications | 
[**applicationsList()**](ApplicationsApi.md#applicationsList) | **GET** /applications | 
[**applicationsMetaPostRetrieve()**](ApplicationsApi.md#applicationsMetaPostRetrieve) | **GET** /applications/meta/post | 
[**applicationsRetrieve()**](ApplicationsApi.md#applicationsRetrieve) | **GET** /applications/{id} | 


## `applicationsChangeStageCreate()`

```php
applicationsChangeStageCreate($x_account_token, $id, $is_debug_mode, $run_async, $update_application_stage_request): \MergeATSClient\Model\ApplicationResponse
```



Updates the `current_stage` field of an `Application` object

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: tokenAuth
$config = MergeATSClient\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = MergeATSClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new MergeATSClient\Api\ApplicationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_account_token = 'x_account_token_example'; // string | Token identifying the end user.
$id = 'id_example'; // string
$is_debug_mode = True; // bool | Whether to include debug fields (such as log file links) in the response.
$run_async = True; // bool | Whether or not third-party updates should be run asynchronously.
$update_application_stage_request = new \MergeATSClient\Model\UpdateApplicationStageRequest(); // \MergeATSClient\Model\UpdateApplicationStageRequest

try {
    $result = $apiInstance->applicationsChangeStageCreate($x_account_token, $id, $is_debug_mode, $run_async, $update_application_stage_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApplicationsApi->applicationsChangeStageCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_account_token** | **string**| Token identifying the end user. |
 **id** | [**string**](../Model/.md)|  |
 **is_debug_mode** | **bool**| Whether to include debug fields (such as log file links) in the response. | [optional]
 **run_async** | **bool**| Whether or not third-party updates should be run asynchronously. | [optional]
 **update_application_stage_request** | [**\MergeATSClient\Model\UpdateApplicationStageRequest**](../Model/UpdateApplicationStageRequest.md)|  | [optional]

### Return type

[**\MergeATSClient\Model\ApplicationResponse**](../Model/ApplicationResponse.md)

### Authorization

[tokenAuth](../../README.md#tokenAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`, `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `applicationsCreate()`

```php
applicationsCreate($x_account_token, $application_endpoint_request, $is_debug_mode, $run_async): \MergeATSClient\Model\ApplicationResponse
```



Creates an `Application` object with the given values.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: tokenAuth
$config = MergeATSClient\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = MergeATSClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new MergeATSClient\Api\ApplicationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_account_token = 'x_account_token_example'; // string | Token identifying the end user.
$application_endpoint_request = new \MergeATSClient\Model\ApplicationEndpointRequest(); // \MergeATSClient\Model\ApplicationEndpointRequest
$is_debug_mode = True; // bool | Whether to include debug fields (such as log file links) in the response.
$run_async = True; // bool | Whether or not third-party updates should be run asynchronously.

try {
    $result = $apiInstance->applicationsCreate($x_account_token, $application_endpoint_request, $is_debug_mode, $run_async);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApplicationsApi->applicationsCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_account_token** | **string**| Token identifying the end user. |
 **application_endpoint_request** | [**\MergeATSClient\Model\ApplicationEndpointRequest**](../Model/ApplicationEndpointRequest.md)|  |
 **is_debug_mode** | **bool**| Whether to include debug fields (such as log file links) in the response. | [optional]
 **run_async** | **bool**| Whether or not third-party updates should be run asynchronously. | [optional]

### Return type

[**\MergeATSClient\Model\ApplicationResponse**](../Model/ApplicationResponse.md)

### Authorization

[tokenAuth](../../README.md#tokenAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`, `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `applicationsList()`

```php
applicationsList($x_account_token, $candidate_id, $created_after, $created_before, $credited_to_id, $current_stage_id, $cursor, $include_deleted_data, $include_remote_data, $job_id, $modified_after, $modified_before, $page_size, $reject_reason_id, $remote_id, $source): \MergeATSClient\Model\PaginatedApplicationList
```



Returns a list of `Application` objects.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: tokenAuth
$config = MergeATSClient\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = MergeATSClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new MergeATSClient\Api\ApplicationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_account_token = 'x_account_token_example'; // string | Token identifying the end user.
$candidate_id = 'candidate_id_example'; // string | If provided, will only return applications for this candidate.
$created_after = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | If provided, will only return objects created after this datetime.
$created_before = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | If provided, will only return objects created before this datetime.
$credited_to_id = 'credited_to_id_example'; // string | If provided, will only return applications credited to this user.
$current_stage_id = 'current_stage_id_example'; // string | If provided, will only return applications at this interview stage.
$cursor = cD0yMDIxLTAxLTA2KzAzJTNBMjQlM0E1My40MzQzMjYlMkIwMCUzQTAw; // string | The pagination cursor value.
$include_deleted_data = True; // bool | Whether to include data that was marked as deleted by third party webhooks.
$include_remote_data = True; // bool | Whether to include the original data Merge fetched from the third-party to produce these models.
$job_id = 'job_id_example'; // string | If provided, will only return applications for this job.
$modified_after = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | If provided, will only return objects modified after this datetime.
$modified_before = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | If provided, will only return objects modified before this datetime.
$page_size = 56; // int | Number of results to return per page.
$reject_reason_id = 'reject_reason_id_example'; // string | If provided, will only return applications with this reject reason.
$remote_id = 'remote_id_example'; // string | The API provider's ID for the given object.
$source = 'source_example'; // string | If provided, will only return applications with this source.

try {
    $result = $apiInstance->applicationsList($x_account_token, $candidate_id, $created_after, $created_before, $credited_to_id, $current_stage_id, $cursor, $include_deleted_data, $include_remote_data, $job_id, $modified_after, $modified_before, $page_size, $reject_reason_id, $remote_id, $source);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApplicationsApi->applicationsList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_account_token** | **string**| Token identifying the end user. |
 **candidate_id** | **string**| If provided, will only return applications for this candidate. | [optional]
 **created_after** | **\DateTime**| If provided, will only return objects created after this datetime. | [optional]
 **created_before** | **\DateTime**| If provided, will only return objects created before this datetime. | [optional]
 **credited_to_id** | **string**| If provided, will only return applications credited to this user. | [optional]
 **current_stage_id** | **string**| If provided, will only return applications at this interview stage. | [optional]
 **cursor** | **string**| The pagination cursor value. | [optional]
 **include_deleted_data** | **bool**| Whether to include data that was marked as deleted by third party webhooks. | [optional]
 **include_remote_data** | **bool**| Whether to include the original data Merge fetched from the third-party to produce these models. | [optional]
 **job_id** | **string**| If provided, will only return applications for this job. | [optional]
 **modified_after** | **\DateTime**| If provided, will only return objects modified after this datetime. | [optional]
 **modified_before** | **\DateTime**| If provided, will only return objects modified before this datetime. | [optional]
 **page_size** | **int**| Number of results to return per page. | [optional]
 **reject_reason_id** | **string**| If provided, will only return applications with this reject reason. | [optional]
 **remote_id** | **string**| The API provider&#39;s ID for the given object. | [optional]
 **source** | **string**| If provided, will only return applications with this source. | [optional]

### Return type

[**\MergeATSClient\Model\PaginatedApplicationList**](../Model/PaginatedApplicationList.md)

### Authorization

[tokenAuth](../../README.md#tokenAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `applicationsMetaPostRetrieve()`

```php
applicationsMetaPostRetrieve($x_account_token, $application_remote_template_id): \MergeATSClient\Model\MetaResponse
```



Returns metadata for `Application` POSTs.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: tokenAuth
$config = MergeATSClient\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = MergeATSClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new MergeATSClient\Api\ApplicationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_account_token = 'x_account_token_example'; // string | Token identifying the end user.
$application_remote_template_id = 'application_remote_template_id_example'; // string | The template ID associated with the nested application in the request.

try {
    $result = $apiInstance->applicationsMetaPostRetrieve($x_account_token, $application_remote_template_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApplicationsApi->applicationsMetaPostRetrieve: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_account_token** | **string**| Token identifying the end user. |
 **application_remote_template_id** | **string**| The template ID associated with the nested application in the request. | [optional]

### Return type

[**\MergeATSClient\Model\MetaResponse**](../Model/MetaResponse.md)

### Authorization

[tokenAuth](../../README.md#tokenAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `applicationsRetrieve()`

```php
applicationsRetrieve($x_account_token, $id, $include_remote_data): \MergeATSClient\Model\Application
```



Returns an `Application` object with the given `id`.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: tokenAuth
$config = MergeATSClient\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = MergeATSClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new MergeATSClient\Api\ApplicationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_account_token = 'x_account_token_example'; // string | Token identifying the end user.
$id = 'id_example'; // string
$include_remote_data = True; // bool | Whether to include the original data Merge fetched from the third-party to produce these models.

try {
    $result = $apiInstance->applicationsRetrieve($x_account_token, $id, $include_remote_data);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApplicationsApi->applicationsRetrieve: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_account_token** | **string**| Token identifying the end user. |
 **id** | [**string**](../Model/.md)|  |
 **include_remote_data** | **bool**| Whether to include the original data Merge fetched from the third-party to produce these models. | [optional]

### Return type

[**\MergeATSClient\Model\Application**](../Model/Application.md)

### Authorization

[tokenAuth](../../README.md#tokenAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
