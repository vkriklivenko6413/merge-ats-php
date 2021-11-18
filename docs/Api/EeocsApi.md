# MergeHRISClient\EeocsApi

All URIs are relative to https://api.merge.dev/api/ats/v1.

Method | HTTP request | Description
------------- | ------------- | -------------
[**eeocsList()**](EeocsApi.md#eeocsList) | **GET** /eeocs | 
[**eeocsRetrieve()**](EeocsApi.md#eeocsRetrieve) | **GET** /eeocs/{id} | 


## `eeocsList()`

```php
eeocsList($x_account_token, $candidate_id, $created_after, $created_before, $cursor, $expand, $include_remote_data, $modified_after, $modified_before, $page_size, $remote_id): \MergeHRISClient\Model\PaginatedEEOCList
```



Returns a list of `EEOC` objects.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: tokenAuth
$config = MergeHRISClient\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = MergeHRISClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new MergeHRISClient\Api\EeocsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_account_token = 'x_account_token_example'; // string | Token identifying the end user.
$candidate_id = 'candidate_id_example'; // string | If provided, will only return EEOC info for this candidate.
$created_after = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | If provided, will only return objects created after this datetime.
$created_before = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | If provided, will only return objects created before this datetime.
$cursor = cD0yMDIxLTAxLTA2KzAzJTNBMjQlM0E1My40MzQzMjYlMkIwMCUzQTAw; // string | The pagination cursor value.
$expand = candidate; // string | Which relations should be returned in expanded form. Multiple relation names should be comma separated without spaces.
$include_remote_data = True; // bool | Whether to include the original data Merge fetched from the third-party to produce these models.
$modified_after = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | If provided, will only return objects modified after this datetime.
$modified_before = new \DateTime("2013-10-20T19:20:30+01:00"); // \DateTime | If provided, will only return objects modified before this datetime.
$page_size = 56; // int | Number of results to return per page.
$remote_id = 'remote_id_example'; // string | The API provider's ID for the given object.

try {
    $result = $apiInstance->eeocsList($x_account_token, $candidate_id, $created_after, $created_before, $cursor, $expand, $include_remote_data, $modified_after, $modified_before, $page_size, $remote_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EeocsApi->eeocsList: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_account_token** | **string**| Token identifying the end user. |
 **candidate_id** | **string**| If provided, will only return EEOC info for this candidate. | [optional]
 **created_after** | **\DateTime**| If provided, will only return objects created after this datetime. | [optional]
 **created_before** | **\DateTime**| If provided, will only return objects created before this datetime. | [optional]
 **cursor** | **string**| The pagination cursor value. | [optional]
 **expand** | **string**| Which relations should be returned in expanded form. Multiple relation names should be comma separated without spaces. | [optional]
 **include_remote_data** | **bool**| Whether to include the original data Merge fetched from the third-party to produce these models. | [optional]
 **modified_after** | **\DateTime**| If provided, will only return objects modified after this datetime. | [optional]
 **modified_before** | **\DateTime**| If provided, will only return objects modified before this datetime. | [optional]
 **page_size** | **int**| Number of results to return per page. | [optional]
 **remote_id** | **string**| The API provider&#39;s ID for the given object. | [optional]

### Return type

[**\MergeHRISClient\Model\PaginatedEEOCList**](../Model/PaginatedEEOCList.md)

### Authorization

[tokenAuth](../../README.md#tokenAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `eeocsRetrieve()`

```php
eeocsRetrieve($x_account_token, $id, $expand, $include_remote_data): \MergeHRISClient\Model\EEOC
```



Returns an `EEOC` object with the given `id`.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: tokenAuth
$config = MergeHRISClient\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = MergeHRISClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');


$apiInstance = new MergeHRISClient\Api\EeocsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_account_token = 'x_account_token_example'; // string | Token identifying the end user.
$id = 'id_example'; // string
$expand = candidate; // string | Which relations should be returned in expanded form. Multiple relation names should be comma separated without spaces.
$include_remote_data = True; // bool | Whether to include the original data Merge fetched from the third-party to produce these models.

try {
    $result = $apiInstance->eeocsRetrieve($x_account_token, $id, $expand, $include_remote_data);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EeocsApi->eeocsRetrieve: ', $e->getMessage(), PHP_EOL;
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

[**\MergeHRISClient\Model\EEOC**](../Model/EEOC.md)

### Authorization

[tokenAuth](../../README.md#tokenAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
