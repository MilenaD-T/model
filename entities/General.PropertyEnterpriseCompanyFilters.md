---
uid: General.PropertyEnterpriseCompanyFilters
---
# General.PropertyEnterpriseCompanyFilters

Provides a way to apply different filtering of the property allowed values for the different enterprise companies. Entity: Gen_Property_Enterprise_Company_Filters

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [FilterXml](General.PropertyEnterpriseCompanyFilters.md#filterxml) | dataaccessfilter (nullable) | When not null, specifies a filter for the allowed values of the property for the specified enterprise company. 
| [Id](General.PropertyEnterpriseCompanyFilters.md#id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](General.PropertyEnterpriseCompanyFilters.md#enterprisecompany) | [General.EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company for which the current filter is specifed. [Required] [Filter(multi eq)] |
| [Property](General.PropertyEnterpriseCompanyFilters.md#property) | [General.CustomProperties](General.CustomProperties.md) | The [CustomProperty](General.CustomProperties.md) to which this PropertyEnterpriseCompanyFilter belongs. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### FilterXml

> When not null, specifies a filter for the allowed values of the property for the specified enterprise company.

_Type_: **dataaccessfilter (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  


## Reference Details

### EnterpriseCompany

> The enterprise company for which the current filter is specifed. [Required] [Filter(multi eq)]

_Type_: **[General.EnterpriseCompanies](General.EnterpriseCompanies.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Property

> The [CustomProperty](General.CustomProperties.md) to which this PropertyEnterpriseCompanyFilter belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[General.CustomProperties](General.CustomProperties.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=General.PropertyEnterpriseCompanyFilters erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.PropertyEnterpriseCompanyFilters erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.PropertyEnterpriseCompanyFilters erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_PropertyEnterpriseCompanyFilters?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_PropertyEnterpriseCompanyFilters?$top=10>
