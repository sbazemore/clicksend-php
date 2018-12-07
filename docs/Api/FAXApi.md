# ClickSend\FAXApi

All URIs are relative to *https://rest.clicksend.com/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**faxReceiptsGet**](FAXApi.md#faxReceiptsGet) | **GET** /fax/receipts | Get all delivery receipts
[**faxReceiptsPost**](FAXApi.md#faxReceiptsPost) | **POST** /fax/receipts | Add a delivery receipt
[**faxReceiptsReadPut**](FAXApi.md#faxReceiptsReadPut) | **PUT** /fax/receipts-read | Mark delivery receipts as read


# **faxReceiptsGet**
> string faxReceiptsGet($page, $limit)

Get all delivery receipts

Get all delivery receipts

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: BasicAuth
$config = ClickSend\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new ClickSend\Api\FAXApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 1; // int | Page number
$limit = 10; // int | Number of records per page

try {
    $result = $apiInstance->faxReceiptsGet($page, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FAXApi->faxReceiptsGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**| Page number | [optional] [default to 1]
 **limit** | **int**| Number of records per page | [optional] [default to 10]

### Return type

**string**

### Authorization

[BasicAuth](../../README.md#BasicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **faxReceiptsPost**
> string faxReceiptsPost($url)

Add a delivery receipt

Add a delivery receipt

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: BasicAuth
$config = ClickSend\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new ClickSend\Api\FAXApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$url = new \ClickSend\Model\Url(); // \ClickSend\Model\Url | Url model

try {
    $result = $apiInstance->faxReceiptsPost($url);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FAXApi->faxReceiptsPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **url** | [**\ClickSend\Model\Url**](../Model/Url.md)| Url model |

### Return type

**string**

### Authorization

[BasicAuth](../../README.md#BasicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **faxReceiptsReadPut**
> string faxReceiptsReadPut($date_before)

Mark delivery receipts as read

Mark delivery receipts as read

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: BasicAuth
$config = ClickSend\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new ClickSend\Api\FAXApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$date_before = new \ClickSend\Model\DateBefore(); // \ClickSend\Model\DateBefore | DateBefore model

try {
    $result = $apiInstance->faxReceiptsReadPut($date_before);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FAXApi->faxReceiptsReadPut: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **date_before** | [**\ClickSend\Model\DateBefore**](../Model/DateBefore.md)| DateBefore model | [optional]

### Return type

**string**

### Authorization

[BasicAuth](../../README.md#BasicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

