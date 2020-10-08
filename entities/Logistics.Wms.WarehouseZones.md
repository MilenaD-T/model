---
uid: Logistics.Wms.WarehouseZones
---
# Logistics.Wms.WarehouseZones

One zone within a warehouse. Each zone can have different rack structure and different temperature and other properties. Entity: Wms_Warehouse_Zones (Introduced in version 20.1.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Logistics.Wms.WarehouseZones.md#code) | string | Zone code, unique within the warehouse. [Required] [Filter(multi eq)] 
| [Id](Logistics.Wms.WarehouseZones.md#id) | guid |  
| [Name](Logistics.Wms.WarehouseZones.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | Multi-language name of the zone. [Required] [Filter(eq;like)] 
| [Notes](Logistics.Wms.WarehouseZones.md#notes) | string (nullable) | Notes for this WarehouseZone. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Parent](Logistics.Wms.WarehouseZones.md#parent) | [Logistics.Wms.WarehouseZones](Logistics.Wms.WarehouseZones.md) (nullable) | The parent Warehouse Zone of the current Warehouse Zone. [Filter(multi eq)] |
| [Warehouse](Logistics.Wms.WarehouseZones.md#warehouse) | [Logistics.Wms.Warehouses](Logistics.Wms.Warehouses.md) | The warehouse in which the zone is located. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Code

> Zone code, unique within the warehouse. [Required] [Filter(multi eq)]

_Type_: **string**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.GetNextCode(obj.Parent)`

_Front-End Recalc Expressions:_  
`obj.GetNextCode(obj.Parent)`
### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

> Multi-language name of the zone. [Required] [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Notes

> Notes for this WarehouseZone.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Parent

> The parent Warehouse Zone of the current Warehouse Zone. [Filter(multi eq)]

_Type_: **[Logistics.Wms.WarehouseZones](Logistics.Wms.WarehouseZones.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Warehouse

> The warehouse in which the zone is located. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Logistics.Wms.Warehouses](Logistics.Wms.Warehouses.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Logistics.Wms.WarehouseZones erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Wms.WarehouseZones erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Wms.WarehouseZones erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Wms_WarehouseZones?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Wms_WarehouseZones?$top=10>
