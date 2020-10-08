---
uid: Applications.Fleet.VehicleObdTroubles
---
# Applications.Fleet.VehicleObdTroubles

Contains troubles, reported by the on-board diagnostics (OBD) of the vehicle. Entity: Fleet_Vehicle_Obd_Troubles

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Details](Applications.Fleet.VehicleObdTroubles.md#details) | string (nullable) | Additional text, human-readable details for the trouble, generated by the hardware agent. Contains at least some summary data in English and optionally, locale-specific data. 
| [DiagnosticTroubleCode](Applications.Fleet.VehicleObdTroubles.md#diagnostictroublecode) | string | Standartized OBD-II diagnostic trouble code. [Required] 
| [Id](Applications.Fleet.VehicleObdTroubles.md#id) | guid |  
| [ManufacturerTroubleCode](Applications.Fleet.VehicleObdTroubles.md#manufacturertroublecode) | string (nullable) | Non-standard manufacturer-specific trouble code. null when it is not available. 
| [OccurenceDateTime](Applications.Fleet.VehicleObdTroubles.md#occurencedatetime) | datetime | Date and time (UTC) when the trouble was detected. [Required] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Vehicle](Applications.Fleet.VehicleObdTroubles.md#vehicle) | [Applications.Fleet.Vehicles](Applications.Fleet.Vehicles.md) | The vehicle, which has experienced the trouble. [Required] [Filter(multi eq)] |


## Attribute Details

### Details

> Additional text, human-readable details for the trouble, generated by the hardware agent. Contains at least some summary data in English and optionally, locale-specific data.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DiagnosticTroubleCode

> Standartized OBD-II diagnostic trouble code. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### ManufacturerTroubleCode

> Non-standard manufacturer-specific trouble code. null when it is not available.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### OccurenceDateTime

> Date and time (UTC) when the trouble was detected. [Required]

_Type_: **datetime**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Vehicle

> The vehicle, which has experienced the trouble. [Required] [Filter(multi eq)]

_Type_: **[Applications.Fleet.Vehicles](Applications.Fleet.Vehicles.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Applications.Fleet.VehicleObdTroubles erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Fleet.VehicleObdTroubles erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.Fleet.VehicleObdTroubles erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Fleet_VehicleObdTroubles?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Fleet_VehicleObdTroubles?$top=10>
