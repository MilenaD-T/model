---
uid: Applications.Fleet.VehicleAlerts
---
# Applications.Fleet.VehicleAlerts

Contains alerts, specific to one vehicle. Alerts are created based on many sources and stay active, until excplicitly hidden. Entity: Fleet_Vehicle_Alerts

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [AlertType](Applications.Fleet.VehicleAlerts.md#alerttype) | string | The type of the alert. The type is specfic to the Source. [Required] 
| [Description](Applications.Fleet.VehicleAlerts.md#description) | string | Description of the alert (Multilanguage). [Required] 
| [Id](Applications.Fleet.VehicleAlerts.md#id) | guid |  
| [IsHidden](Applications.Fleet.VehicleAlerts.md#ishidden) | boolean | Specifies, whether the alert is hidden (e.g. managed by the responsible person). [Required] [Default(false)] 
| [Source](Applications.Fleet.VehicleAlerts.md#source) | string | The source of the alert. G=GPS, O=OBD, M=Maintenance. [Required] 
| [Time](Applications.Fleet.VehicleAlerts.md#time) | datetime | The time of the alert. [Required] [ORD] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Vehicle](Applications.Fleet.VehicleAlerts.md#vehicle) | [Applications.Fleet.Vehicles](Applications.Fleet.Vehicles.md) | The vehicle, for which is the alert. [Required] [Filter(multi eq)] |


## Attribute Details

### AlertType

> The type of the alert. The type is specfic to the Source. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Description

> Description of the alert (Multilanguage). [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsHidden

> Specifies, whether the alert is hidden (e.g. managed by the responsible person). [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Source

> The source of the alert. G=GPS, O=OBD, M=Maintenance. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Time

> The time of the alert. [Required] [ORD]

_Type_: **datetime**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **True**  


## Reference Details

### Vehicle

> The vehicle, for which is the alert. [Required] [Filter(multi eq)]

_Type_: **[Applications.Fleet.Vehicles](Applications.Fleet.Vehicles.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Applications.Fleet.VehicleAlerts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Fleet.VehicleAlerts erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.Fleet.VehicleAlerts erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Fleet_VehicleAlerts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Fleet_VehicleAlerts?$top=10>
