# Swagger\Client\GeometryApi

All URIs are relative to *https://api.vasttrafik.se/bin/rest.exe/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getGeometry**](GeometryApi.md#getGeometry) | **GET** /geometry | Returns the polyline for a leg.


# **getGeometry**
> \Swagger\Client\Model\Geometry getGeometry($ref)

Returns the polyline for a leg.

Returns the polyline for a leg. This service can not be called directly but only by reference URLs in a result of a trip or JourneyDetail request. The result contains a list of WGS84 coordinates which can be used to display the polyline on a map.If the parameter needItinerary=1 is passed in the URL of the trip request that contained the reference to the Geometry service, the geometry reference link will also contain an itinerary for walk, bike and car legs, that can be used to generate turn-by-turn instructions.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\GeometryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$ref = "ref_example"; // string | the ref query parameter, URL decoded, from a URL retrieved as a result of a trip or JourneyDetail request

try {
    $result = $apiInstance->getGeometry($ref);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GeometryApi->getGeometry: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ref** | **string**| the ref query parameter, URL decoded, from a URL retrieved as a result of a trip or JourneyDetail request |

### Return type

[**\Swagger\Client\Model\Geometry**](../Model/Geometry.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

