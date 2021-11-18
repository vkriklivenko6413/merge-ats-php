# MergeHRISClient\CandidatesApi

All URIs are relative to https://api.merge.dev/api/ats/v1.

Method | HTTP request | Description
------------- | ------------- | -------------
[**candidatesCreate()**](CandidatesApi.md#candidatesCreate) | **POST** /candidates | 
[**candidatesList()**](CandidatesApi.md#candidatesList) | **GET** /candidates | 
[**candidatesRetrieve()**](CandidatesApi.md#candidatesRetrieve) | **GET** /candidates/{id} | 


## `candidatesCreate()`

```php
candidatesCreate($x_account_token, $remote_user_id, $run_async, $candidate_request): \MergeHRISClient\Model\Candidate
```



Creates a `Candidate` object with the given values.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: tokenAuth
$config = MergeHRISClient\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = MergeHRISClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new MergeHRISClient\Api\CandidatesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_account_token = 'x_account_token_example'; // string | Token identifying the end user.
$remote_user_id = 'remote_user_id_example'; // string | The ID of the RemoteUser modifying the resource. This can be found in the ID field (not remote_id) in the RemoteUser table.
$run_async = True; // bool | Whether or not third-party updates should be run asynchronously.
$candidate_request = new \MergeHRISClient\Model\CandidateRequest(); // \MergeHRISClient\Model\CandidateRequest

try {
    $result = $apiInstance->candidatesCreate($x_account_token, $remote_user_id, $run_async, $candidate_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CandidatesApi->candidatesCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_account_token** | **string**| Token identifying the end user. |
 **remote_user_id** | **string**| The ID of the RemoteUser modifying the resource. This can be found in the ID field (not remote_id) in the RemoteUser table. | [optional]
 **run_async** | **bool**| Whether or not third-party updates should be run asynchronously. | [optional]
 **candidate_request** | [**\MergeHRISClient\Model\CandidateRequest**](../Model/CandidateRequest.md)|  | [optional]

### Return type

[**\MergeHRISClient\Model\Candidate**](../Model/Candidate.md)

### Authorization

[tokenAuth](../../README.md#tokenAuth)

### HTTP request headers

- **Content-Type**: `application/json`, `application/x-www-form-urlencoded`, `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `candidatesList()`

```php
candidatesList($x_account_token, $created_after, $created_before, $cursor, $email_address, $expand, $first_name, $include_remote_data, $last_name, $modified_after, $modified_before, $page_size, $remote_id, $tag): \MergeHRISClient\Model\PaginatedCandidateList
```



Returns a list of `Candidate` objects.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: tokenAuth
$config = MergeHRISClient\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = MergeHRISClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new MergeHRISClient\Api\CandidatesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_account_token = 'x_account_token_example'; // string | Token identifying the end user.
$created_after = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | If provided, will only return objects created after this datetime.
$created_before = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | If provided, will only return objects created before this datetime.
$cursor = cD0yMDIxLTAxLTA2KzAzJTNBMjQlM0E1My40MzQzMjYlMkIwMCUzQTAw; // string | The pagination cursor value.
$email_address = 'email_address_example'; // string | If provided, will only return candidates with this email_address.
$expand = applications,attachments; // string | Which relations should be returned in expanded form. Multiple relation names should be comma separated without spaces.
$first_name = 'first_name_example'; // string | If provided, will only return candidates with this first name.
$include_remote_data = True; // bool | Whether to include the original data Merge fetched from the third-party to produce these models.
$last_name = 'last_name_example'; // string | If provided, will only return candidates with this last name.
$modified_after = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | If provided, will only return objects modified after this datetime.
$modified_before = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | If provided, will only return objects modified before this datetime.
$page_size = 56; // int | Number of results to return per page.
$remote_id = 'remote_id_example'; // string | The API provider's ID for the given object.
$tag = 'tag_example'; // string | If provided, will only return candidates with this tag.

try {
    $result = $apiInstance->candidatesList($x_account_token, $created_after, $created_before, $cursor, $email_address, $expand, $first_name, $include_remote_data, $last_name, $modified_after, $modified_before, $page_size, $remote_id, $tag);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CandidatesApi->candidatesList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_account_token** | **string**| Token identifying the end user. |
 **created_after** | **\DateTime**| If provided, will only return objects created after this datetime. | [optional]
 **created_before** | **\DateTime**| If provided, will only return objects created before this datetime. | [optional]
 **cursor** | **string**| The pagination cursor value. | [optional]
 **email_address** | **string**| If provided, will only return candidates with this email_address. | [optional]
 **expand** | **string**| Which relations should be returned in expanded form. Multiple relation names should be comma separated without spaces. | [optional]
 **first_name** | **string**| If provided, will only return candidates with this first name. | [optional]
 **include_remote_data** | **bool**| Whether to include the original data Merge fetched from the third-party to produce these models. | [optional]
 **last_name** | **string**| If provided, will only return candidates with this last name. | [optional]
 **modified_after** | **\DateTime**| If provided, will only return objects modified after this datetime. | [optional]
 **modified_before** | **\DateTime**| If provided, will only return objects modified before this datetime. | [optional]
 **page_size** | **int**| Number of results to return per page. | [optional]
 **remote_id** | **string**| The API provider&#39;s ID for the given object. | [optional]
 **tag** | **string**| If provided, will only return candidates with this tag. | [optional]

### Return type

[**\MergeHRISClient\Model\PaginatedCandidateList**](../Model/PaginatedCandidateList.md)

### Authorization

[tokenAuth](../../README.md#tokenAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `candidatesRetrieve()`

```php
candidatesRetrieve($x_account_token, $id, $expand, $include_remote_data): \MergeHRISClient\Model\Candidate
```



Returns a `Candidate` object with the given `id`.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: tokenAuth
$config = MergeHRISClient\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = MergeHRISClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new MergeHRISClient\Api\CandidatesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_account_token = 'x_account_token_example'; // string | Token identifying the end user.
$id = 'id_example'; // string
$expand = applications,attachments; // string | Which relations should be returned in expanded form. Multiple relation names should be comma separated without spaces.
$include_remote_data = True; // bool | Whether to include the original data Merge fetched from the third-party to produce these models.

try {
    $result = $apiInstance->candidatesRetrieve($x_account_token, $id, $expand, $include_remote_data);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CandidatesApi->candidatesRetrieve: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_account_token** | **string**| Token identifying the end user. |
 **id** | [**string**](../Model/.md)|  |
 **expand** | **string**| Which relations should be returned in expanded form. Multiple relation names should be comma separated without spaces. | [optional]
 **include_remote_data** | **bool**| Whether to include the original data Merge fetched from the third-party to produce these models. | [optional]

### Return type

[**\MergeHRISClient\Model\Candidate**](../Model/Candidate.md)

### Authorization

[tokenAuth](../../README.md#tokenAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
