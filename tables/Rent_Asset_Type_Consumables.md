# Table Rent_Asset_Type_Consumables

Consumables are products, which are usually sold accompanying an asset rental. Entity: Rent_Asset_Type_Consumables

## Owner Tables Hierarchy

* [Rent_Asset_Types](Rent_Asset_Types.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Asset_Type_Consumable_Id](#asset_type_consumable_id)|`uniqueidentifier` `PK`||
|[Rental_Asset_Type_Id](#rental_asset_type_id)|`uniqueidentifier` |The rental asset type for which the consumable would be offered.|
|[Product_Id](#product_id)|`uniqueidentifier` |The consumable which is offered accompanying the asset rental.|
|[Consumable_Quantity](#consumable_quantity)|`decimal(12, 3)` |Specifies what quantity of the consumable should be offered for each rented asset.|
|[Consumable_Quantity_Unit_Id](#consumable_quantity_unit_id)|`uniqueidentifier` |The measurement unit of Consumable Quantity.|
|[Store_Id](#store_id)|`uniqueidentifier` |The store which contains the consumable.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Asset_Type_Consumable_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Rental_Asset_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Consumable_Quantity

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Consumable_Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

