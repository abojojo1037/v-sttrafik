# SwaggerClient-php
Provides access to Västtrafik journey planner

This PHP package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 1.10.1
- Build package: io.swagger.codegen.languages.PhpClientCodegen
For more information, please visit [api@vasttrafik.se](api@vasttrafik.se)

## Requirements

PHP 5.5 and later

## Installation & Usage
### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com//.git"
    }
  ],
  "require": {
    "/": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/SwaggerClient-php/vendor/autoload.php');
```

## Tests

To run the unit tests:

```
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\ArrivalBoardApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 789; // int | stop id
$date = new \DateTime("2013-10-20"); // \DateTime | the date
$time = "time_example"; // string | the time in format HH:MM
$direction = 789; // int | stop id in order to get only departures of vehicles with a specified direction
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
$format = "format_example"; // string | the required response format
$jsonp_callback = "jsonp_callback_example"; // string | If JSONP response format is needed, you can append an additional parameter to specify the name of a callback function, and the JSON object will be wrapped by a function call with this name.

try {
    $result = $apiInstance->getArrivalBoard($id, $date, $time, $direction, $use_vas, $use_ld_train, $use_reg_train, $use_bus, $use_boat, $use_tram, $exclude_dr, $time_span, $max_departures_per_line, $need_journey_detail, $format, $jsonp_callback);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ArrivalBoardApi->getArrivalBoard: ', $e->getMessage(), PHP_EOL;
}

?>
```

## Documentation for API Endpoints

All URIs are relative to *https://api.vasttrafik.se/bin/rest.exe/v2*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*ArrivalBoardApi* | [**getArrivalBoard**](docs/Api/ArrivalBoardApi.md#getarrivalboard) | **GET** /arrivalBoard | Return the next 20 arrivals (or less if not existing) from a given point in time or the next arrivals in a given timespan.
*DepartureBoardApi* | [**getDepartureBoard**](docs/Api/DepartureBoardApi.md#getdepartureboard) | **GET** /departureBoard | Return the next 20 departures (or less if not existing) from a given point in time or the next departures in a given timespan.
*GeometryApi* | [**getGeometry**](docs/Api/GeometryApi.md#getgeometry) | **GET** /geometry | Returns the polyline for a leg.
*JourneyDetailApi* | [**getJourneyDetail**](docs/Api/JourneyDetailApi.md#getjourneydetail) | **GET** /journeyDetail | Returns information about the complete route of a trip.
*LivemapApi* | [**livemap**](docs/Api/LivemapApi.md#livemap) | **GET** /livemap | Returns the positions of all vehicles in a given bounding box
*LocationApi* | [**getAllStops**](docs/Api/LocationApi.md#getallstops) | **GET** /location.allstops | Returns a list of all stops available in the journey planner.
*LocationApi* | [**getLocationByName**](docs/Api/LocationApi.md#getlocationbyname) | **GET** /location.name | Returns a list of possible matches in the journey planner database
*LocationApi* | [**getNearbyAddress**](docs/Api/LocationApi.md#getnearbyaddress) | **GET** /location.nearbyaddress | Returns the address nearest a given coordinate.
*LocationApi* | [**getNearbyStops**](docs/Api/LocationApi.md#getnearbystops) | **GET** /location.nearbystops | Returns a list of stops around a given center coordinate.
*SysteminfoApi* | [**getSystemInfo**](docs/Api/SysteminfoApi.md#getsysteminfo) | **GET** /systeminfo | Provides information about the journey planner and the underlying data
*TripApi* | [**getTrip**](docs/Api/TripApi.md#gettrip) | **GET** /trip | Calculates a trip from a specified origin to a specified destination.


## Documentation For Models

 - [Arrival](docs/Model/Arrival.md)
 - [ArrivalBoard](docs/Model/ArrivalBoard.md)
 - [Color](docs/Model/Color.md)
 - [CoordLocation](docs/Model/CoordLocation.md)
 - [CreationDate](docs/Model/CreationDate.md)
 - [DateBegin](docs/Model/DateBegin.md)
 - [DateEnd](docs/Model/DateEnd.md)
 - [Departure](docs/Model/Departure.md)
 - [DepartureBoard](docs/Model/DepartureBoard.md)
 - [Destination](docs/Model/Destination.md)
 - [Direction](docs/Model/Direction.md)
 - [Geometry](docs/Model/Geometry.md)
 - [GeometryRef](docs/Model/GeometryRef.md)
 - [JourneyDetail](docs/Model/JourneyDetail.md)
 - [JourneyDetailRef](docs/Model/JourneyDetailRef.md)
 - [JourneyId](docs/Model/JourneyId.md)
 - [JourneyName](docs/Model/JourneyName.md)
 - [JourneyType](docs/Model/JourneyType.md)
 - [Leg](docs/Model/Leg.md)
 - [LiveMap](docs/Model/LiveMap.md)
 - [LocationList](docs/Model/LocationList.md)
 - [Note](docs/Model/Note.md)
 - [Notes](docs/Model/Notes.md)
 - [Origin](docs/Model/Origin.md)
 - [Point](docs/Model/Point.md)
 - [Points](docs/Model/Points.md)
 - [Stop](docs/Model/Stop.md)
 - [StopLocation](docs/Model/StopLocation.md)
 - [SystemInfo](docs/Model/SystemInfo.md)
 - [TimeTableData](docs/Model/TimeTableData.md)
 - [TimeTablePeriod](docs/Model/TimeTablePeriod.md)
 - [TimetableInfo](docs/Model/TimetableInfo.md)
 - [Trip](docs/Model/Trip.md)
 - [TripList](docs/Model/TripList.md)
 - [Vehicle](docs/Model/Vehicle.md)


## Documentation For Authorization

 All endpoints do not require authorization.


## Author




