# CoordLocation

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**lon** | **string** | The WGS84 longitude | 
**idx** | **string** | This index can be used to reorder the StopLocations and CoordLocations in JSON format response to their correct order. IN JSON you can receive two arrays, one for Stops and one for Addresses. This attribute is only contained in reponses to the location.name request. The location with idx&#x3D;1 is the best fitting location. | 
**name** | **string** | Contains the output name of the address or point of interest | 
**type** | **string** | The attribute type specifies the type of location. Valid values are ADR (address) or POI (point of interest). This attribute can be used to do some sort of classification in the user interface. For later trip requests it does not have any meaning. | 
**lat** | **string** | The WGS84 latitude | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


