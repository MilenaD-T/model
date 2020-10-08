---
uid: Finance.Assets.AssetTransactionLines
---
# Finance.Assets.AssetTransactionLines

Asset value transaction lines. Each line changes the values of one asset in one valuation model. Entity: Ast_Asset_Transaction_Lines

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [DepreciationValue](Finance.Assets.AssetTransactionLines.md#depreciationvalue) | [Amount](../data-types.md#amount) | Change in the depreciation value of the asset (in the currency of the asset). [Currency: Asset.ValuationCurrency] [Required] [Default(0)] 
| [DepreciationValueBase](Finance.Assets.AssetTransactionLines.md#depreciationvaluebase) | [Amount](../data-types.md#amount) | Change in the depreciation value of the asset (in the currency of the enterprise company). [Currency: Asset.EnterpriseCompany.BaseCurrency] [Required] [Default(0)] 
| [Id](Finance.Assets.AssetTransactionLines.md#id) | guid |  
| [NegativeReserveValue](Finance.Assets.AssetTransactionLines.md#negativereservevalue) | [Amount](../data-types.md#amount) | Change in the value of the negative reserve after asset valuations (in the currency of the asset). [Currency: Asset.ValuationCurrency] [Required] [Default(0)] 
| [NegativeReserveValueBase](Finance.Assets.AssetTransactionLines.md#negativereservevaluebase) | [Amount](../data-types.md#amount) | Change in the value of the negative reserve after asset valuations (in the currency of the enterprise company). [Currency: Asset.EnterpriseCompany.BaseCurrency] [Required] [Default(0)] 
| [OperationType](Finance.Assets.AssetTransactionLines.md#operationtype) | [OperationType](Finance.Assets.AssetTransactionLines.md#operationtype) | Type of the current asset operation: PUR = Purchase, SLS = Sale, DEP = Depreciation, ADJ = Adjustment, REV = Reevaluation. [Required] [Default("ADJ")] [Filter(multi eq)] 
| [PositiveReserveValue](Finance.Assets.AssetTransactionLines.md#positivereservevalue) | [Amount](../data-types.md#amount) | Change in the value of the positive reserve after asset valuations (in the currency of the asset). [Currency: Asset.ValuationCurrency] [Required] [Default(0)] 
| [PositiveReserveValueBase](Finance.Assets.AssetTransactionLines.md#positivereservevaluebase) | [Amount](../data-types.md#amount) | Change in the value of the positive reserve after asset valuations (in the currency of the enterprise company). [Currency: Asset.EnterpriseCompany.BaseCurrency] [Required] [Default(0)] 
| [PurchaseValue](Finance.Assets.AssetTransactionLines.md#purchasevalue) | [Amount](../data-types.md#amount) | Change in the purchase value of the asset (in the currency of the asset). [Currency: Asset.ValuationCurrency] [Required] [Default(0)] 
| [PurchaseValueBase](Finance.Assets.AssetTransactionLines.md#purchasevaluebase) | [Amount](../data-types.md#amount) | Change in the purchase value of the asset (in the currency of the enterprise company). [Currency: Asset.EnterpriseCompany.BaseCurrency] [Required] [Default(0)] 
| [SalvageValue](Finance.Assets.AssetTransactionLines.md#salvagevalue) | [Amount](../data-types.md#amount) | Change in the salvage value of the asset (in the currency of the asset). [Currency: Asset.ValuationCurrency] [Required] [Default(0)] 
| [SalvageValueBase](Finance.Assets.AssetTransactionLines.md#salvagevaluebase) | [Amount](../data-types.md#amount) | Change in the salvage value of the asset (in the currency of the enterprise company). [Currency: Asset.EnterpriseCompany.BaseCurrency] [Required] [Default(0)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Asset](Finance.Assets.AssetTransactionLines.md#asset) | [Finance.Assets.Assets](Finance.Assets.Assets.md) | Asset for which changes in values have occurred. [Required] [Filter(multi eq)] |
| [AssetTransaction](Finance.Assets.AssetTransactionLines.md#assettransaction) | [Finance.Assets.AssetTransactions](Finance.Assets.AssetTransactions.md) | The [AssetTransaction](Finance.Assets.AssetTransactionLines.md#assettransaction) to which this AssetTransactionLine belongs. [Required] [Filter(multi eq)] [Owner] |
| [ValuationModel](Finance.Assets.AssetTransactionLines.md#valuationmodel) | [Finance.Assets.ValuationModels](Finance.Assets.ValuationModels.md) | Valuation model in which the changes of the asset values have occurred (Taxation model or Accounting model or other). [Required] [Filter(multi eq)] |


## Attribute Details

### DepreciationValue

> Change in the depreciation value of the asset (in the currency of the asset). [Currency: Asset.ValuationCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### DepreciationValueBase

> Change in the depreciation value of the asset (in the currency of the enterprise company). [Currency: Asset.EnterpriseCompany.BaseCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### NegativeReserveValue

> Change in the value of the negative reserve after asset valuations (in the currency of the asset). [Currency: Asset.ValuationCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### NegativeReserveValueBase

> Change in the value of the negative reserve after asset valuations (in the currency of the enterprise company). [Currency: Asset.EnterpriseCompany.BaseCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### OperationType

> Type of the current asset operation: PUR = Purchase, SLS = Sale, DEP = Depreciation, ADJ = Adjustment, REV = Reevaluation. [Required] [Default("ADJ")] [Filter(multi eq)]

_Type_: **[OperationType](Finance.Assets.AssetTransactionLines.md#operationtype)**  
Allowed values for the [OperationType](Finance.Assets.AssetTransactionLines.md#operationtype) data attribute  
_Allowed Values (Finance.Assets.AssetTransactionLinesRepository.OperationType Enum Members)_  

| Value | Description |
| ---- | --- |
| Adjustment | Adjustment value. Stored as 'ADJ'. <br /> _Database Value:_ 'ADJ' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Adjustment' |
| Depreciation | Depreciation value. Stored as 'DEP'. <br /> _Database Value:_ 'DEP' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Depreciation' |
| Purchase | Purchase value. Stored as 'PUR'. <br /> _Database Value:_ 'PUR' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Purchase' |
| Sale | Sale value. Stored as 'SLS'. <br /> _Database Value:_ 'SLS' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'Sale' |
| Reevaluation | Reevaluation value. Stored as 'REV'. <br /> _Database Value:_ 'REV' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'Reevaluation' |

_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **Adjustment**  

### PositiveReserveValue

> Change in the value of the positive reserve after asset valuations (in the currency of the asset). [Currency: Asset.ValuationCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### PositiveReserveValueBase

> Change in the value of the positive reserve after asset valuations (in the currency of the enterprise company). [Currency: Asset.EnterpriseCompany.BaseCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### PurchaseValue

> Change in the purchase value of the asset (in the currency of the asset). [Currency: Asset.ValuationCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### PurchaseValueBase

> Change in the purchase value of the asset (in the currency of the enterprise company). [Currency: Asset.EnterpriseCompany.BaseCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### SalvageValue

> Change in the salvage value of the asset (in the currency of the asset). [Currency: Asset.ValuationCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### SalvageValueBase

> Change in the salvage value of the asset (in the currency of the enterprise company). [Currency: Asset.EnterpriseCompany.BaseCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  


## Reference Details

### Asset

> Asset for which changes in values have occurred. [Required] [Filter(multi eq)]

_Type_: **[Finance.Assets.Assets](Finance.Assets.Assets.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### AssetTransaction

> The [AssetTransaction](Finance.Assets.AssetTransactionLines.md#assettransaction) to which this AssetTransactionLine belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Finance.Assets.AssetTransactions](Finance.Assets.AssetTransactions.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ValuationModel

> Valuation model in which the changes of the asset values have occurred (Taxation model or Accounting model or other). [Required] [Filter(multi eq)]

_Type_: **[Finance.Assets.ValuationModels](Finance.Assets.ValuationModels.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Finance.Assets.AssetTransactionLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Assets.AssetTransactionLines erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Assets.AssetTransactionLines erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Assets_AssetTransactionLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Assets_AssetTransactionLines?$top=10>
