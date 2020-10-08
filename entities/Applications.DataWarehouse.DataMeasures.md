---
uid: Applications.DataWarehouse.DataMeasures
---
# Applications.DataWarehouse.DataMeasures

Contains the data measures of the General data warehouse. Entity: Dw_Data_Measures (Introduced in version 18.2.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Applications.DataWarehouse.DataMeasures.md#code) | string | Unique measure code. [Required] [Filter(eq;like)] [ORD] 
| [GreenZoneSpreadPercent](Applications.DataWarehouse.DataMeasures.md#greenzonespreadpercent) | decimal | The plus or minus percent, by which the goal can be missed, but still considered achieved. [Required] [Default(0.2)] [Filter(eq)] 
| [HorizontalTrendSpreadPercent](Applications.DataWarehouse.DataMeasures.md#horizontaltrendspreadpercent) | decimal | The change in percents, which is considered neutral. Higher positive/negative changes are considered positive/negative trends. [Required] [Default(0.01)] [Filter(eq)] 
| [Id](Applications.DataWarehouse.DataMeasures.md#id) | guid |  
| [Name](Applications.DataWarehouse.DataMeasures.md#name) | string | The name of the measure (multilanguage). [Required] [Filter(eq;like)] 
| [Notes](Applications.DataWarehouse.DataMeasures.md#notes) | string (nullable) | Notes for this DataMeasure. 
| [Period](Applications.DataWarehouse.DataMeasures.md#period) | [Period](Applications.DataWarehouse.DataMeasures.md#period) | The period for which the data is collected. D=Day, M=Month, Q=Quarter, Y=Year. [Required] [Default("Q")] [Filter(eq)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DataMeasureGroup](Applications.DataWarehouse.DataMeasures.md#datameasuregroup) | [Applications.DataWarehouse.DataMeasureGroups](Applications.DataWarehouse.DataMeasureGroups.md) | The group to which this measure belongs. [Required] [Filter(multi eq)] |


## Attribute Details

### Code

> Unique measure code. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### GreenZoneSpreadPercent

> The plus or minus percent, by which the goal can be missed, but still considered achieved. [Required] [Default(0.2)] [Filter(eq)]

_Type_: **decimal**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **0.2**  

### HorizontalTrendSpreadPercent

> The change in percents, which is considered neutral. Higher positive/negative changes are considered positive/negative trends. [Required] [Default(0.01)] [Filter(eq)]

_Type_: **decimal**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **0.01**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

> The name of the measure (multilanguage). [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Notes

> Notes for this DataMeasure.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Period

> The period for which the data is collected. D=Day, M=Month, Q=Quarter, Y=Year. [Required] [Default("Q")] [Filter(eq)]

_Type_: **[Period](Applications.DataWarehouse.DataMeasures.md#period)**  
Allowed values for the [Period](Applications.DataWarehouse.DataMeasures.md#period) data attribute  
_Allowed Values (Applications.DataWarehouse.DataMeasuresRepository.Period Enum Members)_  

| Value | Description |
| ---- | --- |
| Day | Day value. Stored as 'D'. <br /> _Database Value:_ 'D' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Day' |
| Month | Month value. Stored as 'M'. <br /> _Database Value:_ 'M' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Month' |
| Quarter | Quarter value. Stored as 'Q'. <br /> _Database Value:_ 'Q' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Quarter' |
| Year | Year value. Stored as 'Y'. <br /> _Database Value:_ 'Y' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'Year' |

_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **Quarter**  


## Reference Details

### DataMeasureGroup

> The group to which this measure belongs. [Required] [Filter(multi eq)]

_Type_: **[Applications.DataWarehouse.DataMeasureGroups](Applications.DataWarehouse.DataMeasureGroups.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Applications.DataWarehouse.DataMeasures erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.DataWarehouse.DataMeasures erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.DataWarehouse.DataMeasures erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_DataWarehouse_DataMeasures?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_DataWarehouse_DataMeasures?$top=10>
