---
uid: Crm.Sales.SalesOrderPromotionalPackages
---
# Crm.Sales.SalesOrderPromotionalPackages

The promotional packages, included in a sales order. Entity: Crm_Sales_Order_Promotional_Packages

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.Sales.SalesOrderPromotionalPackages.md#id) | guid |  
| [LineNumber](Crm.Sales.SalesOrderPromotionalPackages.md#linenumber) | int32 | Consecutive line number of the package, unique within the document. [Required] [Filter(eq)] 
| [NumberOfPackages](Crm.Sales.SalesOrderPromotionalPackages.md#numberofpackages) | int32 | Number of packages sold. [Required] [Default(0)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [PromotionalPackage](Crm.Sales.SalesOrderPromotionalPackages.md#promotionalpackage) | [Crm.PromotionalPackages](Crm.PromotionalPackages.md) | The type of promotional package sold. [Required] [Filter(multi eq)] |
| [SalesOrder](Crm.Sales.SalesOrderPromotionalPackages.md#salesorder) | [Crm.Sales.SalesOrders](Crm.Sales.SalesOrders.md) | The [SalesOrder](Crm.Sales.SalesOrderPromotionalPackages.md#salesorder) to which this SalesOrderPromotionalPackage belongs. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LineNumber

> Consecutive line number of the package, unique within the document. [Required] [Filter(eq)]

_Type_: **int32**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`(obj.SalesOrder.PromotionalPackages.Select(c => c.LineNumber).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.SalesOrder.PromotionalPackages.Select(c => c.LineNumber).DefaultIfEmpty(0).Max() + 10)`
### NumberOfPackages

> Number of packages sold. [Required] [Default(0)]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  


## Reference Details

### PromotionalPackage

> The type of promotional package sold. [Required] [Filter(multi eq)]

_Type_: **[Crm.PromotionalPackages](Crm.PromotionalPackages.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### SalesOrder

> The [SalesOrder](Crm.Sales.SalesOrderPromotionalPackages.md#salesorder) to which this SalesOrderPromotionalPackage belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Crm.Sales.SalesOrders](Crm.Sales.SalesOrders.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Crm.Sales.SalesOrderPromotionalPackages erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.Sales.SalesOrderPromotionalPackages erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Crm.Sales.SalesOrderPromotionalPackages erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Sales_SalesOrderPromotionalPackages?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Sales_SalesOrderPromotionalPackages?$top=10>
