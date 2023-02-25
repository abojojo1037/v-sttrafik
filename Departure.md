# Departure

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**fg_color** | **string** | Foregroundcolor of this line | 
**stop** | **string** | Contains the name of the stop/station | 
**booking** | **bool** | Will be true if this journey needs to be booked | [optional] 
**direction** | **string** | Direction information | 
**journey_detail_ref** | [**\Swagger\Client\Model\JourneyDetailRef**](JourneyDetailRef.md) |  | 
**track** | **string** | Track information, if available | 
**rt_track** | **string** | Realtime track information, if available | [optional] 
**sname** | **string** | Short name of the leg | 
**type** | **string** | The attribute type specifies the type of the departing journey. Valid values are VAS, LDT (Long Distance Train), REG (Regional train), BUS , BOAT, TRAM, TAXI (Taxi/Telebus) | 
**date** | [**\DateTime**](\DateTime.md) | Date in format YYYY-MM-DD | 
**bg_color** | **string** | Backgroundcolor of this line | 
**stroke** | **string** | Stroke style of this line | 
**rt_date** | [**\DateTime**](\DateTime.md) | Realtime date in format YYYY-MM-DD, if available | 
**time** | **string** | Time in format HH:MM | 
**name** | **string** | The attribute name specifies the name of the departing journey | 
**rt_time** | **string** | Realtime time in format HH:MM if available | 
**night** | **bool** | Will be true if this journey is a night journey | [optional] 
**stopid** | **string** | Contains the id of the stop/station | 
**journeyid** | **string** | Contains the id of the journey | 
**accessibility** | **string** | will only be set if the vehicle has wheelchair + ramp/lift or lowfloor according to realtime data | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


