---
uid: Production.ShopFloor.OutputOrderConsumptionLines
---
# Production.ShopFloor.OutputOrderConsumptionLines

The internal production consumption of materials. Used only for control purposes - for comparison with the active consumption orders. Warehouse and accounting are still updated only by Consumption Orders. Entity: Prd_Output_Order_Consumption_Lines

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ConsumedQuantityForRun](Production.ShopFloor.OutputOrderConsumptionLines.md#consumedquantityforrun) | [Quantity](../data-types.md#quantity) | The consumed quantity of the material for the operation. [Unit: QuantityUnit] [Required] [Default(0)] 
| [ConsumedQuantityForScrap](Production.ShopFloor.OutputOrderConsumptionLines.md#consumedquantityforscrap) | [Quantity](../data-types.md#quantity) | The scrapped quantity of the material for this operation. [Unit: QuantityUnit] [Required] [Default(0)] 
| [ConsumedQuantityForSetup](Production.ShopFloor.OutputOrderConsumptionLines.md#consumedquantityforsetup) | [Quantity](../data-types.md#quantity) | The consumed quantity of the material while setting up the operation. [Unit: QuantityUnit] [Required] [Default(0)] 
| [Id](Production.ShopFloor.OutputOrderConsumptionLines.md#id) | guid |  
| [LineNo](Production.ShopFloor.OutputOrderConsumptionLines.md#lineno) | int32 | Line number, unique within the OutputOrder. Usually is increasing number like 10, 20, 30, ... when initially entering the OutputOrder (in order to allow insertions with adjustment documents). [Required] 
| [Notes](Production.ShopFloor.OutputOrderConsumptionLines.md#notes) | string (nullable) | Notes for this OutputOrderConsumptionLine. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [LineWorkOrder](Production.ShopFloor.OutputOrderConsumptionLines.md#lineworkorder) | [Production.ShopFloor.WorkOrders](Production.ShopFloor.WorkOrders.md) | Work order for the line. Initially copied from the header (if there work order is not null). [Required] [Filter(multi eq)] |
| [Material](Production.ShopFloor.OutputOrderConsumptionLines.md#material) | [General.Products.Products](General.Products.Products.md) | The consumed material. [Required] [Filter(multi eq)] |
| [OutputOrder](Production.ShopFloor.OutputOrderConsumptionLines.md#outputorder) | [Production.ShopFloor.OutputOrders](Production.ShopFloor.OutputOrders.md) | The [OutputOrder](Production.ShopFloor.OutputOrderConsumptionLines.md#outputorder) to which this OutputOrderConsumptionLine belongs. [Required] [Filter(multi eq)] [Owner] |
| [QuantityUnit](Production.ShopFloor.OutputOrderConsumptionLines.md#quantityunit) | [General.MeasurementUnits](General.MeasurementUnits.md) | The measurement unit for the consumed quantity for setup, run and scrap. [Required] [Filter(multi eq)] |
| [ScrapType](Production.ShopFloor.OutputOrderConsumptionLines.md#scraptype) | [Logistics.Inventory.ScrapTypes](Logistics.Inventory.ScrapTypes.md) (nullable) | When Consumed_Quantity_For_Scrap <> 0 denotes the reason for the scrap. [Filter(multi eq)] |
| [WorkOrderItem](Production.ShopFloor.OutputOrderConsumptionLines.md#workorderitem) | [Production.ShopFloor.WorkOrderItems](Production.ShopFloor.WorkOrderItems.md) | The work order item, for which the consumption is recorded. [Required] [Filter(multi eq)] |
| [WorkOrderItemOperation](Production.ShopFloor.OutputOrderConsumptionLines.md#workorderitemoperation) | [Production.ShopFloor.WorkOrderItemOperations](Production.ShopFloor.WorkOrderItemOperations.md) (nullable) | The operation in which the material was consumed. null = unknown. [Filter(multi eq)] |


## Attribute Details

### ConsumedQuantityForRun

> The consumed quantity of the material for the operation. [Unit: QuantityUnit] [Required] [Default(0)]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### ConsumedQuantityForScrap

> The scrapped quantity of the material for this operation. [Unit: QuantityUnit] [Required] [Default(0)]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### ConsumedQuantityForSetup

> The consumed quantity of the material while setting up the operation. [Unit: QuantityUnit] [Required] [Default(0)]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LineNo

> Line number, unique within the OutputOrder. Usually is increasing number like 10, 20, 30, ... when initially entering the OutputOrder (in order to allow insertions with adjustment documents). [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`(obj.OutputOrder.ConsumptionLines.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.OutputOrder.ConsumptionLines.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`
### Notes

> Notes for this OutputOrderConsumptionLine.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### LineWorkOrder

> Work order for the line. Initially copied from the header (if there work order is not null). [Required] [Filter(multi eq)]

_Type_: **[Production.ShopFloor.WorkOrders](Production.ShopFloor.WorkOrders.md)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`obj.OutputOrder.WorkOrder`
### Material

> The consumed material. [Required] [Filter(multi eq)]

_Type_: **[General.Products.Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### OutputOrder

> The [OutputOrder](Production.ShopFloor.OutputOrderConsumptionLines.md#outputorder) to which this OutputOrderConsumptionLine belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Production.ShopFloor.OutputOrders](Production.ShopFloor.OutputOrders.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### QuantityUnit

> The measurement unit for the consumed quantity for setup, run and scrap. [Required] [Filter(multi eq)]

_Type_: **[General.MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`obj.Material.MeasurementUnit`
### ScrapType

> When Consumed_Quantity_For_Scrap <> 0 denotes the reason for the scrap. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.ScrapTypes](Logistics.Inventory.ScrapTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### WorkOrderItem

> The work order item, for which the consumption is recorded. [Required] [Filter(multi eq)]

_Type_: **[Production.ShopFloor.WorkOrderItems](Production.ShopFloor.WorkOrderItems.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### WorkOrderItemOperation

> The operation in which the material was consumed. null = unknown. [Filter(multi eq)]

_Type_: **[Production.ShopFloor.WorkOrderItemOperations](Production.ShopFloor.WorkOrderItemOperations.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Production.ShopFloor.OutputOrderConsumptionLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Production.ShopFloor.OutputOrderConsumptionLines erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Production.ShopFloor.OutputOrderConsumptionLines erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Production_ShopFloor_OutputOrderConsumptionLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Production_ShopFloor_OutputOrderConsumptionLines?$top=10>
