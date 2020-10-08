---
uid: Logistics.Inventory.CostCorrectionsOptions
---
# Logistics.Inventory.CostCorrectionsOptions

Options per document type for the cost corrections. Entity: Inv_Cost_Corrections_Options

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Inventory.CostCorrectionsOptions.md#id) | guid |  
| [ResetTransactionsStateOnReleasing](Logistics.Inventory.CostCorrectionsOptions.md#resettransactionsstateonreleasing) | boolean | When true, the stock transactions state are re-set when the cost correction is released. The idea is to notify these documents, so that they have chance to re-generate their sub-documents. [Required] [Default(false)] [Filter(eq)] 
| [ScheduleDocumentEvents](Logistics.Inventory.CostCorrectionsOptions.md#scheduledocumentevents) | boolean | Indicates wheather the document events caused by the cost correction should be scheduled for later procession. [Required] [Default(false)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DocumentType](Logistics.Inventory.CostCorrectionsOptions.md#documenttype) | [General.DocumentTypes](General.DocumentTypes.md) | The document type for which we specify the options. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### ResetTransactionsStateOnReleasing

> When true, the stock transactions state are re-set when the cost correction is released. The idea is to notify these documents, so that they have chance to re-generate their sub-documents. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### ScheduleDocumentEvents

> Indicates wheather the document events caused by the cost correction should be scheduled for later procession. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  


## Reference Details

### DocumentType

> The document type for which we specify the options. [Required] [Filter(multi eq)]

_Type_: **[General.DocumentTypes](General.DocumentTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Logistics.Inventory.CostCorrectionsOptions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Inventory.CostCorrectionsOptions erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Inventory.CostCorrectionsOptions erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Inventory_CostCorrectionsOptions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Inventory_CostCorrectionsOptions?$top=10>
