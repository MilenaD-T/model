---
uid: Logistics.Procurement.Suppliers
---
# Logistics.Procurement.Suppliers

Contains supplier conditions (contracts). Entity: Scm_Suppliers

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CreationTime](Logistics.Procurement.Suppliers.md#creationtime) | datetime (nullable) | Date and time when the Supplier was created. [Filter(ge;le)] [ReadOnly] 
| [CreationUser](Logistics.Procurement.Suppliers.md#creationuser) | string (nullable) | Login name of the user, who created the Supplier. [Filter(like)] [ReadOnly] 
| [DefaultDeliveryTermDays](Logistics.Procurement.Suppliers.md#defaultdeliverytermdays) | int32 | Default term in days for goods delivery, starting at the day of sending the purchase order. [Required] [Default(0)] 
| [DefaultPaymentStartDays](Logistics.Procurement.Suppliers.md#defaultpaymentstartdays) | int32 | Default number of days until the payment becomes executable. 0 means that the payment is executable at all times. [Required] [Default(0)] 
| [DefaultPaymentTermDays](Logistics.Procurement.Suppliers.md#defaultpaymenttermdays) | int32 | Default payment term in days, starting from the date of receiving the invoice. [Required] [Default(0)] 
| [FromDate](Logistics.Procurement.Suppliers.md#fromdate) | datetime (nullable) | The date on which this party became a supplier or the date, when the supplier contract was signed. [Filter(ge;le)] 
| [Id](Logistics.Procurement.Suppliers.md#id) | guid |  
| [IsActive](Logistics.Procurement.Suppliers.md#isactive) | boolean | Indicates whether the current supplier is active. [Required] [Default(true)] [Filter(eq)] 
| [Number](Logistics.Procurement.Suppliers.md#number) | string (nullable) | The unique supplier number. [Filter(eq)] [ORD] 
| [ThruDate](Logistics.Procurement.Suppliers.md#thrudate) | datetime (nullable) | The date (inclusive) on which this party ceased to be a supplier. [Filter(ge;le)] 
| [UpdateTime](Logistics.Procurement.Suppliers.md#updatetime) | datetime (nullable) | Date and time when the Supplier was last updated. [Filter(ge;le)] [ReadOnly] 
| [UpdateUser](Logistics.Procurement.Suppliers.md#updateuser) | string (nullable) | Login name of the user, who last updated the Supplier. [Filter(like)] [ReadOnly] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DefaultCurrency](Logistics.Procurement.Suppliers.md#defaultcurrency) | [General.Currencies](General.Currencies.md) (nullable) | The default currency for purchases from this supplier. null means there is no default. [Filter(multi eq)] |
| [DefaultPaymentAccount](Logistics.Procurement.Suppliers.md#defaultpaymentaccount) | [Finance.Payments.PaymentAccounts](Finance.Payments.PaymentAccounts.md) (nullable) | When not null, specifies the default payment account which should be used for new purchase document for this supplier. [Filter(multi eq)] |
| [DefaultPaymentType](Logistics.Procurement.Suppliers.md#defaultpaymenttype) | [Finance.Payments.PaymentTypes](Finance.Payments.PaymentTypes.md) (nullable) | When not null, specifies the default payment type which should be used for new purchase document for this supplier. [Filter(multi eq)] |
| [DefaultPurchasePriceList](Logistics.Procurement.Suppliers.md#defaultpurchasepricelist) | [Logistics.Procurement.PurchasePriceLists](Logistics.Procurement.PurchasePriceLists.md) (nullable) | The default purchase price list, which shall be used for new purchase documents for this supplier. [Filter(multi eq)] |
| [EnterpriseCompany](Logistics.Procurement.Suppliers.md#enterprisecompany) | [General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | The Enterprise Company to which this Supplier applies, or null if it is for all enterprise companies. [Filter(multi eq)] |
| [Party](Logistics.Procurement.Suppliers.md#party) | [General.Contacts.Parties](General.Contacts.Parties.md) | The [Party](General.Contacts.Parties.md) to which this Supplier belongs. [Required] [Filter(multi eq)] [Owner] |
| [SupplierType](Logistics.Procurement.Suppliers.md#suppliertype) | [Logistics.Procurement.SupplierTypes](Logistics.Procurement.SupplierTypes.md) (nullable) | When not null, specifies the type of this supplier. The type is primarily used for security access differentiation of the supplier records. [Filter(multi eq)] |


## Attribute Details

### CreationTime

> Date and time when the Supplier was created. [Filter(ge;le)] [ReadOnly]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### CreationUser

> Login name of the user, who created the Supplier. [Filter(like)] [ReadOnly]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### DefaultDeliveryTermDays

> Default term in days for goods delivery, starting at the day of sending the purchase order. [Required] [Default(0)]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### DefaultPaymentStartDays

> Default number of days until the payment becomes executable. 0 means that the payment is executable at all times. [Required] [Default(0)]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### DefaultPaymentTermDays

> Default payment term in days, starting from the date of receiving the invoice. [Required] [Default(0)]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### FromDate

> The date on which this party became a supplier or the date, when the supplier contract was signed. [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

> Indicates whether the current supplier is active. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Number

> The unique supplier number. [Filter(eq)] [ORD]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **True**  

### ThruDate

> The date (inclusive) on which this party ceased to be a supplier. [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### UpdateTime

> Date and time when the Supplier was last updated. [Filter(ge;le)] [ReadOnly]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### UpdateUser

> Login name of the user, who last updated the Supplier. [Filter(like)] [ReadOnly]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  


## Reference Details

### DefaultCurrency

> The default currency for purchases from this supplier. null means there is no default. [Filter(multi eq)]

_Type_: **[General.Currencies](General.Currencies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### DefaultPaymentAccount

> When not null, specifies the default payment account which should be used for new purchase document for this supplier. [Filter(multi eq)]

_Type_: **[Finance.Payments.PaymentAccounts](Finance.Payments.PaymentAccounts.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### DefaultPaymentType

> When not null, specifies the default payment type which should be used for new purchase document for this supplier. [Filter(multi eq)]

_Type_: **[Finance.Payments.PaymentTypes](Finance.Payments.PaymentTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### DefaultPurchasePriceList

> The default purchase price list, which shall be used for new purchase documents for this supplier. [Filter(multi eq)]

_Type_: **[Logistics.Procurement.PurchasePriceLists](Logistics.Procurement.PurchasePriceLists.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### EnterpriseCompany

> The Enterprise Company to which this Supplier applies, or null if it is for all enterprise companies. [Filter(multi eq)]

_Type_: **[General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Party

> The [Party](General.Contacts.Parties.md) to which this Supplier belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### SupplierType

> When not null, specifies the type of this supplier. The type is primarily used for security access differentiation of the supplier records. [Filter(multi eq)]

_Type_: **[Logistics.Procurement.SupplierTypes](Logistics.Procurement.SupplierTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Logistics.Procurement.Suppliers erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Procurement.Suppliers erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Procurement.Suppliers erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Procurement_Suppliers?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Procurement_Suppliers?$top=10>
