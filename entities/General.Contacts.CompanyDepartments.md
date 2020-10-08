---
uid: General.Contacts.CompanyDepartments
---
# General.Contacts.CompanyDepartments

Hierarchical structure of the company departments. The departments and divisions are parallel and different structuring mechanisms for the companies. Entity: Cm_Company_Departments

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [DepartmentName](General.Contacts.CompanyDepartments.md#departmentname) | string | The name of the department. [Required] [Filter(like)] 
| [Id](General.Contacts.CompanyDepartments.md#id) | guid |  
| [Notes](General.Contacts.CompanyDepartments.md#notes) | string (nullable) | Notes for this CompanyDepartment. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Company](General.Contacts.CompanyDepartments.md#company) | [General.Contacts.Companies](General.Contacts.Companies.md) | The [Company](General.Contacts.CompanyDepartments.md#company) to which this CompanyDepartment belongs. [Required] [Filter(multi eq)] [Owner] |
| [Parent](General.Contacts.CompanyDepartments.md#parent) | [General.Contacts.CompanyDepartments](General.Contacts.CompanyDepartments.md) (nullable) | The parent department. null if this is root department in the company. [Filter(multi eq)] |


## Attribute Details

### DepartmentName

> The name of the department. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

> Notes for this CompanyDepartment.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Company

> The [Company](General.Contacts.CompanyDepartments.md#company) to which this CompanyDepartment belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[General.Contacts.Companies](General.Contacts.Companies.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Parent

> The parent department. null if this is root department in the company. [Filter(multi eq)]

_Type_: **[General.Contacts.CompanyDepartments](General.Contacts.CompanyDepartments.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=General.Contacts.CompanyDepartments erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Contacts.CompanyDepartments erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.Contacts.CompanyDepartments erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Contacts_CompanyDepartments?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Contacts_CompanyDepartments?$top=10>
