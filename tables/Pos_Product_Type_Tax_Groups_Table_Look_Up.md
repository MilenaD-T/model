# Query Pos_Product_Type_Tax_Groups_Table_Look_Up


## Summary

| Name | Type | Description |
| - | - | --- |
|[Product_Type_Tax_Group_Id](#product_type_tax_group_id)|`uniqueidentifier` `PK`||
|[Tax_Group](#tax_group)|`int` Allowed: `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`|The tax group of the product type within the specified applicable legislation.|
|[Applicable_Legislation](#applicable_legislation)|`nvarchar` Allowed: `AE`, `AU`, `BG`, `CA`, `CN`, `CZ`, `DE`, `ES`, `EU`, `FR`, `GR`, `HU`, `IN`, `IT`, `JP`, `MK`, `PL`, `PT`, `RO`, `RS`, `RU`, `TR`, `UK`, `US`, `ZA`|The legislation, for which the tax group is applicable.|

## Columns

### Product_Type_Tax_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Tax_Group

| Property | Value |
| - | - |
|Type|int|

### Applicable_Legislation

| Property | Value |
| - | - |
|Type|nvarchar|

