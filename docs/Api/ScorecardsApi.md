# MergeATSClient\ScorecardsApi

All URIs are relative to https://api.merge.dev/api/ats/v1.

Method | HTTP request | Description
------------- | ------------- | -------------
[**scorecardsCreate()**](ScorecardsApi.md#scorecardsCreate) | **POST** /scorecards | 
[**scorecardsList()**](ScorecardsApi.md#scorecardsList) | **GET** /scorecards | 
[**scorecardsRetrieve()**](ScorecardsApi.md#scorecardsRetrieve) | **GET** /scorecards/{id} | 


## `scorecardsCreate()`

```php
scorecardsCreate($x_account_token, $remote_user_id, $run_async, $scorecard_request): \MergeATSClient\Model\Scorecard
```



Creates a `Scorecard` object with the given values.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: tokenAuth
$config = MergeATSClient\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = MergeATSClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new MergeATSClient\Api\ScorecardsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_account_token = 'x_account_token_example'; // string | Token identifying the end user.
$remote_user_id = 'remote_user_id_example'; // string | The ID of the RemoteUser modifying the resource. This can be found in the ID field (not remote_id) in the RemoteUser table.
$run_async = True; // bool | Whether or not third-party updates should be run asynchronously.
$scorecard_request = new \MergeATSClient\Model\ScorecardRequest(); // \MergeATSClient\Model\ScorecardRequest

try {
    $result = $apiInstance->scorecardsCreate($x_account_token, $remote_user_id, $run_async, $scorecard_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ScorecardsApi->scorecardsCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_account_token** | **string**| Token identifying the end user. |
 **remote_user_id** | **string**| The ID of the RemoteUser modifying the resource. This can be found in the ID field (not remote_id) in the RemoteUser table. | [optional]
 **run_async** | **bool**| Whether or not third-party updates should be run asynchronously. | [optional]
 **scorecard_request** | [**\MergeATSClient\Model\ScorecardRequest**](../Model/ScorecardRequest.md)|  | [optional]

### Return type

[**\MergeATSClient\Model\Scorecard**](../Model/Scorecard.md)

### Authorization

[tokenAuth](../../README.md#tokenAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`, `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scorecardsList()`

```php
scorecardsList($x_account_token, $application_id, $created_after, $created_before, $cursor, $include_remote_data, $interview_id, $interviewer_id, $modified_after, $modified_before, $page_size, $remote_id): \MergeATSClient\Model\PaginatedScorecardList
```



Returns a list of `Scorecard` objects.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: tokenAuth
$config = MergeATSClient\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = MergeATSClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new MergeATSClient\Api\ScorecardsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_account_token = 'x_account_token_example'; // string | Token identifying the end user.
$application_id = 'application_id_example'; // string | If provided, will only return scorecards for this application.
$created_after = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | If provided, will only return objects created after this datetime.
$created_before = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | If provided, will only return objects created before this datetime.
$cursor = cD0yMDIxLTAxLTA2KzAzJTNBMjQlM0E1My40MzQzMjYlMkIwMCUzQTAw; // string | The pagination cursor value.
$include_remote_data = True; // bool | Whether to include the original data Merge fetched from the third-party to produce these models.
$interview_id = 'interview_id_example'; // string | If provided, will only return scorecards for this interview.
$interviewer_id = 'interviewer_id_example'; // string | If provided, will only return scorecards for this interviewer.
$modified_after = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | If provided, will only return objects modified after this datetime.
$modified_before = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | If provided, will only return objects modified before this datetime.
$page_size = 56; // int | Number of results to return per page.
$remote_id = 'remote_id_example'; // string | The API provider's ID for the given object.

try {
    $result = $apiInstance->scorecardsList($x_account_token, $application_id, $created_after, $created_before, $cursor, $include_remote_data, $interview_id, $interviewer_id, $modified_after, $modified_before, $page_size, $remote_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ScorecardsApi->scorecardsList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_account_token** | **string**| Token identifying the end user. |
 **application_id** | **string**| If provided, will only return scorecards for this application. | [optional]
 **created_after** | **\DateTime**| If provided, will only return objects created after this datetime. | [optional]
 **created_before** | **\DateTime**| If provided, will only return objects created before this datetime. | [optional]
 **cursor** | **string**| The pagination cursor value. | [optional]
 **include_remote_data** | **bool**| Whether to include the original data Merge fetched from the third-party to produce these models. | [optional]
 **interview_id** | **string**| If provided, will only return scorecards for this interview. | [optional]
 **interviewer_id** | **string**| If provided, will only return scorecards for this interviewer. | [optional]
 **modified_after** | **\DateTime**| If provided, will only return objects modified after this datetime. | [optional]
 **modified_before** | **\DateTime**| If provided, will only return objects modified before this datetime. | [optional]
 **page_size** | **int**| Number of results to return per page. | [optional]
 **remote_id** | **string**| The API provider&#39;s ID for the given object. | [optional]

### Return type

[**\MergeATSClient\Model\PaginatedScorecardList**](../Model/PaginatedScorecardList.md)

### Authorization

[tokenAuth](../../README.md#tokenAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `scorecardsRetrieve()`

```php
scorecardsRetrieve($x_account_token, $id, $include_remote_data): \MergeATSClient\Model\Scorecard
```



Returns a `Scorecard` object with the given `id`.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: tokenAuth
$config = MergeATSClient\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = MergeATSClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new MergeATSClient\Api\ScorecardsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_account_token = 'x_account_token_example'; // string | Token identifying the end user.
$id = 'id_example'; // string
$include_remote_data = True; // bool | Whether to include the original data Merge fetched from the third-party to produce these models.

try {
    $result = $apiInstance->scorecardsRetrieve($x_account_token, $id, $include_remote_data);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ScorecardsApi->scorecardsRetrieve: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_account_token** | **string**| Token identifying the end user. |
 **id** | [**string**](../Model/.md)|  |
 **include_remote_data** | **bool**| Whether to include the original data Merge fetched from the third-party to produce these models. | [optional]

### Return type

[**\MergeATSClient\Model\Scorecard**](../Model/Scorecard.md)

### Authorization

[tokenAuth](../../README.md#tokenAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
