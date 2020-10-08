---
uid: General.Resources.ResourceAvailability
---
# General.Resources.ResourceAvailability

Contains the resources availability for the different periods. Each period is a separate record. The availability of a resource for any given date is determined by the sum of all availability periods that include it. Entity: Gen_Resource_Availability

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [AvailableResources](General.Resources.ResourceAvailability.md#availableresources) | decimal | The quantity of the resource, available for the specified period. For non-discrete resources, this number can contain fractions. When several availability periods for a resource overlap, the total availability is the sum of all. [Required] [Default(1)] 
| [FromDate](General.Resources.ResourceAvailability.md#fromdate) | date | The date from which availability starts. [Required] 
| [Id](General.Resources.ResourceAvailability.md#id) | guid |  
| [ToDate](General.Resources.ResourceAvailability.md#todate) | date (nullable) | The date to which the availability continues. When null, the availability continues infinitely. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Resource](General.Resources.ResourceAvailability.md#resource) | [General.Resources.Resources](General.Resources.Resources.md) | The resource, for which we provide availability. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### AvailableResources

> The quantity of the resource, available for the specified period. For non-discrete resources, this number can contain fractions. When several availability periods for a resource overlap, the total availability is the sum of all. [Required] [Default(1)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **1**  

### FromDate

> The date from which availability starts. [Required]

_Type_: **date**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### ToDate

> The date to which the availability continues. When null, the availability continues infinitely.

_Type_: **date (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Resource

> The resource, for which we provide availability. [Required] [Filter(multi eq)] [Owner]

_Type_: **[General.Resources.Resources](General.Resources.Resources.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=General.Resources.ResourceAvailability erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Resources.ResourceAvailability erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.Resources.ResourceAvailability erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Resources_ResourceAvailability?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Resources_ResourceAvailability?$top=10>
