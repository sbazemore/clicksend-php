# ClickSend\UploadApi

All URIs are relative to *https://rest.clicksend.com/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**uploadsPost**](UploadApi.md#uploadsPost) | **POST** /uploads | Upload File


# **uploadsPost**
> string uploadsPost($convert, $upload_file)

Upload File

Upload File

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: BasicAuth
$config = ClickSend\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new ClickSend\Api\UploadApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$convert = "convert_example"; // string | 
$upload_file = new \ClickSend\Model\UploadFile(); // \ClickSend\Model\UploadFile | 

try {
    $result = $apiInstance->uploadsPost($convert, $upload_file);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UploadApi->uploadsPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **convert** | **string**|  |
 **upload_file** | [**\ClickSend\Model\UploadFile**](../Model/UploadFile.md)|  | [optional]

### Return type

**string**

### Authorization

[BasicAuth](../../README.md#BasicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

