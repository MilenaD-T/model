---
uid: General.ProductVariants
---
# General.ProductVariants

Contains definitions of different variants of a product. The variants are differentiated by color, size and style. Entity: Gen_Product_Variants

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [BarCode](General.ProductVariants.md#barcode) | string (nullable) | When specified, it contains a bar code which uniquely identifies the product variant. [Filter(eq;like)] [ORD] 
| [Code](General.ProductVariants.md#code) | string | The code of the variant. The code is unique within the Product. It is the concatenation of the codes of the color, size and style. [Required] [Filter(eq;like)] [ReadOnly] 
| [Id](General.ProductVariants.md#id) | guid |  
| [Name](General.ProductVariants.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) (nullable) | Product variant name. It is the concatenation of the names of the color, size and style. [ReadOnly] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Product](General.ProductVariants.md#product) | [General.Products.Products](General.Products.Products.md) | The product for which this variant is defined. [Required] [Filter(multi eq)] [Owner] |
| [VariantColor](General.ProductVariants.md#variantcolor) | [General.Products.VariantColors](General.Products.VariantColors.md) (nullable) | The color of the variant. null means that the variant does not have a specific color. [Filter(multi eq)] |
| [VariantSize](General.ProductVariants.md#variantsize) | [General.Products.VariantSizes](General.Products.VariantSizes.md) (nullable) | The size of the variant. null means that the variant does not have a specific size. [Filter(multi eq)] |
| [VariantStyle](General.ProductVariants.md#variantstyle) | [General.Products.VariantStyles](General.Products.VariantStyles.md) (nullable) | The style of the variant. null means that the variant does not have a specific style. [Filter(multi eq)] |


## Attribute Details

### BarCode

> When specified, it contains a bar code which uniquely identifies the product variant. [Filter(eq;like)] [ORD]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### Code

> The code of the variant. The code is unique within the Product. It is the concatenation of the codes of the color, size and style. [Required] [Filter(eq;like)] [ReadOnly]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

> Product variant name. It is the concatenation of the names of the color, size and style. [ReadOnly]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`Join(" ", new [] {obj.VariantColor.Name, obj.VariantSize.Name, obj.VariantStyle.Name})`

_Front-End Recalc Expressions:_  
`Join(" ", new [] {obj.VariantColor.Name, obj.VariantSize.Name, obj.VariantStyle.Name})`

## Reference Details

### Product

> The product for which this variant is defined. [Required] [Filter(multi eq)] [Owner]

_Type_: **[General.Products.Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### VariantColor

> The color of the variant. null means that the variant does not have a specific color. [Filter(multi eq)]

_Type_: **[General.Products.VariantColors](General.Products.VariantColors.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### VariantSize

> The size of the variant. null means that the variant does not have a specific size. [Filter(multi eq)]

_Type_: **[General.Products.VariantSizes](General.Products.VariantSizes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### VariantStyle

> The style of the variant. null means that the variant does not have a specific style. [Filter(multi eq)]

_Type_: **[General.Products.VariantStyles](General.Products.VariantStyles.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=General.ProductVariants erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.ProductVariants erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.ProductVariants erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_ProductVariants?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_ProductVariants?$top=10>
