# ClickSend\AccountApi

All URIs are relative to *https://rest.clicksend.com/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**accountGet**](AccountApi.md#accountGet) | **GET** /account | Get account information
[**accountPost**](AccountApi.md#accountPost) | **POST** /account | Create a new account
[**accountVerifySendPut**](AccountApi.md#accountVerifySendPut) | **PUT** /account-verify/send | Send account activation token
[**accountVerifyVerifyByActivationTokenPut**](AccountApi.md#accountVerifyVerifyByActivationTokenPut) | **PUT** /account-verify/verify/{activation_token} | Verify new account
[**forgotPasswordPut**](AccountApi.md#forgotPasswordPut) | **PUT** /forgot-password | Forgot password
[**forgotPasswordVerifyPut**](AccountApi.md#forgotPasswordVerifyPut) | **PUT** /forgot-password/verify | Verify forgot password
[**forgotUsernamePut**](AccountApi.md#forgotUsernamePut) | **PUT** /forgot-username | Forgot username


# **accountGet**
> string accountGet()

Get account information

Get account details

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: BasicAuth
$config = ClickSend\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new ClickSend\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->accountGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->accountGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

**string**

### Authorization

[BasicAuth](../../README.md#BasicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **accountPost**
> string accountPost($account)

Create a new account

Create An Account

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: BasicAuth
$config = ClickSend\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new ClickSend\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account = new \ClickSend\ClickSend.Model\Account(); // \ClickSend\ClickSend.Model\Account | Account model

try {
    $result = $apiInstance->accountPost($account);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->accountPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **account** | [**\ClickSend\ClickSend.Model\Account**](../Model/Account.md)| Account model |

### Return type

**string**

### Authorization

[BasicAuth](../../README.md#BasicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **accountVerifySendPut**
> string accountVerifySendPut($account_verify)

Send account activation token

Send account activation token

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: BasicAuth
$config = ClickSend\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new ClickSend\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_verify = new \ClickSend\ClickSend.Model\AccountVerify(); // \ClickSend\ClickSend.Model\AccountVerify | Account details

try {
    $result = $apiInstance->accountVerifySendPut($account_verify);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->accountVerifySendPut: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **account_verify** | [**\ClickSend\ClickSend.Model\AccountVerify**](../Model/AccountVerify.md)| Account details |

### Return type

**string**

### Authorization

[BasicAuth](../../README.md#BasicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **accountVerifyVerifyByActivationTokenPut**
> string accountVerifyVerifyByActivationTokenPut($activation_token)

Verify new account

Verify new account

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: BasicAuth
$config = ClickSend\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new ClickSend\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$activation_token = 56; // int | 

try {
    $result = $apiInstance->accountVerifyVerifyByActivationTokenPut($activation_token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->accountVerifyVerifyByActivationTokenPut: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **activation_token** | **int**|  |

### Return type

**string**

### Authorization

[BasicAuth](../../README.md#BasicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **forgotPasswordPut**
> string forgotPasswordPut($username)

Forgot password

Forgot password

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: BasicAuth
$config = ClickSend\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new ClickSend\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$username = "username_example"; // string | Username belonging to account

try {
    $result = $apiInstance->forgotPasswordPut($username);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->forgotPasswordPut: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **username** | **string**| Username belonging to account |

### Return type

**string**

### Authorization

[BasicAuth](../../README.md#BasicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **forgotPasswordVerifyPut**
> string forgotPasswordVerifyPut($verify_password)

Verify forgot password

Verify forgot password

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure HTTP basic authorization: BasicAuth
$config = ClickSend\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new ClickSend\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$verify_password = new \ClickSend\ClickSend.Model\AccountForgotPasswordVerify(); // \ClickSend\ClickSend.Model\AccountForgotPasswordVerify | verifyPassword data

try {
    $result = $apiInstance->forgotPasswordVerifyPut($verify_password);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->forgotPasswordVerifyPut: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **verify_password** | [**\ClickSend\ClickSend.Model\AccountForgotPasswordVerify**](../Model/AccountForgotPasswordVerify.md)| verifyPassword data |

### Return type

**string**

### Authorization

[BasicAuth](../../README.md#BasicAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **forgotUsernamePut**
> string forgotUsernamePut($email)

Forgot username

Forgot username

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new ClickSend\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$email = "email_example"; // string | Email belonging to account

try {
    $result = $apiInstance->forgotUsernamePut($email);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->forgotUsernamePut: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **email** | **string**| Email belonging to account |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)
