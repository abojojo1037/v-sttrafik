# Destination

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**route_idx** | **string** | Route index of a stop/station. Can be used as a reference of the stop/station in a journeyDetail response | [optional] 
**value** | **string** |  | 
**cancelled** | **bool** | Will be set to true if departure/arrival at this stop is cancelled | [optional] 
**track** | **string** | Track information, if available | [optional] 
**rt_track** | **string** | Realtime track information, if available | [optional] 
**type** | **string** | The attribute type specifies the type of location. Valid values are ST (stop/station), ADR (address) or POI (point of interest) | 
**date** | [**\DateTime**](\DateTime.md) | Date in format YYYY-MM-DD | 
**notes** | [**\Swagger\Client\Model\Notes**](Notes.md) |  | [optional] 
**id** | **string** | ID of this stop | 
**rt_date** | [**\DateTime**](\DateTime.md) | Realtime date in format YYYY-MM-DD, if available | [optional] 
**time** | **string** | Time in format HH:MM | 
**directdate** | [**\DateTime**](\DateTime.md) | Date in format YYYY-MM-DD.  Based on the direct travel time | [optional] 
**name** | **string** | Contains the name of the location | 
**rt_time** | **string** | Realtime time in format HH:MM if available | [optional] 
**directtime** | **string** | Direct Time format HH:MM. Based on the direct travel time | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


