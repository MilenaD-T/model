---
uid: Crm.Distributors
---
# Crm.Distributors

Distributors are external for the enterprise persons or companies who obtain sales orders from end-customers in benefit of the enterprise. Entity: Crm_Distributors

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [FlatCommisionPercentage](Crm.Distributors.md#flatcommisionpercentage) | decimal | Not-zero if commision percentage should be applyied to all sales, regardless of product/discount/progressive/qunatity considerations. [Required] [Default(0)] 
| [Id](Crm.Distributors.md#id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Party](Crm.Distributors.md#party) | [General.Contacts.Parties](General.Contacts.Parties.md) | Base party Id. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### FlatCommisionPercentage

> Not-zero if commision percentage should be applyied to all sales, regardless of product/discount/progressive/qunatity considerations. [Required] [Default(0)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  


## Reference Details

### Party

> Base party Id. [Required] [Filter(multi eq)] [Owner]

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Crm.Distributors erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.Distributors erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Crm.Distributors erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Distributors?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Distributors?$top=10>
