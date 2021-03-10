# Query Inv_Current_Availability_Table_Load_Navigator_In_Measurement_Unit


## Summary

| Name | Type | Description |
| - | - | --- |
|[Store_Id](#store_id)|`uniqueidentifier` ||
|[Store_Bin_Id](#store_bin_id)|`uniqueidentifier` ||
|[Product_Id](#product_id)|`uniqueidentifier` ||
|[Product_Name](#product_name)|`nvarchar` `ML`||
|[Product_Group_Full_Path](#product_group_full_path)|`nvarchar` ||
|[PG_L1_Name](#pg_l1_name)|`nvarchar` ||
|[PG_L2_Name](#pg_l2_name)|`nvarchar` ||
|[PG_L3_Name](#pg_l3_name)|`nvarchar` ||
|[PG_L4_Name](#pg_l4_name)|`nvarchar` ||
|[PG_L5_Name](#pg_l5_name)|`nvarchar` ||
|[PG_L6_Name](#pg_l6_name)|`nvarchar` ||
|[Lot_Id](#lot_id)|`uniqueidentifier` ||
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` |Item serial number for serialized items. NULL for non-serialized items|
|[Product_Variant_Id](#product_variant_id)|`uniqueidentifier` |If specified determines which product variant of the current product in this line is used.|
|[Quantity_Base](#quantity_base)|`decimal(0, 0)` ||
|[Base_Measurement_Unit_Id](#base_measurement_unit_id)|`uniqueidentifier` `PK`||
|[Quantity](#quantity)|`decimal(0, 0)` ||
|[Planning_Safety_Stock_Quantity_Base](#planning_safety_stock_quantity_base)|`decimal(0, 0)` ||
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` ||
|[Quantity_In_Measurement_Unit](#quantity_in_measurement_unit)|`decimal(0, 0)` ||
|[In_Measurement_Unit_Id](#in_measurement_unit_id)|`uniqueidentifier` `PK`||
|[Product_Cost](#product_cost)|`decimal(0, 0)` ||
|[Product_Currency_Id](#product_currency_id)|`uniqueidentifier` `PK`||
|[Store_Cost](#store_cost)|`decimal(0, 0)` ||
|[Store_Currency_Id](#store_currency_id)|`uniqueidentifier` `PK`||
|[Base_Cost](#base_cost)|`decimal(0, 0)` ||
|[Base_Currency_Id](#base_currency_id)|`uniqueidentifier` `PK`||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||

## Columns

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Bin_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Group_Full_Path

| Property | Value |
| - | - |
|Type|nvarchar|

### PG_L1_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### PG_L2_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### PG_L3_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### PG_L4_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### PG_L5_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### PG_L6_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Lot_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Serial_Number_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Variant_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Base_Measurement_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Planning_Safety_Stock_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity_In_Measurement_Unit

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### In_Measurement_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Product_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Store_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Base_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Base_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

