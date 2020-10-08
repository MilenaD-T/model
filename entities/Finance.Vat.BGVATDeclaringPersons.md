---
uid: Finance.Vat.BGVATDeclaringPersons
---
# Finance.Vat.BGVATDeclaringPersons

National data: Contains the persons, which are authorized to issue and sign VAT declarations. Entity: Nat_BG_VAT_Declaring_Persons

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [DeclarerType](Finance.Vat.BGVATDeclaringPersons.md#declarertype) | [DeclarerType](Finance.Vat.BGVATDeclaringPersons.md#declarertype) | Type of the declaring person. A=Attorney, R=Representative. [Required] [Filter(eq)] 
| [DeclaringPersonAddress](Finance.Vat.BGVATDeclaringPersons.md#declaringpersonaddress) | string | Address for correspondation of the declaring person. [Required] 
| [DeclaringPersonCity](Finance.Vat.BGVATDeclaringPersons.md#declaringpersoncity) | string | City from the address for correspondation of the declaring person. [Required] 
| [DeclaringPersonPosition](Finance.Vat.BGVATDeclaringPersons.md#declaringpersonposition) | string (nullable) | Position of the declaring person in the enterprise company. 
| [DeclaringPersonPostcode](Finance.Vat.BGVATDeclaringPersons.md#declaringpersonpostcode) | string | Postcode from the address for correspondation of the declaring person. [Required] 
| [Id](Finance.Vat.BGVATDeclaringPersons.md#id) | guid |  
| [IsDefault](Finance.Vat.BGVATDeclaringPersons.md#isdefault) | boolean | True if this is the default person, which issues VAT declarations for this Enterprise Company. [Required] [Default(true)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](Finance.Vat.BGVATDeclaringPersons.md#enterprisecompany) | [General.EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company for which the person is presenting the declaration. [Required] [Filter(multi eq)] [Owner] |
| [Person](Finance.Vat.BGVATDeclaringPersons.md#person) | [General.Contacts.Persons](General.Contacts.Persons.md) | The person that is presenting the declaration. [Required] [Filter(multi eq)] |


## Attribute Details

### DeclarerType

> Type of the declaring person. A=Attorney, R=Representative. [Required] [Filter(eq)]

_Type_: **[DeclarerType](Finance.Vat.BGVATDeclaringPersons.md#declarertype)**  
Allowed values for the [DeclarerType](Finance.Vat.BGVATDeclaringPersons.md#declarertype) data attribute  
_Allowed Values (Finance.Vat.BGVATDeclaringPersonsRepository.DeclarerType Enum Members)_  

| Value | Description |
| ---- | --- |
| Attorney | Attorney value. Stored as 'A'. <br /> _Database Value:_ 'A' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Attorney' |
| Representative | Representative value. Stored as 'R'. <br /> _Database Value:_ 'R' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Representative' |

_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### DeclaringPersonAddress

> Address for correspondation of the declaring person. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DeclaringPersonCity

> City from the address for correspondation of the declaring person. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DeclaringPersonPosition

> Position of the declaring person in the enterprise company.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DeclaringPersonPostcode

> Postcode from the address for correspondation of the declaring person. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsDefault

> True if this is the default person, which issues VAT declarations for this Enterprise Company. [Required] [Default(true)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **True**  


## Reference Details

### EnterpriseCompany

> The enterprise company for which the person is presenting the declaration. [Required] [Filter(multi eq)] [Owner]

_Type_: **[General.EnterpriseCompanies](General.EnterpriseCompanies.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Person

> The person that is presenting the declaration. [Required] [Filter(multi eq)]

_Type_: **[General.Contacts.Persons](General.Contacts.Persons.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Finance.Vat.BGVATDeclaringPersons erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Vat.BGVATDeclaringPersons erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Vat.BGVATDeclaringPersons erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Vat_BGVATDeclaringPersons?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Vat_BGVATDeclaringPersons?$top=10>
