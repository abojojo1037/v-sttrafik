# Leg

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**fg_color** | **string** | Foregroundcolor of this line | [optional] 
**booking** | **bool** | Will be true if this journey needs to be booked | [optional] 
**direction** | **string** | Direction information | [optional] 
**journey_detail_ref** | [**\Swagger\Client\Model\JourneyDetailRef**](JourneyDetailRef.md) |  | [optional] 
**cancelled** | **bool** | Will be true if this journey is cancelled | [optional] 
**kcal** | **float** | Energy use | [optional] 
**origin** | [**\Swagger\Client\Model\Origin**](Origin.md) |  | [optional] 
**sname** | **string** | Short name of the leg | [optional] 
**type** | **string** | The attribute type specifies the type of the leg. Valid values are VAS, LDT (Long Distance Train), REG (Regional train), BUS , BOAT, TRAM, TAXI (Taxi/Telebus). Furthermore it can be of type WALK, BIKE and CAR if these legs are routes on the street network | 
**geometry_ref** | [**\Swagger\Client\Model\GeometryRef**](GeometryRef.md) |  | [optional] 
**bg_color** | **string** | Backgroundcolor of this line | [optional] 
**notes** | [**\Swagger\Client\Model\Notes**](Notes.md) |  | [optional] 
**id** | **string** | ID of the journey | [optional] 
**stroke** | **string** | Stroke style of this line | [optional] 
**reachable** | **bool** | Will be true if this journey is not reachable due to delay of the feeder | [optional] 
**name** | **string** | The attribute name specifies the name of the leg | 
**night** | **bool** | Will be true if this journey is a night journey | [optional] 
**destination** | [**\Swagger\Client\Model\Destination**](Destination.md) |  | [optional] 
**percent_bike_road** | **float** | Percentage of the route that is made up of bike roads | [optional] 
**accessibility** | **string** | will only be set if the vehicle has wheelchair + ramp/lift or lowfloor according to realtime data | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


