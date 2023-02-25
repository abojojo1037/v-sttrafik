# Swagger\Client\DepartureBoardApi

All URIs are relative to *https://api.vasttrafik.se/bin/rest.exe/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getDepartureBoard**](DepartureBoardApi.md#getDepartureBoard) | **GET** /departureBoard | Return the next 20 departures (or less if not existing) from a given point in time or the next departures in a given timespan.


# **getDepartureBoard**
> \Swagger\Client\Model\DepartureBoard getDepartureBoard($id, $date, $time, $use_vas, $use_ld_train, $use_reg_train, $use_bus, $use_boat, $use_tram, $exclude_dr, $time_span, $max_departures_per_line, $need_journey_detail, $direction, $format, $jsonp_callback)

Return the next 20 departures (or less if not existing) from a given point in time or the next departures in a given timespan.

This method will return the next 20 departures (or less if not existing) from a given point in time or the next departures in a given timespan. The service can only be called for stops/stations by using according ID retrieved by the location method. The parameter is called id. The time and date are defined with the parameters date and time.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\DepartureBoardApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 789; // int | stop id
$date = new \DateTime("2013-10-20"); // \DateTime | the date
$time = "time_example"; // string | the time in format HH:MM
$use_vas = "use_vas_example"; // string | to exclude trips with Västtågen, set this parameter to 0.
$use_ld_train = "use_ld_train_example"; // string | to exclude trips with long distance trains, set this parameter to 0.
$use_reg_train = "use_reg_train_example"; // string | to exclude trips with regional trains, set this parameter to 0.
$use_bus = "use_bus_example"; // string | to exclude trips with buses, set this parameter to 0.
$use_boat = "use_boat_example"; // string | to exclude trips with boats, set this parameter to 0.
$use_tram = "use_tram_example"; // string | to exclude trips with trams, set this parameter to 0.
$exclude_dr = "exclude_dr_example"; // string | to exclude journeys which require tel. registration, set this parameter to 0.
$time_span = 56; // int | to get the next departures in a specified timespan of up to 24 hours (unit: minutes). If this parameter is not set, the result will contain the next 20 departures.
$max_departures_per_line = 56; // int | if timeSpan is set you can further reduce the number of returned journeys by adding this parameter, which will cause only the given number of journeys for every combination of line and direction.
$need_journey_detail = "need_journey_detail_example"; // string | if the reference URL for the journey detail service is not needed in the result, set this parameter to 0
$direction = 789; // int | stop id in order to get only departures of vehicles with a specified direction
$format = "format_example"; // string | the required response format
$jsonp_callback = "jsonp_callback_example"; // string | If JSONP response format is needed, you can append an additional parameter to specify the name of a callback function, and the JSON object will be wrapped by a function call with this name.

try {
    $result = $apiInstance->getDepartureBoard($id, $date, $time, $use_vas, $use_ld_train, $use_reg_train, $use_bus, $use_boat, $use_tram, $exclude_dr, $time_span, $max_departures_per_line, $need_journey_detail, $direction, $format, $jsonp_callback);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DepartureBoardApi->getDepartureBoard: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| stop id |
 **date** | **\DateTime**| the date |
 **time** | **string**| the time in format HH:MM |
 **use_vas** | **string**| to exclude trips with Västtågen, set this parameter to 0. | [optional]
 **use_ld_train** | **string**| to exclude trips with long distance trains, set this parameter to 0. | [optional]
 **use_reg_train** | **string**| to exclude trips with regional trains, set this parameter to 0. | [optional]
 **use_bus** | **string**| to exclude trips with buses, set this parameter to 0. | [optional]
 **use_boat** | **string**| to exclude trips with boats, set this parameter to 0. | [optional]
 **use_tram** | **string**| to exclude trips with trams, set this parameter to 0. | [optional]
 **exclude_dr** | **string**| to exclude journeys which require tel. registration, set this parameter to 0. | [optional]
 **time_span** | **int**| to get the next departures in a specified timespan of up to 24 hours (unit: minutes). If this parameter is not set, the result will contain the next 20 departures. | [optional]
 **max_departures_per_line** | **int**| if timeSpan is set you can further reduce the number of returned journeys by adding this parameter, which will cause only the given number of journeys for every combination of line and direction. | [optional]
 **need_journey_detail** | **string**| if the reference URL for the journey detail service is not needed in the result, set this parameter to 0 | [optional]
 **direction** | **int**| stop id in order to get only departures of vehicles with a specified direction | [optional]
 **format** | **string**| the required response format | [optional]
 **jsonp_callback** | **string**| If JSONP response format is needed, you can append an additional parameter to specify the name of a callback function, and the JSON object will be wrapped by a function call with this name. | [optional]

### Return type

[**\Swagger\Client\Model\DepartureBoard**](../Model/DepartureBoard.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

