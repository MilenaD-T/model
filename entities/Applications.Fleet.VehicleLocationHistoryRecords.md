---
uid: Applications.Fleet.VehicleLocationHistoryRecords
---
# Applications.Fleet.VehicleLocationHistoryRecords

Stores information about vehicle locations. Entity: Fleet_Vehicle_Location_History_Records

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CurrentSpeedKmH](Applications.Fleet.VehicleLocationHistoryRecords.md#currentspeedkmh) | int32 (nullable) | The current speed of the vehicle in km/h. null means the speed is unknown. (Introduced in version 19.1.100.0) 
| [Id](Applications.Fleet.VehicleLocationHistoryRecords.md#id) | guid |  
| [Latitude](Applications.Fleet.VehicleLocationHistoryRecords.md#latitude) | decimal | Latitude of the vehicle at the specified time. Latitude is the vertical angle from equator to the pole of the point. Positive values denote points north of the equator. The value is in the range [-90, 90]. [Required] 
| [Longitude](Applications.Fleet.VehicleLocationHistoryRecords.md#longitude) | decimal | Longitude of the vehicle at the specified time. Longitude is angle from the prime meridian (in England) in east-west direction. Positive values denote east and negative - west. The value is in the range [-180, 180]. [Required] 
| [Time](Applications.Fleet.VehicleLocationHistoryRecords.md#time) | datetime | The time, for which the location is stored. [Required] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Vehicle](Applications.Fleet.VehicleLocationHistoryRecords.md#vehicle) | [Applications.Fleet.Vehicles](Applications.Fleet.Vehicles.md) | The vehicle, whose location is being stored. [Required] [Filter(multi eq)] |


## Attribute Details

### CurrentSpeedKmH

> The current speed of the vehicle in km/h. null means the speed is unknown. (Introduced in version 19.1.100.0)

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Latitude

> Latitude of the vehicle at the specified time. Latitude is the vertical angle from equator to the pole of the point. Positive values denote points north of the equator. The value is in the range [-90, 90]. [Required]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Longitude

> Longitude of the vehicle at the specified time. Longitude is angle from the prime meridian (in England) in east-west direction. Positive values denote east and negative - west. The value is in the range [-180, 180]. [Required]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Time

> The time, for which the location is stored. [Required]

_Type_: **datetime**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Vehicle

> The vehicle, whose location is being stored. [Required] [Filter(multi eq)]

_Type_: **[Applications.Fleet.Vehicles](Applications.Fleet.Vehicles.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Applications.Fleet.VehicleLocationHistoryRecords erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Fleet.VehicleLocationHistoryRecords erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.Fleet.VehicleLocationHistoryRecords erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Fleet_VehicleLocationHistoryRecords?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Fleet_VehicleLocationHistoryRecords?$top=10>
