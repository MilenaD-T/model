---
uid: Applications.DataWarehouse.DataMeasureGroups
---
# Applications.DataWarehouse.DataMeasureGroups

Contains the groups of measures in the general data warehouse. Entity: Dw_Data_Measure_Groups (Introduced in version 18.2.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Applications.DataWarehouse.DataMeasureGroups.md#code) | string | Unique group code. [Required] [Filter(eq;like)] [ORD] 
| [Id](Applications.DataWarehouse.DataMeasureGroups.md#id) | guid |  
| [Name](Applications.DataWarehouse.DataMeasureGroups.md#name) | string | Group name (multilanguage). [Required] [Filter(eq;like)] 
| [Notes](Applications.DataWarehouse.DataMeasureGroups.md#notes) | string (nullable) | Notes for this DataMeasureGroup. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Parent](Applications.DataWarehouse.DataMeasureGroups.md#parent) | [Applications.DataWarehouse.DataMeasureGroups](Applications.DataWarehouse.DataMeasureGroups.md) (nullable) | Parent data measure group in the hierarchy. Null when this is root node. [Filter(multi eq)] |


## Attribute Details

### Code

> Unique group code. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

> Group name (multilanguage). [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Notes

> Notes for this DataMeasureGroup.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Parent

> Parent data measure group in the hierarchy. Null when this is root node. [Filter(multi eq)]

_Type_: **[Applications.DataWarehouse.DataMeasureGroups](Applications.DataWarehouse.DataMeasureGroups.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Applications.DataWarehouse.DataMeasureGroups erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.DataWarehouse.DataMeasureGroups erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.DataWarehouse.DataMeasureGroups erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_DataWarehouse_DataMeasureGroups?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_DataWarehouse_DataMeasureGroups?$top=10>
