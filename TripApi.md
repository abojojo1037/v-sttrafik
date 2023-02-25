# Swagger\Client\TripApi

All URIs are relative to *https://api.vasttrafik.se/bin/rest.exe/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getTrip**](TripApi.md#getTrip) | **GET** /trip | Calculates a trip from a specified origin to a specified destination.


# **getTrip**
> \Swagger\Client\Model\TripList getTrip($origin_id, $origin_coord_lat, $origin_coord_long, $origin_coord_name, $dest_id, $dest_coord_lat, $dest_coord_long, $dest_coord_name, $via_id, $date, $time, $search_for_arrival, $use_vas, $use_ld_train, $use_reg_train, $use_bus, $use_medical, $origin_medical_con, $dest_medical_con, $wheel_chair_space, $stroller_space, $low_floor, $ramp_or_lift, $use_boat, $use_tram, $use_pt, $exclude_dr, $max_walk_dist, $walk_speed, $origin_walk, $dest_walk, $only_walk, $origin_bike, $max_bike_dist, $bike_criterion, $bike_profile, $only_bike, $origin_car, $origin_car_with_parking, $max_car_dist, $only_car, $max_changes, $additional_change_time, $disregard_default_change_margin, $need_journey_detail, $need_geo, $need_itinerary, $num_trips, $format, $jsonp_callback)

Calculates a trip from a specified origin to a specified destination.

Calculates a trip from a specified origin to a specified destination. These might be stop/station IDs or coordinates based on addresses and points of interest validated by the location service or coordinates freely defined by the client. Parameters specifying both origin and destination are mandatory in calls to the trip service. When specifying a stop as origin, the parameter originId is used, while originCoordLat, originCoordLong, and originCoordName are used to specify a (named) coordinate. For the destination, the corresponding parameters are named either destId or destCoordLat, destCoordLong and destCoordName. It is also possible to define a via-stop/station. This forces the journey planner to search for trips which pass the defined station. The parameter is called viaId. When searching for a trip that goes via a coordinate, rather than a stop, two separate trip requests need to be combined into one.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\TripApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$origin_id = 789; // int | origin stop id
$origin_coord_lat = 1.2; // double | origin latitude of center coordinate in the WGS84 system
$origin_coord_long = 1.2; // double | origin longitude of center coordinate in the WGS84 system
$origin_coord_name = "origin_coord_name_example"; // string | name of the address at the specified origin coordinate
$dest_id = 789; // int | destination stop id
$dest_coord_lat = 1.2; // double | destination latitude of center coordinate in the WGS84 system
$dest_coord_long = 1.2; // double | destination longitude of center coordinate in the WGS84 system
$dest_coord_name = "dest_coord_name_example"; // string | name of the address at the specified destination coordinate
$via_id = 789; // int | via stop/station id
$date = new \DateTime("2013-10-20"); // \DateTime | date of the trip
$time = "time_example"; // string | time of the trip in format HH:MM
$search_for_arrival = "search_for_arrival_example"; // string | to specify that the given time and date is not the departure time but the latest time to arrive at the destination, set this parameter to the value 1.
$use_vas = "use_vas_example"; // string | to exclude trips with Västtågen, set this parameter to 0.
$use_ld_train = "use_ld_train_example"; // string | to exclude trips with long distance trains, set this parameter to 0.
$use_reg_train = "use_reg_train_example"; // string | to exclude trips with regional trains, set this parameter to 0.
$use_bus = "use_bus_example"; // string | to exclude trips with buses, set this parameter to 0.
$use_medical = "use_medical_example"; // string | to include medical transport lines trips with buses, set this parameter to 1.
$origin_medical_con = "origin_medical_con_example"; // string | to search for medical transport connections from the origin, set this parameter to 1.
$dest_medical_con = "dest_medical_con_example"; // string | to search for medical transport connections from the destination, set this parameter to 1.
$wheel_chair_space = "wheel_chair_space_example"; // string | to search for trips where at least one wheelchair space is present in the vehicle, set this parameter to 1.
$stroller_space = "stroller_space_example"; // string | to search for trips with space for stroller, baby carriage or rollator in the vehicle, set this parameter to 1.
$low_floor = "low_floor_example"; // string | to search for trips where the vehicle is equipped with a low floor section, but not necessarily a ramp or lift, set this parameter to 1.
$ramp_or_lift = "ramp_or_lift_example"; // string | to search for trips where the vehicle is equipped with ramp or lift that allows fully barrier-free boarding and alighting, set this parameter to 1.
$use_boat = "use_boat_example"; // string | to exclude trips with boats, set this parameter to 0.
$use_tram = "use_tram_example"; // string | to exclude trips with trams, set this parameter to 0.
$use_pt = "use_pt_example"; // string | to exclude trips with public transportation, set this parameter to 0.
$exclude_dr = "exclude_dr_example"; // string | to exclude journeys which require tel. registration, set this parameter to 1.
$max_walk_dist = 56; // int | maximum walking distance from/to the coordinate in meters
$walk_speed = "walk_speed_example"; // string | walking speed given in percent of normal speed
$origin_walk = "origin_walk_example"; // string | to exclude trips with walks from/to coordinates, set this to 0
$dest_walk = "dest_walk_example"; // string | to exclude trips with walks from/to coordinates, set this to 0
$only_walk = "only_walk_example"; // string | to search for walk-only trips, set this to 1
$origin_bike = "origin_bike_example"; // string | to search for trips with a bike ride from the origin to a nearby stop, where the journey continues using public transport, set this to 1.
$max_bike_dist = 56; // int | maximum biking distance from/to the coordinate in meters
$bike_criterion = "bike_criterion_example"; // string | optimize for either the fastest route or a route that is made up of a larger percentage of bike road, where 'F' is used to indicate tha fastest route with mimimized travel time, and 'D' is used to indicate dedicated bike roads to maximize use of bike roads.
$bike_profile = "bike_profile_example"; // string | determines the altitude profile of the route, based on a setting for how fast the user can bike when it is steep, where 'E' is used to indicate easy with minimized steepnes, 'N' is used to indicate normal, and 'P' is used to indicate powerful to allow more steepness.
$only_bike = "only_bike_example"; // string | to search for bike-only trips, set this to 1
$origin_car = "origin_car_example"; // string | to search for trips where customer travels by car from the origin and is dropped off at a stop to continue the trip using public transport, set this to 1.
$origin_car_with_parking = "origin_car_with_parking_example"; // string | to search for trips where the customer travels by car from the origin, parks at a commuter parking and walks to a nearby stop to continue the trip using public transport, set this to 1.
$max_car_dist = 56; // int | maximum car distance from/to the coordinate in meters
$only_car = "only_car_example"; // string | to search for car-only trips, set this to 1
$max_changes = 56; // int | maximum number of changes in the trip
$additional_change_time = 56; // int | to prolong the minimal change times in minutes between the public transport legs of the returned journeys
$disregard_default_change_margin = "disregard_default_change_margin_example"; // string | to ignore the default change margin, set this to 1
$need_journey_detail = "need_journey_detail_example"; // string | if the reference URL for the journey detail service is not needed in the re, set this to 0
$need_geo = "need_geo_example"; // string | if a reference link for each leg of the resulting trips, which can be used to request the geometry, is needed, set this to 1
$need_itinerary = "need_itinerary_example"; // string | if a reference link for each leg of the resulting trips, which can be used to request the itinerary, is needed, set this to 1
$num_trips = 56; // int | the number of trips in the returned result
$format = "format_example"; // string | the required response format
$jsonp_callback = "jsonp_callback_example"; // string | If JSONP response format is needed, you can append an additional parameter to specify the name of a callback function, and the JSON object will be wrapped by a function call with this name.

try {
    $result = $apiInstance->getTrip($origin_id, $origin_coord_lat, $origin_coord_long, $origin_coord_name, $dest_id, $dest_coord_lat, $dest_coord_long, $dest_coord_name, $via_id, $date, $time, $search_for_arrival, $use_vas, $use_ld_train, $use_reg_train, $use_bus, $use_medical, $origin_medical_con, $dest_medical_con, $wheel_chair_space, $stroller_space, $low_floor, $ramp_or_lift, $use_boat, $use_tram, $use_pt, $exclude_dr, $max_walk_dist, $walk_speed, $origin_walk, $dest_walk, $only_walk, $origin_bike, $max_bike_dist, $bike_criterion, $bike_profile, $only_bike, $origin_car, $origin_car_with_parking, $max_car_dist, $only_car, $max_changes, $additional_change_time, $disregard_default_change_margin, $need_journey_detail, $need_geo, $need_itinerary, $num_trips, $format, $jsonp_callback);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TripApi->getTrip: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **origin_id** | **int**| origin stop id | [optional]
 **origin_coord_lat** | **double**| origin latitude of center coordinate in the WGS84 system | [optional]
 **origin_coord_long** | **double**| origin longitude of center coordinate in the WGS84 system | [optional]
 **origin_coord_name** | **string**| name of the address at the specified origin coordinate | [optional]
 **dest_id** | **int**| destination stop id | [optional]
 **dest_coord_lat** | **double**| destination latitude of center coordinate in the WGS84 system | [optional]
 **dest_coord_long** | **double**| destination longitude of center coordinate in the WGS84 system | [optional]
 **dest_coord_name** | **string**| name of the address at the specified destination coordinate | [optional]
 **via_id** | **int**| via stop/station id | [optional]
 **date** | **\DateTime**| date of the trip | [optional]
 **time** | **string**| time of the trip in format HH:MM | [optional]
 **search_for_arrival** | **string**| to specify that the given time and date is not the departure time but the latest time to arrive at the destination, set this parameter to the value 1. | [optional]
 **use_vas** | **string**| to exclude trips with Västtågen, set this parameter to 0. | [optional]
 **use_ld_train** | **string**| to exclude trips with long distance trains, set this parameter to 0. | [optional]
 **use_reg_train** | **string**| to exclude trips with regional trains, set this parameter to 0. | [optional]
 **use_bus** | **string**| to exclude trips with buses, set this parameter to 0. | [optional]
 **use_medical** | **string**| to include medical transport lines trips with buses, set this parameter to 1. | [optional]
 **origin_medical_con** | **string**| to search for medical transport connections from the origin, set this parameter to 1. | [optional]
 **dest_medical_con** | **string**| to search for medical transport connections from the destination, set this parameter to 1. | [optional]
 **wheel_chair_space** | **string**| to search for trips where at least one wheelchair space is present in the vehicle, set this parameter to 1. | [optional]
 **stroller_space** | **string**| to search for trips with space for stroller, baby carriage or rollator in the vehicle, set this parameter to 1. | [optional]
 **low_floor** | **string**| to search for trips where the vehicle is equipped with a low floor section, but not necessarily a ramp or lift, set this parameter to 1. | [optional]
 **ramp_or_lift** | **string**| to search for trips where the vehicle is equipped with ramp or lift that allows fully barrier-free boarding and alighting, set this parameter to 1. | [optional]
 **use_boat** | **string**| to exclude trips with boats, set this parameter to 0. | [optional]
 **use_tram** | **string**| to exclude trips with trams, set this parameter to 0. | [optional]
 **use_pt** | **string**| to exclude trips with public transportation, set this parameter to 0. | [optional]
 **exclude_dr** | **string**| to exclude journeys which require tel. registration, set this parameter to 1. | [optional]
 **max_walk_dist** | **int**| maximum walking distance from/to the coordinate in meters | [optional]
 **walk_speed** | **string**| walking speed given in percent of normal speed | [optional]
 **origin_walk** | **string**| to exclude trips with walks from/to coordinates, set this to 0 | [optional]
 **dest_walk** | **string**| to exclude trips with walks from/to coordinates, set this to 0 | [optional]
 **only_walk** | **string**| to search for walk-only trips, set this to 1 | [optional]
 **origin_bike** | **string**| to search for trips with a bike ride from the origin to a nearby stop, where the journey continues using public transport, set this to 1. | [optional]
 **max_bike_dist** | **int**| maximum biking distance from/to the coordinate in meters | [optional]
 **bike_criterion** | **string**| optimize for either the fastest route or a route that is made up of a larger percentage of bike road, where &#39;F&#39; is used to indicate tha fastest route with mimimized travel time, and &#39;D&#39; is used to indicate dedicated bike roads to maximize use of bike roads. | [optional]
 **bike_profile** | **string**| determines the altitude profile of the route, based on a setting for how fast the user can bike when it is steep, where &#39;E&#39; is used to indicate easy with minimized steepnes, &#39;N&#39; is used to indicate normal, and &#39;P&#39; is used to indicate powerful to allow more steepness. | [optional]
 **only_bike** | **string**| to search for bike-only trips, set this to 1 | [optional]
 **origin_car** | **string**| to search for trips where customer travels by car from the origin and is dropped off at a stop to continue the trip using public transport, set this to 1. | [optional]
 **origin_car_with_parking** | **string**| to search for trips where the customer travels by car from the origin, parks at a commuter parking and walks to a nearby stop to continue the trip using public transport, set this to 1. | [optional]
 **max_car_dist** | **int**| maximum car distance from/to the coordinate in meters | [optional]
 **only_car** | **string**| to search for car-only trips, set this to 1 | [optional]
 **max_changes** | **int**| maximum number of changes in the trip | [optional]
 **additional_change_time** | **int**| to prolong the minimal change times in minutes between the public transport legs of the returned journeys | [optional]
 **disregard_default_change_margin** | **string**| to ignore the default change margin, set this to 1 | [optional]
 **need_journey_detail** | **string**| if the reference URL for the journey detail service is not needed in the re, set this to 0 | [optional]
 **need_geo** | **string**| if a reference link for each leg of the resulting trips, which can be used to request the geometry, is needed, set this to 1 | [optional]
 **need_itinerary** | **string**| if a reference link for each leg of the resulting trips, which can be used to request the itinerary, is needed, set this to 1 | [optional]
 **num_trips** | **int**| the number of trips in the returned result | [optional]
 **format** | **string**| the required response format | [optional]
 **jsonp_callback** | **string**| If JSONP response format is needed, you can append an additional parameter to specify the name of a callback function, and the JSON object will be wrapped by a function call with this name. | [optional]

### Return type

[**\Swagger\Client\Model\TripList**](../Model/TripList.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/xml, application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

