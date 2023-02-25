# Swagger\Client\LocationApi

All URIs are relative to *https://api.vasttrafik.se/bin/rest.exe/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getAllStops**](LocationApi.md#getAllStops) | **GET** /location.allstops | Returns a list of all stops available in the journey planner.
[**getLocationByName**](LocationApi.md#getLocationByName) | **GET** /location.name | Returns a list of possible matches in the journey planner database
[**getNearbyAddress**](LocationApi.md#getNearbyAddress) | **GET** /location.nearbyaddress | Returns the address nearest a given coordinate.
[**getNearbyStops**](LocationApi.md#getNearbyStops) | **GET** /location.nearbystops | Returns a list of stops around a given center coordinate.


# **getAllStops**
> \Swagger\Client\Model\LocationList getAllStops($format, $jsonp_callback)

Returns a list of all stops available in the journey planner.

Returns a list of all stops available in the journey planner. Be aware that a call of this service is very time consuming and should be only requested when it is really needed.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\LocationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$format = "format_example"; // string | the required response format
$jsonp_callback = "jsonp_callback_example"; // string | If JSONP response format is needed, you can append an additional parameter to specify the name of a callback function, and the JSON object will be wrapped by a function call with this name.

try {
    $result = $apiInstance->getAllStops($format, $jsonp_callback);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LocationApi->getAllStops: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **format** | **string**| the required response format | [optional]
 **jsonp_callback** | **string**| If JSONP response format is needed, you can append an additional parameter to specify the name of a callback function, and the JSON object will be wrapped by a function call with this name. | [optional]

### Return type

[**\Swagger\Client\Model\LocationList**](../Model/LocationList.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getLocationByName**
> \Swagger\Client\Model\LocationList getLocationByName($input, $format, $jsonp_callback)

Returns a list of possible matches in the journey planner database

Performs a pattern matching of a user input to retrieve a list of possible matches in the journey planner database. Possible matches might be stops/stations, points of interest and addresses.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\LocationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$input = "input_example"; // string | a string with the user input
$format = "format_example"; // string | the required response format
$jsonp_callback = "jsonp_callback_example"; // string | If JSONP response format is needed, you can append an additional parameter to specify the name of a callback function, and the JSON object will be wrapped by a function call with this name.

try {
    $result = $apiInstance->getLocationByName($input, $format, $jsonp_callback);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LocationApi->getLocationByName: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **input** | **string**| a string with the user input | [optional]
 **format** | **string**| the required response format | [optional]
 **jsonp_callback** | **string**| If JSONP response format is needed, you can append an additional parameter to specify the name of a callback function, and the JSON object will be wrapped by a function call with this name. | [optional]

### Return type

[**\Swagger\Client\Model\LocationList**](../Model/LocationList.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getNearbyAddress**
> \Swagger\Client\Model\LocationList getNearbyAddress($origin_coord_lat, $origin_coord_long, $format, $jsonp_callback)

Returns the address nearest a given coordinate.



### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\LocationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$origin_coord_lat = 1.2; // double | latitude of coordinate in the WGS84 system
$origin_coord_long = 1.2; // double | longitude of coordinate in the WGS84 system
$format = "format_example"; // string | the required response format
$jsonp_callback = "jsonp_callback_example"; // string | If JSONP response format is needed, you can append an additional parameter to specify the name of a callback function, and the JSON object will be wrapped by a function call with this name.

try {
    $result = $apiInstance->getNearbyAddress($origin_coord_lat, $origin_coord_long, $format, $jsonp_callback);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LocationApi->getNearbyAddress: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **origin_coord_lat** | **double**| latitude of coordinate in the WGS84 system |
 **origin_coord_long** | **double**| longitude of coordinate in the WGS84 system |
 **format** | **string**| the required response format | [optional]
 **jsonp_callback** | **string**| If JSONP response format is needed, you can append an additional parameter to specify the name of a callback function, and the JSON object will be wrapped by a function call with this name. | [optional]

### Return type

[**\Swagger\Client\Model\LocationList**](../Model/LocationList.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getNearbyStops**
> \Swagger\Client\Model\LocationList getNearbyStops($origin_coord_lat, $origin_coord_long, $max_no, $max_dist, $format, $jsonp_callback)

Returns a list of stops around a given center coordinate.

Returns a list of stops around a given center coordinate. The returned results are ordered by their distance to the center coordinate.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\LocationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$origin_coord_lat = 1.2; // double | latitude of center coordinate in the WGS84 system
$origin_coord_long = 1.2; // double | longitude of center coordinate in the WGS84 system
$max_no = 56; // int | maximum number of returned stops
$max_dist = 56; // int | maximum distance from the center coordinate
$format = "format_example"; // string | the required response format
$jsonp_callback = "jsonp_callback_example"; // string | If JSONP response format is needed, you can append an additional parameter to specify the name of a callback function, and the JSON object will be wrapped by a function call with this name.

try {
    $result = $apiInstance->getNearbyStops($origin_coord_lat, $origin_coord_long, $max_no, $max_dist, $format, $jsonp_callback);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LocationApi->getNearbyStops: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **origin_coord_lat** | **double**| latitude of center coordinate in the WGS84 system |
 **origin_coord_long** | **double**| longitude of center coordinate in the WGS84 system |
 **max_no** | **int**| maximum number of returned stops | [optional]
 **max_dist** | **int**| maximum distance from the center coordinate | [optional]
 **format** | **string**| the required response format | [optional]
 **jsonp_callback** | **string**| If JSONP response format is needed, you can append an additional parameter to specify the name of a callback function, and the JSON object will be wrapped by a function call with this name. | [optional]

### Return type

[**\Swagger\Client\Model\LocationList**](../Model/LocationList.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

