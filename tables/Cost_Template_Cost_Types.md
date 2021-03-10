# Table Cost_Template_Cost_Types

Contains the cost types and their hierachy positions within a cost calculation. Entity: Cost_Template_Cost_Types

## Owner Tables Hierarchy

* [Cost_Templates](Cost_Templates.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Cost_Template_Cost_Type_Id](#cost_template_cost_type_id)|`uniqueidentifier` `PK`||
|[Cost_Template_Id](#cost_template_id)|`uniqueidentifier` ||
|[Cost_Type_Id](#cost_type_id)|`uniqueidentifier` |The Cost Type for which the hierarchy is specified.|
|[Hierarchy_Level](#hierarchy_level)|`int` |The level in the hierarchy on which this cost is incurred (0..9)|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Cost_Template_Cost_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Cost_Template_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Cost_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Hierarchy_Level

| Property | Value |
| - | - |
|Type|int|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

