---
uid: Applications.Fleet.TripSegments
---
# Applications.Fleet.TripSegments

Represents the segments which comprise the route of the trips. Entity: Fleet_Trip_Segments

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [EndingTimestamp](Applications.Fleet.TripSegments.md#endingtimestamp) | datetime (nullable) | The ending date and time of the travel on the segment. 
| [Id](Applications.Fleet.TripSegments.md#id) | guid |  
| [Mileage](Applications.Fleet.TripSegments.md#mileage) | decimal (nullable) | Mileage of the route segment. The mileage is measured in the operational units of the vehicle even when it is not miles or kilometers. null means unknown mileage. 
| [Notes](Applications.Fleet.TripSegments.md#notes) | string (nullable) | Notes for the segment. 
| [StartingTimestamp](Applications.Fleet.TripSegments.md#startingtimestamp) | datetime | The starting date and time of the travel on the segment. [Required] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EndingMapPoint](Applications.Fleet.TripSegments.md#endingmappoint) | [MapPoints](General.Geography.MapPoints.md) | The ending geographical point of the route segment. [Required] [Filter(multi eq)] |
| [StartingMapPoint](Applications.Fleet.TripSegments.md#startingmappoint) | [MapPoints](General.Geography.MapPoints.md) | The starting geographical point of the route segment. [Required] [Filter(multi eq)] |
| [Trip](Applications.Fleet.TripSegments.md#trip) | [Trips](Applications.Fleet.Trips.md) | The trip for which the segment is defined. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### EndingTimestamp

> The ending date and time of the travel on the segment.

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Mileage

> Mileage of the route segment. The mileage is measured in the operational units of the vehicle even when it is not miles or kilometers. null means unknown mileage.

_Type_: **decimal (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Notes

> Notes for the segment.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### StartingTimestamp

> The starting date and time of the travel on the segment. [Required]

_Type_: **datetime**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### EndingMapPoint

> The ending geographical point of the route segment. [Required] [Filter(multi eq)]

_Type_: **[MapPoints](General.Geography.MapPoints.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### StartingMapPoint

> The starting geographical point of the route segment. [Required] [Filter(multi eq)]

_Type_: **[MapPoints](General.Geography.MapPoints.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Trip

> The trip for which the segment is defined. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Trips](Applications.Fleet.Trips.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Applications.Fleet.TripSegments erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Fleet.TripSegments erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.Fleet.TripSegments erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Fleet_TripSegments?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Fleet_TripSegments?$top=10>

