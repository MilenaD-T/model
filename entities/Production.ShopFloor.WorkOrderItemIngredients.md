---
uid: Production.ShopFloor.WorkOrderItemIngredients
---
# Production.ShopFloor.WorkOrderItemIngredients

The materials consumed in the production order operations. Entity: Prd_Work_Order_Item_Ingredients

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [DistributeBy](Production.ShopFloor.WorkOrderItemIngredients.md#distributeby) | [DistributeBy](Production.ShopFloor.WorkOrderItemIngredients.md#distributeby) (nullable) | Distribution method in case the materials from the line are distributed amongst all work order items. Should be NOT null iif Work_Order_Item_Id is null. MC=Measurement, SP=Standard_Price. 
| [FixedScrapQuantity](Production.ShopFloor.WorkOrderItemIngredients.md#fixedscrapquantity) | [Quantity](../data-types.md#quantity) | The quantity of the material, which will be used for setup. [Unit: UsedQuantityUnit] [Required] [Default(0)] 
| [Id](Production.ShopFloor.WorkOrderItemIngredients.md#id) | guid |  
| [LineOrd](Production.ShopFloor.WorkOrderItemIngredients.md#lineord) | int32 | The order of the line within the item. [Required] [Filter(eq;like)] 
| [Notes](Production.ShopFloor.WorkOrderItemIngredients.md#notes) | string (nullable) | Notes for this WorkOrderItemIngredient. 
| [UsedQuantity](Production.ShopFloor.WorkOrderItemIngredients.md#usedquantity) | [Quantity](../data-types.md#quantity) | The quantity of the material consumed in the operation. [Unit: UsedQuantityUnit] [Required] [Default(1)] 
| [UsedQuantityBase](Production.ShopFloor.WorkOrderItemIngredients.md#usedquantitybase) | [Quantity](../data-types.md#quantity) | The equivalence of Used Quantity in the base measurement category of the material. [Unit: Material.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly] 
| [UsedStandardQuantityBase](Production.ShopFloor.WorkOrderItemIngredients.md#usedstandardquantitybase) | [Quantity](../data-types.md#quantity) | The theoretical quantity in base measurement unit according to the current measurement dimensions of the product. Used to measure the execution. null means to take the value from Used Quantity Base. [Unit: Material.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly] (Introduced in version 18.2.100.0) 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DistributeByMeasurementCategory](Production.ShopFloor.WorkOrderItemIngredients.md#distributebymeasurementcategory) | [General.MeasurementCategories](General.MeasurementCategories.md) (nullable) | Measurement category by which the materials from the line are distributed amongst all work order items in case Distribute_By = MC. Should be NOT null iif Distribute_By = MC. [Filter(multi eq)] |
| [Lot](Production.ShopFloor.WorkOrderItemIngredients.md#lot) | [Logistics.Inventory.Lots](Logistics.Inventory.Lots.md) (nullable) | Lot from which to get the material. When null, any lot can be used. [Filter(multi eq)] |
| [Material](Production.ShopFloor.WorkOrderItemIngredients.md#material) | [General.Products.Products](General.Products.Products.md) | The Id of the consumed material (Gen_Products_Table). [Required] [Filter(multi eq)] |
| [Operation](Production.ShopFloor.WorkOrderItemIngredients.md#operation) | [Production.Resources.Operations](Production.Resources.Operations.md) (nullable) | Specifies for which operation this ingredient is used. [Filter(multi eq)] |
| [PrincipalRecipeIngredient](Production.ShopFloor.WorkOrderItemIngredients.md#principalrecipeingredient) | [Production.Technologies.PrincipalRecipeIngredients](Production.Technologies.PrincipalRecipeIngredients.md) (nullable) | The principal recipe ingredient on which this record is based. [Filter(multi eq)] |
| [ProductCode](Production.ShopFloor.WorkOrderItemIngredients.md#productcode) | [General.Products.ProductCodes](General.Products.ProductCodes.md) (nullable) | Selects the product thru some of the product codes. [Filter(multi eq)] |
| [SerialNumber](Production.ShopFloor.WorkOrderItemIngredients.md#serialnumber) | [Logistics.Inventory.SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable) | If not null, specifies the serial number of the ingredient. [Filter(multi eq)] |
| [Store](Production.ShopFloor.WorkOrderItemIngredients.md#store) | [Logistics.Inventory.Stores](Logistics.Inventory.Stores.md) (nullable) | The store from which to retrieve the material. [Filter(multi eq)] |
| [StoreBin](Production.ShopFloor.WorkOrderItemIngredients.md#storebin) | [Logistics.Inventory.StoreBins](Logistics.Inventory.StoreBins.md) (nullable) | The store bin from which to take the ingredients. [Filter(multi eq)] |
| [UsedQuantityUnit](Production.ShopFloor.WorkOrderItemIngredients.md#usedquantityunit) | [General.MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of the quantity of the material consumed in the operation. [Required] [Filter(multi eq)] |
| [WorkOrder](Production.ShopFloor.WorkOrderItemIngredients.md#workorder) | [Production.ShopFloor.WorkOrders](Production.ShopFloor.WorkOrders.md) | The [WorkOrder](Production.ShopFloor.WorkOrderItemIngredients.md#workorder) to which this WorkOrderItemIngredient belongs. [Required] [Filter(multi eq)] [Owner] |
| [WorkOrderItem](Production.ShopFloor.WorkOrderItemIngredients.md#workorderitem) | [Production.ShopFloor.WorkOrderItems](Production.ShopFloor.WorkOrderItems.md) (nullable) | The work order item for which the materials in this line are used. If null means that the materials are distributed amongst all work order items in the document. [Filter(multi eq)] |


## Attribute Details

### DistributeBy

> Distribution method in case the materials from the line are distributed amongst all work order items. Should be NOT null iif Work_Order_Item_Id is null. MC=Measurement, SP=Standard_Price.

_Type_: **[DistributeBy](Production.ShopFloor.WorkOrderItemIngredients.md#distributeby) (nullable)**  
Allowed values for the [DistributeBy](Production.ShopFloor.WorkOrderItemIngredients.md#distributeby) data attribute  
_Allowed Values (Production.ShopFloor.WorkOrderItemIngredientsRepository.DistributeBy Enum Members)_  

| Value | Description |
| ---- | --- |
| StandardPrice | StandardPrice value. Stored as 'SP'. <br /> _Database Value:_ 'SP' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'StandardPrice' |
| Measurement | Measurement value. Stored as 'MC'. <br /> _Database Value:_ 'MC' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Measurement' |
| StandardCost | StandardCost value. Stored as 'SC'. <br /> _Database Value:_ 'SC' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'StandardCost' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF((obj.WorkOrderItem != null), null, obj.DistributeBy)`
### FixedScrapQuantity

> The quantity of the material, which will be used for setup. [Unit: UsedQuantityUnit] [Required] [Default(0)]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LineOrd

> The order of the line within the item. [Required] [Filter(eq;like)]

_Type_: **int32**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`(obj.WorkOrder.ItemIngredients.Select(c => c.LineOrd).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.WorkOrder.ItemIngredients.Select(c => c.LineOrd).DefaultIfEmpty(0).Max() + 10)`
### Notes

> Notes for this WorkOrderItemIngredient.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### UsedQuantity

> The quantity of the material consumed in the operation. [Unit: UsedQuantityUnit] [Required] [Default(1)]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### UsedQuantityBase

> The equivalence of Used Quantity in the base measurement category of the material. [Unit: Material.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`IIF((((obj.Material != null) AndAlso (obj.UsedQuantity != null)) AndAlso (obj.UsedQuantityUnit != null)), obj.UsedQuantity.ConvertTo(obj.Material.BaseUnit, obj.Material), obj.UsedQuantityBase)`

_Front-End Recalc Expressions:_  
`IIF((((obj.Material != null) AndAlso (obj.UsedQuantity != null)) AndAlso (obj.UsedQuantityUnit != null)), obj.UsedQuantity.ConvertTo(obj.Material.BaseUnit, obj.Material), obj.UsedQuantityBase)`
### UsedStandardQuantityBase

> The theoretical quantity in base measurement unit according to the current measurement dimensions of the product. Used to measure the execution. null means to take the value from Used Quantity Base. [Unit: Material.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly] (Introduced in version 18.2.100.0)

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`IIF((((obj.UsedQuantity != null) AndAlso (obj.UsedQuantityUnit != null)) AndAlso (obj.Material != null)), IIF(obj.Material.AllowVariableMeasurementRatios, obj.UsedQuantity.ConvertTo(obj.Material.BaseUnit, obj.Material), obj.UsedQuantityBase), obj.UsedStandardQuantityBase)`

_Front-End Recalc Expressions:_  
`IIF((((obj.UsedQuantity != null) AndAlso (obj.UsedQuantityUnit != null)) AndAlso (obj.Material != null)), obj.UsedQuantity.ConvertTo(obj.Material.BaseUnit, obj.Material), obj.UsedStandardQuantityBase)`

## Reference Details

### DistributeByMeasurementCategory

> Measurement category by which the materials from the line are distributed amongst all work order items in case Distribute_By = MC. Should be NOT null iif Distribute_By = MC. [Filter(multi eq)]

_Type_: **[General.MeasurementCategories](General.MeasurementCategories.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`IIF(((obj.DistributeBy == null) OrElse (Convert(obj.DistributeBy.Value, Int32) != 1)), null, obj.DistributeByMeasurementCategory)`
### Lot

> Lot from which to get the material. When null, any lot can be used. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.Lots](Logistics.Inventory.Lots.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Material

> The Id of the consumed material (Gen_Products_Table). [Required] [Filter(multi eq)]

_Type_: **[General.Products.Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  

_Back-End Default Expression:_  
`obj.ProductCode.Product.IfNullThen(obj.Material)`

_Front-End Recalc Expressions:_  
`obj.ProductCode.Product.IfNullThen(obj.Material)`
### Operation

> Specifies for which operation this ingredient is used. [Filter(multi eq)]

_Type_: **[Production.Resources.Operations](Production.Resources.Operations.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### PrincipalRecipeIngredient

> The principal recipe ingredient on which this record is based. [Filter(multi eq)]

_Type_: **[Production.Technologies.PrincipalRecipeIngredients](Production.Technologies.PrincipalRecipeIngredients.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ProductCode

> Selects the product thru some of the product codes. [Filter(multi eq)]

_Type_: **[General.Products.ProductCodes](General.Products.ProductCodes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`IIF((obj.ProductCode.Product != obj.Material), null, obj.ProductCode)`
### SerialNumber

> If not null, specifies the serial number of the ingredient. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Store

> The store from which to retrieve the material. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.Stores](Logistics.Inventory.Stores.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Back-End Default Expression:_  
`obj.WorkOrder.DefaultMaterialsStore`

_Front-End Recalc Expressions:_  
`obj.WorkOrder.DefaultMaterialsStore`
### StoreBin

> The store bin from which to take the ingredients. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.StoreBins](Logistics.Inventory.StoreBins.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### UsedQuantityUnit

> The measurement unit of the quantity of the material consumed in the operation. [Required] [Filter(multi eq)]

_Type_: **[General.MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  

_Back-End Default Expression:_  
`obj.ProductCode.CodingSystem.DefaultMeasurementUnit.IfNullThen(obj.Material.MeasurementUnit.IfNullThen(obj.UsedQuantityUnit))`

_Front-End Recalc Expressions:_  
`obj.ProductCode.CodingSystem.DefaultMeasurementUnit.IfNullThen(obj.Material.MeasurementUnit.IfNullThen(obj.UsedQuantityUnit))`
### WorkOrder

> The [WorkOrder](Production.ShopFloor.WorkOrderItemIngredients.md#workorder) to which this WorkOrderItemIngredient belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Production.ShopFloor.WorkOrders](Production.ShopFloor.WorkOrders.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### WorkOrderItem

> The work order item for which the materials in this line are used. If null means that the materials are distributed amongst all work order items in the document. [Filter(multi eq)]

_Type_: **[Production.ShopFloor.WorkOrderItems](Production.ShopFloor.WorkOrderItems.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`IIF((obj.WorkOrderItem != null), null, obj.WorkOrderItem)`


## Business Rules

[!list erp.entity=Production.ShopFloor.WorkOrderItemIngredients erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Production.ShopFloor.WorkOrderItemIngredients erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Production.ShopFloor.WorkOrderItemIngredients erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Production_ShopFloor_WorkOrderItemIngredients?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Production_ShopFloor_WorkOrderItemIngredients?$top=10>
