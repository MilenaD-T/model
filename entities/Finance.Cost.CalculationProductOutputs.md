---
uid: Finance.Cost.CalculationProductOutputs
---
# Finance.Cost.CalculationProductOutputs

Represents costs allocated to product outputs. Entity: Cost_Calculation_Product_Outputs

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Cost.CalculationProductOutputs.md#id) | guid |  
| [LineNo](Finance.Cost.CalculationProductOutputs.md#lineno) | int32 | Consecutive number of the line within the calculation. [Required] 
| [ProjectId](Finance.Cost.CalculationProductOutputs.md#projectid) | guid (nullable) | The Project, which absorbed the cost. [Filter(multi eq)] 
| [Quantity](Finance.Cost.CalculationProductOutputs.md#quantity) | decimal | The quantity produced. [Required] [Default(0)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Calculation](Finance.Cost.CalculationProductOutputs.md#calculation) | [Finance.Cost.Calculations](Finance.Cost.Calculations.md) | The [Calculation](Finance.Cost.CalculationProductOutputs.md#calculation) to which this CalculationProductOutput belongs. [Required] [Filter(multi eq)] [Owner] |
| [Lot](Finance.Cost.CalculationProductOutputs.md#lot) | [Logistics.Inventory.Lots](Logistics.Inventory.Lots.md) (nullable) | The Lot, which absorbed the cost. [Filter(multi eq)] |
| [Parent](Finance.Cost.CalculationProductOutputs.md#parent) | [Finance.Cost.CalculationProductOutputs](Finance.Cost.CalculationProductOutputs.md) (nullable) | When not null specifies the parent output, whose cost is "absorbed" within the current output. [Filter(multi eq)] |
| [Product](Finance.Cost.CalculationProductOutputs.md#product) | [General.Products.Products](General.Products.Products.md) | The Product, which absorbed the cost. [Required] [Filter(multi eq)] |
| [ProfitCenter](Finance.Cost.CalculationProductOutputs.md#profitcenter) | [Finance.Accounting.ProfitCenters](Finance.Accounting.ProfitCenters.md) (nullable) | The Profit Center, which absorbed the cost. [Filter(multi eq)] |
| [SalesOrder](Finance.Cost.CalculationProductOutputs.md#salesorder) | [Crm.Sales.SalesOrders](Crm.Sales.SalesOrders.md) (nullable) | The Sales Order, which absorbed the cost. [Filter(multi eq)] |
| [Workgroup](Finance.Cost.CalculationProductOutputs.md#workgroup) | [Production.Resources.Workgroups](Production.Resources.Workgroups.md) (nullable) | The Workgroup, which absorbed the cost. [Filter(multi eq)] |
| [WorkOrder](Finance.Cost.CalculationProductOutputs.md#workorder) | [Production.ShopFloor.WorkOrders](Production.ShopFloor.WorkOrders.md) (nullable) | The Work Order, which absorbed the cost. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LineNo

> Consecutive number of the line within the calculation. [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`(obj.Calculation.ProductOutputs.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.Calculation.ProductOutputs.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`
### ProjectId

> The Project, which absorbed the cost. [Filter(multi eq)]

_Type_: **guid (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Quantity

> The quantity produced. [Required] [Default(0)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  


## Reference Details

### Calculation

> The [Calculation](Finance.Cost.CalculationProductOutputs.md#calculation) to which this CalculationProductOutput belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Finance.Cost.Calculations](Finance.Cost.Calculations.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Lot

> The Lot, which absorbed the cost. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.Lots](Logistics.Inventory.Lots.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Parent

> When not null specifies the parent output, whose cost is "absorbed" within the current output. [Filter(multi eq)]

_Type_: **[Finance.Cost.CalculationProductOutputs](Finance.Cost.CalculationProductOutputs.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Product

> The Product, which absorbed the cost. [Required] [Filter(multi eq)]

_Type_: **[General.Products.Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ProfitCenter

> The Profit Center, which absorbed the cost. [Filter(multi eq)]

_Type_: **[Finance.Accounting.ProfitCenters](Finance.Accounting.ProfitCenters.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### SalesOrder

> The Sales Order, which absorbed the cost. [Filter(multi eq)]

_Type_: **[Crm.Sales.SalesOrders](Crm.Sales.SalesOrders.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Workgroup

> The Workgroup, which absorbed the cost. [Filter(multi eq)]

_Type_: **[Production.Resources.Workgroups](Production.Resources.Workgroups.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### WorkOrder

> The Work Order, which absorbed the cost. [Filter(multi eq)]

_Type_: **[Production.ShopFloor.WorkOrders](Production.ShopFloor.WorkOrders.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Finance.Cost.CalculationProductOutputs erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Cost.CalculationProductOutputs erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Cost.CalculationProductOutputs erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Cost_CalculationProductOutputs?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Cost_CalculationProductOutputs?$top=10>
