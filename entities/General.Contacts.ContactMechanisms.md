---
uid: General.Contacts.ContactMechanisms
---
# General.Contacts.ContactMechanisms

Contains contacting mechanisms - telephone numbers, addresses, web sites, etc. Contact mechanisms can be attached to parties. Currently each contact mechanism is attached to strictly one party. Entity: Cm_Contact_Mechanisms

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ContactMechanismType](General.Contacts.ContactMechanisms.md#contactmechanismtype) | [ContactMechanismType](General.Contacts.ContactMechanisms.md#contactmechanismtype) | A=Address; E=e-mail; T=Telephone. [Required] [Default("A")] [Filter(multi eq)] 
| [Id](General.Contacts.ContactMechanisms.md#id) | guid |  
| [Name](General.Contacts.ContactMechanisms.md#name) | string | Contact mechanism description. [Required] [Filter(eq;like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AdministrativeRegion](General.Contacts.ContactMechanisms.md#administrativeregion) | [General.Geography.AdministrativeRegions](General.Geography.AdministrativeRegions.md) (nullable) | The administrative region, where the contact mechanism is situated. Null if this is unknown or N/A. [Filter(multi eq)] (Introduced in version 18.2.100.0) |
| [GeoPoint](General.Contacts.ContactMechanisms.md#geopoint) | [General.Geography.GeoPoints](General.Geography.GeoPoints.md) (nullable) | The geographical point, where the contact mechanism is situated. Null if this is unknown or N/A. [Filter(multi eq)] (Introduced in version 18.2.100.0) |


## Attribute Details

### ContactMechanismType

> A=Address; E=e-mail; T=Telephone. [Required] [Default("A")] [Filter(multi eq)]

_Type_: **[ContactMechanismType](General.Contacts.ContactMechanisms.md#contactmechanismtype)**  
Allowed values for the [ContactMechanismType](General.Contacts.ContactMechanisms.md#contactmechanismtype) data attribute  
_Allowed Values (General.Contacts.ContactMechanismsRepository.ContactMechanismType Enum Members)_  

| Value | Description |
| ---- | --- |
| Address | Address value. Stored as 'A'. <br /> _Database Value:_ 'A' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Address' |
| Mail | Mail value. Stored as 'E'. <br /> _Database Value:_ 'E' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Mail' |
| Fax | Fax value. Stored as 'F'. <br /> _Database Value:_ 'F' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Fax' |
| MobilePhone | MobilePhone value. Stored as 'M'. <br /> _Database Value:_ 'M' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'MobilePhone' |
| Other | Other value. Stored as 'O'. <br /> _Database Value:_ 'O' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'Other' |
| Telephone | Telephone value. Stored as 'T'. <br /> _Database Value:_ 'T' <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'Telephone' |
| WebSite | WebSite value. Stored as 'W'. <br /> _Database Value:_ 'W' <br /> _Model Value:_ 6 <br /> _Domain API Value:_ 'WebSite' |

_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **Address**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

> Contact mechanism description. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  


## Reference Details

### AdministrativeRegion

> The administrative region, where the contact mechanism is situated. Null if this is unknown or N/A. [Filter(multi eq)] (Introduced in version 18.2.100.0)

_Type_: **[General.Geography.AdministrativeRegions](General.Geography.AdministrativeRegions.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### GeoPoint

> The geographical point, where the contact mechanism is situated. Null if this is unknown or N/A. [Filter(multi eq)] (Introduced in version 18.2.100.0)

_Type_: **[General.Geography.GeoPoints](General.Geography.GeoPoints.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=General.Contacts.ContactMechanisms erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Contacts.ContactMechanisms erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.Contacts.ContactMechanisms erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Contacts_ContactMechanisms?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Contacts_ContactMechanisms?$top=10>
