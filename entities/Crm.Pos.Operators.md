---
uid: Crm.Pos.Operators
---
# Crm.Pos.Operators

Represents one operator (person) in one POS location. Entity: Pos_Operators (Introduced in version 19.1.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.Pos.Operators.md#id) | guid |  
| [IsActive](Crm.Pos.Operators.md#isactive) | boolean | Indicates whether this operator is active and can be chosen for new records. [Required] [Default(true)] [Filter(multi eq)] 
| [PosOperatorCode](Crm.Pos.Operators.md#posoperatorcode) | string | Operator code. Unique within the Pos Location. [Required] [Filter(multi eq;like)] [ORD] 
| [StartingDate](Crm.Pos.Operators.md#startingdate) | date | The first date, when the operator has started working for this POS location. [Required] [Filter(multi eq;ge;le)] 
| [TerminationDate](Crm.Pos.Operators.md#terminationdate) | date (nullable) | The date, when the operator has ceased working in this POS location. null means, that the operator is still working or the termination date is still unknown. [Filter(multi eq;ge;le)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DefaultPosTerminal](Crm.Pos.Operators.md#defaultposterminal) | [Crm.Pos.Terminals](Crm.Pos.Terminals.md) (nullable) | The default POS terminal for this opertor. null when there is no default. [Filter(multi eq)] |
| [PosLocation](Crm.Pos.Operators.md#poslocation) | [Crm.Pos.Locations](Crm.Pos.Locations.md) | The POS location where this operator works. [Required] [Filter(multi eq)] |
| [PosRole](Crm.Pos.Operators.md#posrole) | [Crm.Pos.Roles](Crm.Pos.Roles.md) | The role, assigned to the operator. The role indicates the permissions of the operator for this POS location. [Required] [Filter(multi eq)] |
| [User](Crm.Pos.Operators.md#user) | [Systems.Security.Users](Systems.Security.Users.md) | The login user for this POS operator. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

> Indicates whether this operator is active and can be chosen for new records. [Required] [Default(true)] [Filter(multi eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### PosOperatorCode

> Operator code. Unique within the Pos Location. [Required] [Filter(multi eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **True**  

### StartingDate

> The first date, when the operator has started working for this POS location. [Required] [Filter(multi eq;ge;le)]

_Type_: **date**  
_Supported Filters_: **Equals, GreaterThanOrLessThan, EqualsIn**  
_Supports Order By_: **False**  

### TerminationDate

> The date, when the operator has ceased working in this POS location. null means, that the operator is still working or the termination date is still unknown. [Filter(multi eq;ge;le)]

_Type_: **date (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan, EqualsIn**  
_Supports Order By_: **False**  


## Reference Details

### DefaultPosTerminal

> The default POS terminal for this opertor. null when there is no default. [Filter(multi eq)]

_Type_: **[Crm.Pos.Terminals](Crm.Pos.Terminals.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### PosLocation

> The POS location where this operator works. [Required] [Filter(multi eq)]

_Type_: **[Crm.Pos.Locations](Crm.Pos.Locations.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### PosRole

> The role, assigned to the operator. The role indicates the permissions of the operator for this POS location. [Required] [Filter(multi eq)]

_Type_: **[Crm.Pos.Roles](Crm.Pos.Roles.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### User

> The login user for this POS operator. [Required] [Filter(multi eq)]

_Type_: **[Systems.Security.Users](Systems.Security.Users.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Crm.Pos.Operators erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.Pos.Operators erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Crm.Pos.Operators erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Pos_Operators?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Pos_Operators?$top=10>
