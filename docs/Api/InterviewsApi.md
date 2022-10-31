# MergeATSClient\InterviewsApi

All URIs are relative to https://api.merge.dev/api/ats/v1.

Method | HTTP request | Description
------------- | ------------- | -------------
[**interviewsList()**](InterviewsApi.md#interviewsList) | **GET** /interviews | 
[**interviewsRetrieve()**](InterviewsApi.md#interviewsRetrieve) | **GET** /interviews/{id} | 


## `interviewsList()`

```php
interviewsList($x_account_token, $application_id, $created_after, $created_before, $cursor, $include_deleted_data, $include_remote_data, $job_interview_stage_id, $modified_after, $modified_before, $organizer_id, $page_size, $remote_fields, $remote_id): \MergeATSClient\Model\PaginatedScheduledInterviewList
```



Returns a list of `ScheduledInterview` objects.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: tokenAuth
$config = MergeATSClient\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = MergeATSClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new MergeATSClient\Api\InterviewsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_account_token = 'x_account_token_example'; // string | Token identifying the end user.
$application_id = 'application_id_example'; // string | If provided, will only return interviews for this application.
$created_after = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | If provided, will only return objects created after this datetime.
$created_before = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | If provided, will only return objects created before this datetime.
$cursor = cD0yMDIxLTAxLTA2KzAzJTNBMjQlM0E1My40MzQzMjYlMkIwMCUzQTAw; // string | The pagination cursor value.
$include_deleted_data = True; // bool | Whether to include data that was marked as deleted by third party webhooks.
$include_remote_data = True; // bool | Whether to include the original data Merge fetched from the third-party to produce these models.
$job_interview_stage_id = 'job_interview_stage_id_example'; // string | If provided, will only return interviews at this stage.
$modified_after = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | If provided, will only return objects modified after this datetime.
$modified_before = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | If provided, will only return objects modified before this datetime.
$organizer_id = 'organizer_id_example'; // string | If provided, will only return interviews organized by this user.
$page_size = 56; // int | Number of results to return per page.
$remote_fields = status; // string | Which fields should be returned in non-normalized form.
$remote_id = 'remote_id_example'; // string | The API provider's ID for the given object.

try {
    $result = $apiInstance->interviewsList($x_account_token, $application_id, $created_after, $created_before, $cursor, $include_deleted_data, $include_remote_data, $job_interview_stage_id, $modified_after, $modified_before, $organizer_id, $page_size, $remote_fields, $remote_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InterviewsApi->interviewsList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_account_token** | **string**| Token identifying the end user. |
 **application_id** | **string**| If provided, will only return interviews for this application. | [optional]
 **created_after** | **\DateTime**| If provided, will only return objects created after this datetime. | [optional]
 **created_before** | **\DateTime**| If provided, will only return objects created before this datetime. | [optional]
 **cursor** | **string**| The pagination cursor value. | [optional]
 **include_deleted_data** | **bool**| Whether to include data that was marked as deleted by third party webhooks. | [optional]
 **include_remote_data** | **bool**| Whether to include the original data Merge fetched from the third-party to produce these models. | [optional]
 **job_interview_stage_id** | **string**| If provided, will only return interviews at this stage. | [optional]
 **modified_after** | **\DateTime**| If provided, will only return objects modified after this datetime. | [optional]
 **modified_before** | **\DateTime**| If provided, will only return objects modified before this datetime. | [optional]
 **organizer_id** | **string**| If provided, will only return interviews organized by this user. | [optional]
 **page_size** | **int**| Number of results to return per page. | [optional]
 **remote_fields** | **string**| Which fields should be returned in non-normalized form. | [optional]
 **remote_id** | **string**| The API provider&#39;s ID for the given object. | [optional]

### Return type

[**\MergeATSClient\Model\PaginatedScheduledInterviewList**](../Model/PaginatedScheduledInterviewList.md)

### Authorization

[tokenAuth](../../README.md#tokenAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `interviewsRetrieve()`

```php
interviewsRetrieve($x_account_token, $id, $include_remote_data, $remote_fields): \MergeATSClient\Model\ScheduledInterview
```



Returns a `ScheduledInterview` object with the given `id`.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: tokenAuth
$config = MergeATSClient\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = MergeATSClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new MergeATSClient\Api\InterviewsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_account_token = 'x_account_token_example'; // string | Token identifying the end user.
$id = 'id_example'; // string
$include_remote_data = True; // bool | Whether to include the original data Merge fetched from the third-party to produce these models.
$remote_fields = status; // string | Which fields should be returned in non-normalized form.

try {
    $result = $apiInstance->interviewsRetrieve($x_account_token, $id, $include_remote_data, $remote_fields);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InterviewsApi->interviewsRetrieve: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_account_token** | **string**| Token identifying the end user. |
 **id** | [**string**](../Model/.md)|  |
 **include_remote_data** | **bool**| Whether to include the original data Merge fetched from the third-party to produce these models. | [optional]
 **remote_fields** | **string**| Which fields should be returned in non-normalized form. | [optional]

### Return type

[**\MergeATSClient\Model\ScheduledInterview**](../Model/ScheduledInterview.md)

### Authorization

[tokenAuth](../../README.md#tokenAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
