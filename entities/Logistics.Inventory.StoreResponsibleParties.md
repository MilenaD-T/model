---
uid: Logistics.Inventory.StoreResponsibleParties
---
# Logistics.Inventory.StoreResponsibleParties

Contains the list of responsible parties (usually persons) for the stores. Stores can have multiple responsible parties. Entity: Inv_Store_Responsible_Parties

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Inventory.StoreResponsibleParties.md#id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ResponsibleParty](Logistics.Inventory.StoreResponsibleParties.md#responsibleparty) | [General.Contacts.Parties](General.Contacts.Parties.md) | The responsible party (usually employee) of the store. [Required] [Filter(multi eq)] |
| [Store](Logistics.Inventory.StoreResponsibleParties.md#store) | [Logistics.Inventory.Stores](Logistics.Inventory.Stores.md) | The store for which we specify the responsible party. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  


## Reference Details

### ResponsibleParty

> The responsible party (usually employee) of the store. [Required] [Filter(multi eq)]

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Store

> The store for which we specify the responsible party. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Logistics.Inventory.Stores](Logistics.Inventory.Stores.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Logistics.Inventory.StoreResponsibleParties erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Inventory.StoreResponsibleParties erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Inventory.StoreResponsibleParties erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Inventory_StoreResponsibleParties?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Inventory_StoreResponsibleParties?$top=10>
