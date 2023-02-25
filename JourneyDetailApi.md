# Swagger\Client\JourneyDetailApi

All URIs are relative to *https://api.vasttrafik.se/bin/rest.exe/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getJourneyDetail**](JourneyDetailApi.md#getJourneyDetail) | **GET** /journeyDetail | Returns information about the complete route of a trip.


# **getJourneyDetail**
> \Swagger\Client\Model\JourneyDetail getJourneyDetail($ref)

Returns information about the complete route of a trip.

Delivers information about the complete route of a trip. This service can not be called directly but only by reference URLs in a result of a trip or departureBoard request. It contains a list of all stops/stations of this journey including all departure and arrival times (with real-time data if available) and additional information like specific attributes about facilities and other texts.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\JourneyDetailApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$ref = "ref_example"; // string | the ref query parameter, URL decoded, from a URL retrieved as a result of a trip or or departureBoard request

try {
    $result = $apiInstance->getJourneyDetail($ref);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling JourneyDetailApi->getJourneyDetail: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ref** | **string**| the ref query parameter, URL decoded, from a URL retrieved as a result of a trip or or departureBoard request |

### Return type

[**\Swagger\Client\Model\JourneyDetail**](../Model/JourneyDetail.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

