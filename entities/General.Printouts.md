---
uid: General.Printouts
---
# General.Printouts

Contains data about binding of printout layouts to specific user-defined document types. Entity: Gen_Printouts

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [AllowPrintingOnState](General.Printouts.md#allowprintingonstate) | [AllowPrintingOnState](General.Printouts.md#allowprintingonstate) | The user can print documents only with state equal or greater than Allow_Printing_On_State. [Required] [Default(0)] 
| [ApplicationName](General.Printouts.md#applicationname) | string | The application which stored and uses the printout. [Required] 
| [BackwardCompatibility](General.Printouts.md#backwardcompatibility) | boolean | Obsolete. Not used. [Required] [Default(false)] 
| [Copies](General.Printouts.md#copies) | int32 | Number of copies that should be printed when using direct printing. [Required] [Default(1)] 
| [Definition](General.Printouts.md#definition) | string (nullable) | Obsolete. Not used. 
| [DefinitionFormat](General.Printouts.md#definitionformat) | string (nullable) | Obsolete. Not used. [Default("default")] 
| [Id](General.Printouts.md#id) | guid |  
| [IsDefault](General.Printouts.md#isdefault) | boolean | True if this is the default printout for the application form. [Required] [Default(false)] [Filter(eq)] 
| [Name](General.Printouts.md#name) | string | The name of the printout. Unique within the application form. [Required] [Filter(like)] 
| [Notes](General.Printouts.md#notes) | string (nullable) | Notes for this Printout. 
| [Ord](General.Printouts.md#ord) | int32 | Order in the list of printouts when using direct printing. [Required] [Default(0)] 
| [OrdFilterXml](General.Printouts.md#ordfilterxml) | dataaccessfilter (nullable) | The condition, required to be matched in order for the printout to be executed upon "Print All" command. 
| [OrdPriority](General.Printouts.md#ordpriority) | int32 (nullable) | Ordinal position and priority of the printout, in regard to other printouts within the current document type. Used for sorting, when executing printouts with "Print All" command. [Default(0)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DocumentType](General.Printouts.md#documenttype) | [General.DocumentTypes](General.DocumentTypes.md) | The document type to which this printout layout is bound. [Required] [Filter(multi eq)] [Owner] |
| [EnterpriseCompany](General.Printouts.md#enterprisecompany) | [General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | The Enterprise Company to which this Printout applies, or null if it is for all enterprise companies. [Filter(multi eq)] |
| [PrintoutLayout](General.Printouts.md#printoutlayout) | [General.PrintoutLayouts](General.PrintoutLayouts.md) | The printout layout, that is bound to the document type. [Required] [Filter(multi eq)] |
| [Report](General.Printouts.md#report) | [Systems.Reporting.DataSources](Systems.Reporting.DataSources.md) (nullable) | If not null points to a custom report that indicates which data will be loaded in the printout. [Filter(multi eq)] |


## Attribute Details

### AllowPrintingOnState

> The user can print documents only with state equal or greater than Allow_Printing_On_State. [Required] [Default(0)]

_Type_: **[AllowPrintingOnState](General.Printouts.md#allowprintingonstate)**  
Allowed values for the [AllowPrintingOnState](General.Printouts.md#allowprintingonstate) data attribute  
_Allowed Values (General.PrintoutsRepository.AllowPrintingOnState Enum Members)_  

| Value | Description |
| ---- | --- |
| New | New value. Stored as 0. <br /> _Database Value:_ 0 <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'New' |
| Planned | Planned value. Stored as 10. <br /> _Database Value:_ 10 <br /> _Model Value:_ 10 <br /> _Domain API Value:_ 'Planned' |
| FirmPlanned | FirmPlanned value. Stored as 20. <br /> _Database Value:_ 20 <br /> _Model Value:_ 20 <br /> _Domain API Value:_ 'FirmPlanned' |
| Released | Released value. Stored as 30. <br /> _Database Value:_ 30 <br /> _Model Value:_ 30 <br /> _Domain API Value:_ 'Released' |
| Completed | Completed value. Stored as 40. <br /> _Database Value:_ 40 <br /> _Model Value:_ 40 <br /> _Domain API Value:_ 'Completed' |
| Closed | Closed value. Stored as 50. <br /> _Database Value:_ 50 <br /> _Model Value:_ 50 <br /> _Domain API Value:_ 'Closed' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### ApplicationName

> The application which stored and uses the printout. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### BackwardCompatibility

> Obsolete. Not used. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Copies

> Number of copies that should be printed when using direct printing. [Required] [Default(1)]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **1**  

### Definition

> Obsolete. Not used.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DefinitionFormat

> Obsolete. Not used. [Default("default")]

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **default**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsDefault

> True if this is the default printout for the application form. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Name

> The name of the printout. Unique within the application form. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Notes

> Notes for this Printout.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Ord

> Order in the list of printouts when using direct printing. [Required] [Default(0)]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### OrdFilterXml

> The condition, required to be matched in order for the printout to be executed upon "Print All" command.

_Type_: **dataaccessfilter (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### OrdPriority

> Ordinal position and priority of the printout, in regard to other printouts within the current document type. Used for sorting, when executing printouts with "Print All" command. [Default(0)]

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  


## Reference Details

### DocumentType

> The document type to which this printout layout is bound. [Required] [Filter(multi eq)] [Owner]

_Type_: **[General.DocumentTypes](General.DocumentTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### EnterpriseCompany

> The Enterprise Company to which this Printout applies, or null if it is for all enterprise companies. [Filter(multi eq)]

_Type_: **[General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### PrintoutLayout

> The printout layout, that is bound to the document type. [Required] [Filter(multi eq)]

_Type_: **[General.PrintoutLayouts](General.PrintoutLayouts.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Report

> If not null points to a custom report that indicates which data will be loaded in the printout. [Filter(multi eq)]

_Type_: **[Systems.Reporting.DataSources](Systems.Reporting.DataSources.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=General.Printouts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Printouts erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.Printouts erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Printouts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Printouts?$top=10>
