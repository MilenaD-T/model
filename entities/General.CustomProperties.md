---
uid: General.CustomProperties
---
# General.CustomProperties

User-defined properties, which can supplement the system properties of almost all entities in the system. Entity: Gen_Properties

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [AllowedValuesEntityName](General.CustomProperties.md#allowedvaluesentityname) | string (nullable) | When not null, specifies that the allowed values are retrieved from the specified entity. [Filter(eq)] 
| [AllowedValuesFilterXML](General.CustomProperties.md#allowedvaluesfilterxml) | string (nullable) | When not null specifies the filter to apply when extracting allowed values from entity. 
| [Code](General.CustomProperties.md#code) | string | Unique property code. [Required] [Filter(multi eq;like)] [ORD] 
| [EntityName](General.CustomProperties.md#entityname) | string | The entity for which the property is applicable. [Required] [Filter(eq)] [ORD] 
| [Hint](General.CustomProperties.md#hint) | [MultilanguageString](../data-types.md#multilanguagestring) (nullable) | The hint, which is displayed alongside the property. [Filter(multi eq;like)] (Introduced in version 20.1.100.0) 
| [Id](General.CustomProperties.md#id) | guid |  
| [KeyOrder](General.CustomProperties.md#keyorder) | byte (nullable) | When not null, indicates, that the property is a key property and contains the property consequtive position withing the entity. Used for BI and other analysis. 
| [LimitToAllowedValues](General.CustomProperties.md#limittoallowedvalues) | boolean | When true, allows the property to be set only to allowed value. When false, the property can have any value. [Required] [Default(false)] [Filter(eq)] 
| [MaskLength](General.CustomProperties.md#masklength) | int16 (nullable) | Limits te length of the property value to the specified number of characters. Null means no limitation. 
| [Name](General.CustomProperties.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | The name of this CustomProperty. [Required] [Filter(like)] [ORD] 
| [Notes](General.CustomProperties.md#notes) | string (nullable) | Notes for this CustomProperty. (Introduced in version 20.1.100.0) 
| [PropertyType](General.CustomProperties.md#propertytype) | [PropertyType](General.CustomProperties.md#propertytype) | Type of property values. 'T' - text; 'P' - picture; 'N' - number; 'D' - date. [Required] [Default("T")] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AllowedValuesParentProperty](General.CustomProperties.md#allowedvaluesparentproperty) | [General.CustomProperties](General.CustomProperties.md) (nullable) | Specifies the user defined property, which is used for filtering the allowed values by value of the parent property. [Filter(multi eq)] |
| [AllowedValuesProperty](General.CustomProperties.md#allowedvaluesproperty) | [General.CustomProperties](General.CustomProperties.md) (nullable) | When not null, specifies that the current property can have the same allowed values as the specified property. Also, this makes the current and the specified property copy-compatible. [Filter(multi eq)] |
| [PropertiesCategory](General.CustomProperties.md#propertiescategory) | [General.PropertiesCategories](General.PropertiesCategories.md) (nullable) | When not null, categorizes the property under a category. [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| AllowedValues | [General.CustomPropertyAllowedValues](General.CustomPropertyAllowedValues.md) | List of [CustomPropertyAllowedValue](General.CustomPropertyAllowedValues.md) child objects, based on the [General.CustomPropertyAllowedValue.Property](General.CustomPropertyAllowedValues.md#property) back reference 
| EnterpriseCompanyFilters | [General.PropertyEnterpriseCompanyFilters](General.PropertyEnterpriseCompanyFilters.md) | List of [PropertyEnterpriseCompanyFilter](General.PropertyEnterpriseCompanyFilters.md) child objects, based on the [General.PropertyEnterpriseCompanyFilter.Property](General.PropertyEnterpriseCompanyFilters.md#property) back reference 


## Attribute Details

### AllowedValuesEntityName

> When not null, specifies that the allowed values are retrieved from the specified entity. [Filter(eq)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### AllowedValuesFilterXML

> When not null specifies the filter to apply when extracting allowed values from entity.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Code

> Unique property code. [Required] [Filter(multi eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **True**  

### EntityName

> The entity for which the property is applicable. [Required] [Filter(eq)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **True**  

### Hint

> The hint, which is displayed alongside the property. [Filter(multi eq;like)] (Introduced in version 20.1.100.0)

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring) (nullable)**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### KeyOrder

> When not null, indicates, that the property is a key property and contains the property consequtive position withing the entity. Used for BI and other analysis.

_Type_: **byte (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### LimitToAllowedValues

> When true, allows the property to be set only to allowed value. When false, the property can have any value. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### MaskLength

> Limits te length of the property value to the specified number of characters. Null means no limitation.

_Type_: **int16 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Name

> The name of this CustomProperty. [Required] [Filter(like)] [ORD]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Like**  
_Supports Order By_: **True**  

### Notes

> Notes for this CustomProperty. (Introduced in version 20.1.100.0)

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PropertyType

> Type of property values. 'T' - text; 'P' - picture; 'N' - number; 'D' - date. [Required] [Default("T")]

_Type_: **[PropertyType](General.CustomProperties.md#propertytype)**  
Allowed values for the [PropertyType](General.CustomProperties.md#propertytype) data attribute  
_Allowed Values (General.CustomPropertiesRepository.PropertyType Enum Members)_  

| Value | Description |
| ---- | --- |
| Text | Text value. Stored as 'T'. <br /> _Database Value:_ 'T' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Text' |
| Number | Number value. Stored as 'N'. <br /> _Database Value:_ 'N' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Number' |
| Picture | Picture value. Stored as 'P'. <br /> _Database Value:_ 'P' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Picture' |
| Date | Date value. Stored as 'D'. <br /> _Database Value:_ 'D' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'Date' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Text**  


## Reference Details

### AllowedValuesParentProperty

> Specifies the user defined property, which is used for filtering the allowed values by value of the parent property. [Filter(multi eq)]

_Type_: **[General.CustomProperties](General.CustomProperties.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### AllowedValuesProperty

> When not null, specifies that the current property can have the same allowed values as the specified property. Also, this makes the current and the specified property copy-compatible. [Filter(multi eq)]

_Type_: **[General.CustomProperties](General.CustomProperties.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### PropertiesCategory

> When not null, categorizes the property under a category. [Filter(multi eq)]

_Type_: **[General.PropertiesCategories](General.PropertiesCategories.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=General.CustomProperties erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.CustomProperties erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.CustomProperties erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_CustomProperties?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_CustomProperties?$top=10>
