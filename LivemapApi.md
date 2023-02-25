# Swagger\Client\LivemapApi

All URIs are relative to *https://api.vasttrafik.se/bin/rest.exe/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**livemap**](LivemapApi.md#livemap) | **GET** /livemap | Returns the positions of all vehicles in a given bounding box


# **livemap**
> \Swagger\Client\Model\LiveMap livemap($minx, $maxx, $miny, $maxy, $only_realtime)

Returns the positions of all vehicles in a given bounding box

This method will return the positions of all vehicles in a given bounding box.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\LivemapApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$minx = "minx_example"; // string | Left border (longitude) of the bounding box in WGS84 * 1000000
$maxx = "maxx_example"; // string | Right border (longitude) of the bounding box in WGS84 * 1000000
$miny = "miny_example"; // string | Lower border (latitude) of the bounding box in WGS84 * 1000000
$maxy = "maxy_example"; // string | Upper border (latitude) of the bounding box in WGS84 * 1000000
$only_realtime = "only_realtime_example"; // string | Can be used to define whether all vehicles should be returned or only those  vehicles which have realtime information. If it is set to yes, only vehicles  with realtime information are returned, if it is set to no, all vehicles in the  bounding box are returned.

try {
    $result = $apiInstance->livemap($minx, $maxx, $miny, $maxy, $only_realtime);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LivemapApi->livemap: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **minx** | **string**| Left border (longitude) of the bounding box in WGS84 * 1000000 |
 **maxx** | **string**| Right border (longitude) of the bounding box in WGS84 * 1000000 |
 **miny** | **string**| Lower border (latitude) of the bounding box in WGS84 * 1000000 |
 **maxy** | **string**| Upper border (latitude) of the bounding box in WGS84 * 1000000 |
 **only_realtime** | **string**| Can be used to define whether all vehicles should be returned or only those  vehicles which have realtime information. If it is set to yes, only vehicles  with realtime information are returned, if it is set to no, all vehicles in the  bounding box are returned. |

### Return type

[**\Swagger\Client\Model\LiveMap**](../Model/LiveMap.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

