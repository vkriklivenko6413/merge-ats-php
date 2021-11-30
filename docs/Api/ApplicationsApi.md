# MergeATSClient\ApplicationsApi

All URIs are relative to https://api.merge.dev/api/ats/v1.

Method | HTTP request | Description
------------- | ------------- | -------------
[**applicationsCreate()**](ApplicationsApi.md#applicationsCreate) | **POST** /applications | 
[**applicationsList()**](ApplicationsApi.md#applicationsList) | **GET** /applications | 
[**applicationsRetrieve()**](ApplicationsApi.md#applicationsRetrieve) | **GET** /applications/{id} | 


## `applicationsCreate()`

```php
applicationsCreate($x_account_token, $remote_user_id, $run_async, $application_request): \MergeATSClient\Model\Application
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
$remote_user_id = 'remote_user_id_example'; // string | The ID of the RemoteUser modifying the resource. This can be found in the ID field (not remote_id) in the RemoteUser table.
$run_async = True; // bool | Whether or not third-party updates should be run asynchronously.
$application_request = new \MergeATSClient\Model\ApplicationRequest(); // \MergeATSClient\Model\ApplicationRequest

try {
    $result = $apiInstance->applicationsCreate($x_account_token, $remote_user_id, $run_async, $application_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ApplicationsApi->applicationsCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_account_token** | **string**| Token identifying the end user. |
 **remote_user_id** | **string**| The ID of the RemoteUser modifying the resource. This can be found in the ID field (not remote_id) in the RemoteUser table. | [optional]
 **run_async** | **bool**| Whether or not third-party updates should be run asynchronously. | [optional]
 **application_request** | [**\MergeATSClient\Model\ApplicationRequest**](../Model/ApplicationRequest.md)|  | [optional]

### Return type

[**\MergeATSClient\Model\Application**](../Model/Application.md)

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
applicationsList($x_account_token, $candidate_id, $created_after, $created_before, $credited_to_id, $current_stage_id, $cursor, $include_remote_data, $job_id, $modified_after, $modified_before, $page_size, $reject_reason_id, $remote_id): \MergeATSClient\Model\PaginatedApplicationList
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
$include_remote_data = True; // bool | Whether to include the original data Merge fetched from the third-party to produce these models.
$job_id = 'job_id_example'; // string | If provided, will only return applications for this job.
$modified_after = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | If provided, will only return objects modified after this datetime.
$modified_before = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | If provided, will only return objects modified before this datetime.
$page_size = 56; // int | Number of results to return per page.
$reject_reason_id = 'reject_reason_id_example'; // string | If provided, will only return applications with this reject reason.
$remote_id = 'remote_id_example'; // string | The API provider's ID for the given object.

try {
    $result = $apiInstance->applicationsList($x_account_token, $candidate_id, $created_after, $created_before, $credited_to_id, $current_stage_id, $cursor, $include_remote_data, $job_id, $modified_after, $modified_before, $page_size, $reject_reason_id, $remote_id);
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
 **include_remote_data** | **bool**| Whether to include the original data Merge fetched from the third-party to produce these models. | [optional]
 **job_id** | **string**| If provided, will only return applications for this job. | [optional]
 **modified_after** | **\DateTime**| If provided, will only return objects modified after this datetime. | [optional]
 **modified_before** | **\DateTime**| If provided, will only return objects modified before this datetime. | [optional]
 **page_size** | **int**| Number of results to return per page. | [optional]
 **reject_reason_id** | **string**| If provided, will only return applications with this reject reason. | [optional]
 **remote_id** | **string**| The API provider&#39;s ID for the given object. | [optional]

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
