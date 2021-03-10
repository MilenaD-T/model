# Procedure Prd_Consumption_Orders_Table_Environment_Load_Lines


## Summary

| Name | Type | Description |
| - | - | --- |
|[Line_Ord](#line_ord)|`int` |Non-unique line number within the order|
|[Work_Order_Item_Ingredient_Id](#work_order_item_ingredient_id)|`uniqueidentifier` |The Work Order Item Ingredient for which we are ordering materials.|
|[Scheduled_Date_Time](#scheduled_date_time)|`datetime` |The scheduled date, when the material is needed.|
|[Product_Id](#product_id)|`uniqueidentifier` |The requested material.|
|[Consumed_Quantity](#consumed_quantity)|`decimal(18, 3)` |Requested quantity of the material.|
|[Consumed_Quantity_Unit_Id](#consumed_quantity_unit_id)|`uniqueidentifier` |Measurement unit of the requested quantity.|
|[Store_Id](#store_id)|`uniqueidentifier` |The store, from which the material is requested.|
|[Store_Bin_Id](#store_bin_id)|`uniqueidentifier` |If not NULL, specifies that the material has to be consumed from specific store bin|
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` |If not NULL, specifies that the material has to be consumed with specific serial number|
|[Row_Version](#row_version)|`timestamp` ||
|[Consumed_Standard_Quantity_Base](#consumed_standard_quantity_base)|`decimal(0, 0)` Readonly|The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. NULL means to convert the value from Quantity using the measurement ratios.|
|[Quantity_By_Recipe](#quantity_by_recipe)|`decimal(0, 0)` ||
|[Notes](#notes)|`nvarchar` ||
|[Id](#id)|`uniqueidentifier` `PK`|Unique order lline Id|
|[Consumption_Type](#consumption_type)|`nvarchar` Allowed: `S`, `A`, Readonly||
|[Consumed_Quantity_Base](#consumed_quantity_base)|`decimal(0, 0)` Readonly||
|[Sum_Consumed_Quantity](#sum_consumed_quantity)|`decimal(0, 0)` ||
|[Consumption_Order_Id](#consumption_order_id)|`uniqueidentifier` ||
|[Lot_Id](#lot_id)|`uniqueidentifier` ||
|[Rest_Quantity](#rest_quantity)|`decimal(0, 0)` ||

## Columns

### Line_Ord

| Property | Value |
| - | - |
|Type|int|

### Work_Order_Item_Ingredient_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Scheduled_Date_Time

| Property | Value |
| - | - |
|Type|datetime|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Consumed_Quantity

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Consumed_Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Bin_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Serial_Number_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Consumed_Standard_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Quantity_By_Recipe

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Consumption_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Consumed_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Sum_Consumed_Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Consumption_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Lot_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Rest_Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

