---
uid: Finance.Accounting.VoucherCorrespondances
---
# Finance.Accounting.VoucherCorrespondances

Obsolete. Not used. Entity: Acc_Voucher_Correspondances

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [AmountBase](Finance.Accounting.VoucherCorrespondances.md#amountbase) | decimal | Obsolete. Not used. [Required] [Default(0)] 
| [CreditAmount](Finance.Accounting.VoucherCorrespondances.md#creditamount) | decimal | Obsolete. Not used. [Required] [Default(0)] 
| [CreditVoucherLineId](Finance.Accounting.VoucherCorrespondances.md#creditvoucherlineid) | guid | Obsolete. Not used. (The voucher line which contains the credited account). [Required] [Filter(multi eq)] 
| [DebitAmount](Finance.Accounting.VoucherCorrespondances.md#debitamount) | decimal | Obsolete. Not used. [Required] [Default(0)] 
| [DebitVoucherLineId](Finance.Accounting.VoucherCorrespondances.md#debitvoucherlineid) | guid | Obsolete. Not used. (The voucher line which contains the debited account). [Required] [Filter(multi eq)] 
| [Id](Finance.Accounting.VoucherCorrespondances.md#id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Voucher](Finance.Accounting.VoucherCorrespondances.md#voucher) | [Finance.Accounting.AccountingVouchers](Finance.Accounting.AccountingVouchers.md) | The [AccountingVoucher](Finance.Accounting.AccountingVouchers.md) to which this VoucherCorrespondance belongs. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### AmountBase

> Obsolete. Not used. [Required] [Default(0)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### CreditAmount

> Obsolete. Not used. [Required] [Default(0)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### CreditVoucherLineId

> Obsolete. Not used. (The voucher line which contains the credited account). [Required] [Filter(multi eq)]

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  

### DebitAmount

> Obsolete. Not used. [Required] [Default(0)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### DebitVoucherLineId

> Obsolete. Not used. (The voucher line which contains the debited account). [Required] [Filter(multi eq)]

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  


## Reference Details

### Voucher

> The [AccountingVoucher](Finance.Accounting.AccountingVouchers.md) to which this VoucherCorrespondance belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Finance.Accounting.AccountingVouchers](Finance.Accounting.AccountingVouchers.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Finance.Accounting.VoucherCorrespondances erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Accounting.VoucherCorrespondances erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Accounting.VoucherCorrespondances erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Accounting_VoucherCorrespondances?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Accounting_VoucherCorrespondances?$top=10>
