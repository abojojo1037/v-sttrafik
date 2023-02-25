# Swagger\Client\SysteminfoApi

All URIs are relative to *https://api.vasttrafik.se/bin/rest.exe/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getSystemInfo**](SysteminfoApi.md#getSystemInfo) | **GET** /systeminfo | Provides information about the journey planner and the underlying data


# **getSystemInfo**
> \Swagger\Client\Model\SystemInfo getSystemInfo($format, $jsonp_callback)

Provides information about the journey planner and the underlying data

Provides information about the journey planner and underlying data. It will return the begin of end of the timetable period and the creation date of the timetable data.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\SysteminfoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$format = "format_example"; // string | the required response format
$jsonp_callback = "jsonp_callback_example"; // string | If JSONP response format is needed, you can append an additional parameter to specify the name of a callback function, and the JSON object will be wrapped by a function call with this name.

try {
    $result = $apiInstance->getSystemInfo($format, $jsonp_callback);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SysteminfoApi->getSystemInfo: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **format** | **string**| the required response format | [optional]
 **jsonp_callback** | **string**| If JSONP response format is needed, you can append an additional parameter to specify the name of a callback function, and the JSON object will be wrapped by a function call with this name. | [optional]

### Return type

[**\Swagger\Client\Model\SystemInfo**](../Model/SystemInfo.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

