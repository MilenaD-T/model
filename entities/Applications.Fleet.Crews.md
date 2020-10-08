---
uid: Applications.Fleet.Crews
---
# Applications.Fleet.Crews

Represents the crews, which can operate vehicles. Entity: Fleet_Crews

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Active](Applications.Fleet.Crews.md#active) | boolean | Is the crew active? true-active for choosing; false-otherwise. [Required] [Default(true)] [Filter(eq)] 
| [Id](Applications.Fleet.Crews.md#id) | guid |  
| [Name](Applications.Fleet.Crews.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | The name of the crew (multilanguage). [Required] [Filter(eq;like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](Applications.Fleet.Crews.md#enterprisecompany) | [General.EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company operating the crew. [Required] [Filter(multi eq)] [Owner] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Members | [Applications.Fleet.CrewMembers](Applications.Fleet.CrewMembers.md) | List of [CrewMember](Applications.Fleet.CrewMembers.md) child objects, based on the [Applications.Fleet.CrewMember.Crew](Applications.Fleet.CrewMembers.md#crew) back reference 


## Attribute Details

### Active

> Is the crew active? true-active for choosing; false-otherwise. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

> The name of the crew (multilanguage). [Required] [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  


## Reference Details

### EnterpriseCompany

> The enterprise company operating the crew. [Required] [Filter(multi eq)] [Owner]

_Type_: **[General.EnterpriseCompanies](General.EnterpriseCompanies.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Applications.Fleet.Crews erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Fleet.Crews erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.Fleet.Crews erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Fleet_Crews?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Fleet_Crews?$top=10>
