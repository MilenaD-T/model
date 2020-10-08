---
uid: Wms.WarehouseOrderExecutions
---
# Wms.WarehouseOrderExecutions

Execution of a warehouse order line. Entity: Wms_Warehouse_Order_Executions (Introduced in version 20.1.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CreationTimeUtc](Wms.WarehouseOrderExecutions.md#creationtimeutc) | datetime | The exact time in UTC, when the execution was created in the system. [Required] 
| [Date](Wms.WarehouseOrderExecutions.md#date) | date | Date, when the execution occurred in the real world. [Required] 
| [ExecutedQuantity](Wms.WarehouseOrderExecutions.md#executedquantity) | decimal | Executed quantity in the measurement unit of the warehouse order line. [Required] 
| [Id](Wms.WarehouseOrderExecutions.md#id) | guid |  
| [IsFinal](Wms.WarehouseOrderExecutions.md#isfinal) | boolean | Specifies whether this execution will finalize the execution of the order line, regardless of any remaining quantities. [Required] 
| [Time](Wms.WarehouseOrderExecutions.md#time) | time | Time, when the execution occurred in the real world. [Required] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CreationUser](Wms.WarehouseOrderExecutions.md#creationuser) | [Systems.Security.Users](Systems.Security.Users.md) | The user, who created the record. [Required] [Filter(multi eq)] |
| [WarehouseOrderLine](Wms.WarehouseOrderExecutions.md#warehouseorderline) | [Logistics.Wms.WarehouseOrderLines](Logistics.Wms.WarehouseOrderLines.md) | The line for which we record execution. [Required] [Filter(multi eq)] |
| [WarehouseWorker](Wms.WarehouseOrderExecutions.md#warehouseworker) | [Logistics.Wms.WarehouseWorkers](Logistics.Wms.WarehouseWorkers.md) | The worker, which executed the line. [Required] [Filter(multi eq)] |


## Attribute Details

### CreationTimeUtc

> The exact time in UTC, when the execution was created in the system. [Required]

_Type_: **datetime**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Date

> Date, when the execution occurred in the real world. [Required]

_Type_: **date**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ExecutedQuantity

> Executed quantity in the measurement unit of the warehouse order line. [Required]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsFinal

> Specifies whether this execution will finalize the execution of the order line, regardless of any remaining quantities. [Required]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Time

> Time, when the execution occurred in the real world. [Required]

_Type_: **time**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### CreationUser

> The user, who created the record. [Required] [Filter(multi eq)]

_Type_: **[Systems.Security.Users](Systems.Security.Users.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### WarehouseOrderLine

> The line for which we record execution. [Required] [Filter(multi eq)]

_Type_: **[Logistics.Wms.WarehouseOrderLines](Logistics.Wms.WarehouseOrderLines.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### WarehouseWorker

> The worker, which executed the line. [Required] [Filter(multi eq)]

_Type_: **[Logistics.Wms.WarehouseWorkers](Logistics.Wms.WarehouseWorkers.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Wms.WarehouseOrderExecutions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Wms.WarehouseOrderExecutions erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Wms.WarehouseOrderExecutions erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Wms_WarehouseOrderExecutions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Wms_WarehouseOrderExecutions?$top=10>
