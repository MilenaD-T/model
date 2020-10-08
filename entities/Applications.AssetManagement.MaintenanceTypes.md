---
uid: Applications.AssetManagement.MaintenanceTypes
---
# Applications.AssetManagement.MaintenanceTypes

Types of maintenances which can be scheduled and performed on the managed assets. Maintenances can be scheduled based on date and tracked parameter change. Entity: Eam_Maintenance_Types (Introduced in version 19.1.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Applications.AssetManagement.MaintenanceTypes.md#code) | string | Unique code of the maintenance type. [Required] [Filter(eq;like)] [ORD] 
| [DefaultParameterChange](Applications.AssetManagement.MaintenanceTypes.md#defaultparameterchange) | int32 (nullable) | Default positive change of the tracked parameter between two maintenances. null means, that maintenances are not scheduled based on parameter change. 
| [DefaultScheduleDays](Applications.AssetManagement.MaintenanceTypes.md#defaultscheduledays) | int32 (nullable) | Specifies the maximum number of days between two maintenances (in addition to the number of months specified in Default Schedule Months). null means that there is no default schedule in days. 
| [DefaultScheduleMonths](Applications.AssetManagement.MaintenanceTypes.md#defaultschedulemonths) | int32 (nullable) | Specifies the maximum number of months between two maintenances. null means that there is no default schedule in months. 
| [Description](Applications.AssetManagement.MaintenanceTypes.md#description) | [MultilanguageString](../data-types.md#multilanguagestring) (nullable) | Detailed description of the maintenance (multilanguage). 
| [Id](Applications.AssetManagement.MaintenanceTypes.md#id) | guid |  
| [Name](Applications.AssetManagement.MaintenanceTypes.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | Multilanguage name of the maintenance type. [Required] [Filter(eq;like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [MaintenanceTypeGroup](Applications.AssetManagement.MaintenanceTypes.md#maintenancetypegroup) | [Applications.AssetManagement.MaintenanceTypeGroups](Applications.AssetManagement.MaintenanceTypeGroups.md) | The group, to which this maintenance type belongs. [Required] [Filter(multi eq)] |
| [TrackedParameter](Applications.AssetManagement.MaintenanceTypes.md#trackedparameter) | [Applications.AssetManagement.TrackedParameters](Applications.AssetManagement.TrackedParameters.md) (nullable) | Specifies the parameter, on which the next scheduled maintenance will be based. null means that there is no default schedule, based on parameter. [Filter(multi eq)] |


## Attribute Details

### Code

> Unique code of the maintenance type. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### DefaultParameterChange

> Default positive change of the tracked parameter between two maintenances. null means, that maintenances are not scheduled based on parameter change.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DefaultScheduleDays

> Specifies the maximum number of days between two maintenances (in addition to the number of months specified in Default Schedule Months). null means that there is no default schedule in days.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DefaultScheduleMonths

> Specifies the maximum number of months between two maintenances. null means that there is no default schedule in months.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Description

> Detailed description of the maintenance (multilanguage).

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

> Multilanguage name of the maintenance type. [Required] [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  


## Reference Details

### MaintenanceTypeGroup

> The group, to which this maintenance type belongs. [Required] [Filter(multi eq)]

_Type_: **[Applications.AssetManagement.MaintenanceTypeGroups](Applications.AssetManagement.MaintenanceTypeGroups.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### TrackedParameter

> Specifies the parameter, on which the next scheduled maintenance will be based. null means that there is no default schedule, based on parameter. [Filter(multi eq)]

_Type_: **[Applications.AssetManagement.TrackedParameters](Applications.AssetManagement.TrackedParameters.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Applications.AssetManagement.MaintenanceTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.AssetManagement.MaintenanceTypes erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.AssetManagement.MaintenanceTypes erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_AssetManagement_MaintenanceTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_AssetManagement_MaintenanceTypes?$top=10>
