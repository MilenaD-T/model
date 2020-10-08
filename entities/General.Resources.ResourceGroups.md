---
uid: General.Resources.ResourceGroups
---
# General.Resources.ResourceGroups

Resource groups categorize the resources. Entity: Gen_Resource_Groups

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.Resources.ResourceGroups.md#id) | guid |  
| [Name](General.Resources.ResourceGroups.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | Resource group name. Unique within its parent. [Required] [Filter(eq;like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](General.Resources.ResourceGroups.md#enterprisecompany) | [General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | The enterprise company to which this resource group belongs. null means that the group is valid for all companies. Can be null only if the parent group company is also null. [Filter(multi eq)] |
| [Parent](General.Resources.ResourceGroups.md#parent) | [General.Resources.ResourceGroups](General.Resources.ResourceGroups.md) (nullable) | The parent resource group or null if this is root group. [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Resources | [General.Resources.Resources](General.Resources.Resources.md) | List of [Resource](General.Resources.Resources.md) child objects, based on the [General.Resources.Resource.ResourceGroup](General.Resources.Resources.md#resourcegroup) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

> Resource group name. Unique within its parent. [Required] [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  


## Reference Details

### EnterpriseCompany

> The enterprise company to which this resource group belongs. null means that the group is valid for all companies. Can be null only if the parent group company is also null. [Filter(multi eq)]

_Type_: **[General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Parent

> The parent resource group or null if this is root group. [Filter(multi eq)]

_Type_: **[General.Resources.ResourceGroups](General.Resources.ResourceGroups.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=General.Resources.ResourceGroups erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Resources.ResourceGroups erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.Resources.ResourceGroups erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Resources_ResourceGroups?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Resources_ResourceGroups?$top=10>
