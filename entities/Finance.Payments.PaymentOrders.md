---
uid: Finance.Payments.PaymentOrders
---
# Finance.Payments.PaymentOrders

Each payment order contains a receivable or payable amount. Entity: Cash_Payment_Orders

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [AllowCloseNotPaid](Finance.Payments.PaymentOrders.md#allowclosenotpaid) | boolean | True to allow closing of payment orders, that are not fully paid. [Required] [Default(false)] [Filter(eq)] 
| [BillTo](Finance.Payments.PaymentOrders.md#billto) | [BillTo](Finance.Payments.PaymentOrders.md#billto) (nullable) | If filled indicates which party is billed for the total amount. Possible values: 'C' = Company (means the Party_Id), 'L' = Company location (the Location_Party_Id), null = unidentified. [Filter(eq)] 
| [CompleteTime](Finance.Payments.PaymentOrders.md#completetime) | datetime (nullable) | Exact time, when the document was last completed[Filter(ge;le)] 
| [CreationTime](Finance.Payments.PaymentOrders.md#creationtime) | datetime | Date/Time when the document was created [Required][Filter(ge;le)] 
| [CreationUser](Finance.Payments.PaymentOrders.md#creationuser) | string | The login name of the user, who created the document [Required][Filter(like)] 
| [Direction](Finance.Payments.PaymentOrders.md#direction) | [Direction](Finance.Payments.PaymentOrders.md#direction) | I for Payment issue, R for payment receipt. [Required] [Default("I")] [Filter(eq)] 
| [DocumentDate](Finance.Payments.PaymentOrders.md#documentdate) | datetime | The date on which the document was issued [Required][Filter(eq;ge;le)][ORD] 
| [DocumentNo](Finance.Payments.PaymentOrders.md#documentno) | string | Document number, unique within Document_Type_Id [Required][Filter(eq;like)][ORD] 
| [DocumentNotes](Finance.Payments.PaymentOrders.md#documentnotes) | string (nullable) | Notes for this Document 
| [DocumentVersion](Finance.Payments.PaymentOrders.md#documentversion) | int32 | [Filter(eq;ge;le)] 
| [DueDate](Finance.Payments.PaymentOrders.md#duedate) | datetime (nullable) | The due date of the payment. null means there is no due date. [Filter(eq;ge;le)] 
| [DueStartDate](Finance.Payments.PaymentOrders.md#duestartdate) | date (nullable) | The date at which the payment becomes executable. null means the payment is executable at all times. [Filter(eq;ge;le)] [ORD] 
| [EntityName](Finance.Payments.PaymentOrders.md#entityname) | string | The entity name of the document equal to the entity name of the document type.[Filter(eq)] [ORD] 
| [Id](Finance.Payments.PaymentOrders.md#id) | guid |  
| [InstallmentNumber](Finance.Payments.PaymentOrders.md#installmentnumber) | int32 (nullable) | Consequtive installment number. Used for identifying the payment when using payment plans. null means that the payment is not part of a payment plan. [Filter(eq)] 
| [InvoiceAmount](Finance.Payments.PaymentOrders.md#invoiceamount) | [Amount](../data-types.md#amount) (nullable) | The invoice amount that is specified in this payment order. (the invoice amount converted to the Total_Amount_Currency_Id must be equal to the Total_Amount). [Currency: InvoiceAmountCurrency] 
| [IsAmountWithVAT](Finance.Payments.PaymentOrders.md#isamountwithvat) | boolean | Is_Amount_With_VAT=true if the requested amount includes VAT. [Required] [Default(true)] [Filter(eq)] 
| [IsReleased](Finance.Payments.PaymentOrders.md#isreleased) | boolean | True if the document is not void and its state is released or greater. [Required] [Default(false)] [Filter(eq)] [ReadOnly] 
| [IsSingleExecution](Finance.Payments.PaymentOrders.md#issingleexecution) | boolean | Specifies whether the document is a single execution of its order document. [Required] [Default(false)] [Filter(eq)] [ReadOnly] 
| [Notes](Finance.Payments.PaymentOrders.md#notes) | string (nullable) | Notes for this PaymentOrder. 
| [ParentDocumentRelationshipType](Finance.Payments.PaymentOrders.md#parentdocumentrelationshiptype) | [ParentDocumentRelationshipType](Finance.Payments.PaymentOrders.md#parentdocumentrelationshiptype) (nullable) | Type of relationship between the current document and the parent document(s). Affects the constraints for execution/completion for the documents. Possible values: 'S' = 'Subtask', 'N' = 'Next task'. 
| [PlanningOnly](Finance.Payments.PaymentOrders.md#planningonly) | boolean (nullable) | Indicates that the document is used only for planning (and as consequence its state cannot be greater than Planned) [Required] 
| [ReadOnly](Finance.Payments.PaymentOrders.md#readonly) | boolean | True - the document is read only; false - the document is not read only [Required] 
| [RefDocumentDate](Finance.Payments.PaymentOrders.md#refdocumentdate) | datetime (nullable) | The date of the original document. null means that it is unknown. [Filter(eq)] 
| [RefDocumentNo](Finance.Payments.PaymentOrders.md#refdocumentno) | string | The number of the document which has created the payment order and is the basis for the payment. [Required] [Filter(eq)] 
| [ReferenceDate](Finance.Payments.PaymentOrders.md#referencedate) | datetime (nullable) | The date to which this document refers, i.e. when the action really occurred. If null, Document_Date is taken [Filter(ge;le)] 
| [ReferenceDocumentNo](Finance.Payments.PaymentOrders.md#referencedocumentno) | string (nullable) | The number of the document (issued by the other party), which was the reason for the creation of the current document. The numebr should be unique within the party documents [Filter(eq;like)] 
| [RefInvoiceApplyDate](Finance.Payments.PaymentOrders.md#refinvoiceapplydate) | datetime (nullable) | The apply date of the related invoice. Not specified when the payment order isn't related to any invoice or the apply date is unknown. [Filter(eq;ge;le)] 
| [RefInvoiceDocumentDate](Finance.Payments.PaymentOrders.md#refinvoicedocumentdate) | datetime (nullable) | The date of the related invoice. null means that the payment order isn't related to any invoice or the date is unknown. [Filter(eq;ge;le)] 
| [RefInvoiceDocumentNo](Finance.Payments.PaymentOrders.md#refinvoicedocumentno) | string (nullable) | The number of the invoice which has created or is related to the payment order and is the basis for the payment. null means that the payment order isn't created or related to any invoice. [Filter(eq)] 
| [ReleaseTime](Finance.Payments.PaymentOrders.md#releasetime) | datetime (nullable) | Exact time, when the document was first released [Filter(ge;le)] 
| [State](Finance.Payments.PaymentOrders.md#state) | [DocumentState](Finance.Payments.PaymentOrders.md#state) | 0=New;5=Corrective;10=Computer Planned;20=Human Planned;30=Released;40=Completed;50=Closed [Required][Filter(eq;ge;le)] 
| [TotalAmount](Finance.Payments.PaymentOrders.md#totalamount) | [Amount](../data-types.md#amount) | Total amount that should be payed. [Currency: TotalAmountCurrency] [Required] [Default(0)] [Filter(eq;ge;le)] 
| [Void](Finance.Payments.PaymentOrders.md#void) | boolean | True if the document is null and void [Required][Filter(eq)] 
| [VoidReason](Finance.Payments.PaymentOrders.md#voidreason) | string (nullable) | Reason for voiding the document, entered by the user 
| [VoidTime](Finance.Payments.PaymentOrders.md#voidtime) | datetime (nullable) | Date/time when the document has become void 
| [VoidUser](Finance.Payments.PaymentOrders.md#voiduser) | string (nullable) | The user who voided the document 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AccessKey](Finance.Payments.PaymentOrders.md#accesskey) | [Systems.Security.AccessKeys](Systems.Security.AccessKeys.md) (nullable) | The access key, containing the user permissions for this document. null means that all users have unlimited permissions |
| [AdjustedDocument](Finance.Payments.PaymentOrders.md#adjusteddocument) | [General.Documents](General.Documents.md) (nullable) | The primary document, which the current document adjusts. null when this is not an adjustment document |
| [AssignedToUser](Finance.Payments.PaymentOrders.md#assignedtouser) | [Systems.Security.Users](Systems.Security.Users.md) (nullable) | The user to which this document is assigned for handling. null means that the document is not assigned to specific user |
| [CurrencyDirectory](Finance.Payments.PaymentOrders.md#currencydirectory) | [General.CurrencyDirectories](General.CurrencyDirectories.md) (nullable) | The currency directory, containing all the convertion rates, used by the document. null means that the document does not need currency convertions |
| [DocumentType](Finance.Payments.PaymentOrders.md#documenttype) | [General.DocumentTypes](General.DocumentTypes.md) | The user defined type of the document. Determines document behaviour, properties, additional amounts, validation, generations, etc. [Required] |
| [EnterpriseCompany](Finance.Payments.PaymentOrders.md#enterprisecompany) | [General.EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company which issued the document [Required] |
| [EnterpriseCompanyLocation](Finance.Payments.PaymentOrders.md#enterprisecompanylocation) | [General.Contacts.CompanyLocations](General.Contacts.CompanyLocations.md) (nullable) | The enterprise company location which issued the document. null means that there is only one location within the enterprise company and locations are not used |
| [FiscalPrinterPosDevice](Finance.Payments.PaymentOrders.md#fiscalprinterposdevice) | [Crm.Pos.Devices](Crm.Pos.Devices.md) (nullable) | When not null, contains suggested fiscal printer for printing fiscal notes upon payment. [Filter(multi eq)] (Introduced in version 19.1.100.0) |
| [FromCompanyDivision](Finance.Payments.PaymentOrders.md#fromcompanydivision) | [General.Contacts.CompanyDivisions](General.Contacts.CompanyDivisions.md) (nullable) | The division of the company, issuing the document. null when the document is not issued by any specific division |
| [FromParty](Finance.Payments.PaymentOrders.md#fromparty) | [General.Contacts.Parties](General.Contacts.Parties.md) | The party which issued the document [Required] |
| [InvoiceAmountCurrency](Finance.Payments.PaymentOrders.md#invoiceamountcurrency) | [General.Currencies](General.Currencies.md) (nullable) | The currency of Invoice Amount. [Filter(multi eq)] |
| [LocationParty](Finance.Payments.PaymentOrders.md#locationparty) | [General.Contacts.Parties](General.Contacts.Parties.md) (nullable) | Location or sub-party of the Party_Id in the order. [Filter(multi eq)] |
| [MasterDocument](Finance.Payments.PaymentOrders.md#masterdocument) | [General.Documents](General.Documents.md) | In a multi-document tree, this is the root document, that created the whole tree. If this is the root it is equal to Id [Required] |
| [Parent](Finance.Payments.PaymentOrders.md#parent) | [General.Documents](General.Documents.md) (nullable) | In a multi-document tree, this is the direct parent document. If this is the root it is null |
| [Party](Finance.Payments.PaymentOrders.md#party) | [General.Contacts.Parties](General.Contacts.Parties.md) | The party which is to pay or receive the amount. [Required] [Filter(multi eq)] |
| [PaymentAccount](Finance.Payments.PaymentOrders.md#paymentaccount) | [Finance.Payments.PaymentAccounts](Finance.Payments.PaymentAccounts.md) (nullable) | When not null, specifies the payment account that is expected or will be used by the payment transaction. [Filter(multi eq)] |
| [PaymentType](Finance.Payments.PaymentOrders.md#paymenttype) | [Finance.Payments.PaymentTypes](Finance.Payments.PaymentTypes.md) (nullable) | Expected payment type. Null when there is no expectation. Can also specify default payment account. [Filter(multi eq)] |
| [PrimeCauseDocument](Finance.Payments.PaymentOrders.md#primecausedocument) | [General.Documents](General.Documents.md) (nullable) | The document that is the prime cause for creation of the current document |
| [RefDocument](Finance.Payments.PaymentOrders.md#refdocument) | [General.Documents](General.Documents.md) (nullable) | The document which has created the payment order and is the basis for the payment. If this column is filled then Ref_Document_Type_Id, Ref_Document_No and Ref_Document_Date must be equal to the type, number and date of the specified document. [Filter(multi eq)] |
| [RefDocumentType](Finance.Payments.PaymentOrders.md#refdocumenttype) | [General.DocumentTypes](General.DocumentTypes.md) | The type of the document which has created the payment order and is the basis for the payment. [Required] [Filter(multi eq)] |
| [RefInvoiceDocument](Finance.Payments.PaymentOrders.md#refinvoicedocument) | [General.Documents](General.Documents.md) (nullable) | The invoice document which has created or is related to the payment order and is the basis for the payment. null means that the payment order isn't created or related to any invoice or the invoice isn't present in the database. If this column is filled then Ref_Invoice_Document_Type_Id, Ref_Invoice_Document_No and Ref_Invoice_Document_Date must be equal to the type, number and date of the specified invoice document. [Filter(multi eq)] |
| [RefInvoiceDocumentType](Finance.Payments.PaymentOrders.md#refinvoicedocumenttype) | [General.DocumentTypes](General.DocumentTypes.md) (nullable) | The document type of the invoice which has created or is related to the payment order and is the basis for the payment. null means that the payment order isn't created or related to any invoice. [Filter(multi eq)] |
| [ResponsiblePerson](Finance.Payments.PaymentOrders.md#responsibleperson) | [General.Contacts.Persons](General.Contacts.Persons.md) (nullable) | The person that is responsible for this order or transaction. It could be the sales person, the orderer, etc. |
| [ReverseOfDocument](Finance.Payments.PaymentOrders.md#reverseofdocument) | [General.Documents](General.Documents.md) (nullable) | The document which the current document is reverse of |
| [Sequence](Finance.Payments.PaymentOrders.md#sequence) | [General.Sequences](General.Sequences.md) (nullable) | The sequence that will be used to give new numbers to the documents of this type |
| [ToCompanyDivision](Finance.Payments.PaymentOrders.md#tocompanydivision) | [General.Contacts.CompanyDivisions](General.Contacts.CompanyDivisions.md) | The division of the company, receiving the document. null when the document is not received by any specific division |
| [ToParty](Finance.Payments.PaymentOrders.md#toparty) | [General.Contacts.Parties](General.Contacts.Parties.md) (nullable) | The party which should receive the document |
| [TotalAmountCurrency](Finance.Payments.PaymentOrders.md#totalamountcurrency) | [General.Currencies](General.Currencies.md) | The currency of Total Amount. [Required] [Filter(multi eq)] |
| [UserStatus](Finance.Payments.PaymentOrders.md#userstatus) | [General.DocumentTypeUserStatuses](General.DocumentTypeUserStatuses.md) (nullable) | The user status of this document if applicable for this document type. null means unknown or not yet set |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Comments | [General.DocumentComments](General.DocumentComments.md) | List of [DocumentComment](General.DocumentComments.md) child objects, based on the [DocumentComment.Document](General.DocumentComments.md#document) back reference 
| DistributedAmounts | [General.DocumentDistributedAmounts](General.DocumentDistributedAmounts.md) | List of [DocumentDistributedAmount](General.DocumentDistributedAmounts.md) child objects, based on the [DocumentDistributedAmount.Document](General.DocumentDistributedAmounts.md#document) back reference 
| DocumentAmounts | [General.DocumentAmounts](General.DocumentAmounts.md) |  
| FileAttachments | [General.DocumentFileAttachments](General.DocumentFileAttachments.md) | List of [DocumentFileAttachment](General.DocumentFileAttachments.md) child objects, based on the [DocumentFileAttachment.Document](General.DocumentFileAttachments.md#document) back reference 
| LineAmounts | [General.DocumentLineAmounts](General.DocumentLineAmounts.md) | List of [DocumentLineAmount](General.DocumentLineAmounts.md) child objects, based on the [DocumentLineAmount.Document](General.DocumentLineAmounts.md#document) back reference 
| Prints | [General.DocumentPrints](General.DocumentPrints.md) | List of [DocumentPrint](General.DocumentPrints.md) child objects, based on the [DocumentPrint.Document](General.DocumentPrints.md#document) back reference 
| StateChanges | [General.DocumentStateChanges](General.DocumentStateChanges.md) | List of [DocumentStateChange](General.DocumentStateChanges.md) child objects, based on the [DocumentStateChange.Document](General.DocumentStateChanges.md#document) back reference 
| Versions | [General.DocumentVersions](General.DocumentVersions.md) | List of [DocumentVersion](General.Documents.md#documentversion) child objects, based on the [DocumentVersion.Document](General.DocumentVersions.md#document) back reference 


## Attribute Details

### AllowCloseNotPaid

> True to allow closing of payment orders, that are not fully paid. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### BillTo

> If filled indicates which party is billed for the total amount. Possible values: 'C' = Company (means the Party_Id), 'L' = Company location (the Location_Party_Id), null = unidentified. [Filter(eq)]

_Type_: **[BillTo](Finance.Payments.PaymentOrders.md#billto) (nullable)**  
Allowed values for the [BillTo](Finance.Payments.PaymentOrders.md#billto) data attribute  
_Allowed Values (Finance.Payments.PaymentOrdersRepository.BillTo Enum Members)_  

| Value | Description |
| ---- | --- |
| Company | Company value. Stored as 'C'. <br /> _Database Value:_ 'C' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Company' |
| CompanyLocation | CompanyLocation value. Stored as 'L'. <br /> _Database Value:_ 'L' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'CompanyLocation' |

_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### CompleteTime

> Exact time, when the document was last completed[Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### CreationTime

> Date/Time when the document was created [Required][Filter(ge;le)]

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTime**  

### CreationUser

> The login name of the user, who created the document [Required][Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Direction

> I for Payment issue, R for payment receipt. [Required] [Default("I")] [Filter(eq)]

_Type_: **[Direction](Finance.Payments.PaymentOrders.md#direction)**  
Allowed values for the [Direction](Finance.Payments.PaymentOrders.md#direction) data attribute  
_Allowed Values (Finance.Payments.PaymentOrdersRepository.Direction Enum Members)_  

| Value | Description |
| ---- | --- |
| Expense | Expense value. Stored as 'I'. <br /> _Database Value:_ 'I' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Expense' |
| Income | Income value. Stored as 'R'. <br /> _Database Value:_ 'R' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Income' |

_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **Expense**  

### DocumentDate

> The date on which the document was issued [Required][Filter(eq;ge;le)][ORD]

_Type_: **datetime**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **True**  
_Default Value_: **CurrentDate**  

### DocumentNo

> Document number, unique within Document_Type_Id [Required][Filter(eq;like)][ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### DocumentNotes

> Notes for this Document

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DocumentVersion

> [Filter(eq;ge;le)]

_Type_: **int32**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **1**  

### DueDate

> The due date of the payment. null means there is no due date. [Filter(eq;ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### DueStartDate

> The date at which the payment becomes executable. null means the payment is executable at all times. [Filter(eq;ge;le)] [ORD]

_Type_: **date (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **True**  

### EntityName

> The entity name of the document equal to the entity name of the document type.[Filter(eq)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **True**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### InstallmentNumber

> Consequtive installment number. Used for identifying the payment when using payment plans. null means that the payment is not part of a payment plan. [Filter(eq)]

_Type_: **int32 (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### InvoiceAmount

> The invoice amount that is specified in this payment order. (the invoice amount converted to the Total_Amount_Currency_Id must be equal to the Total_Amount). [Currency: InvoiceAmountCurrency]

_Type_: **[Amount](../data-types.md#amount) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### IsAmountWithVAT

> Is_Amount_With_VAT=true if the requested amount includes VAT. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### IsReleased

> True if the document is not void and its state is released or greater. [Required] [Default(false)] [Filter(eq)] [ReadOnly]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### IsSingleExecution

> Specifies whether the document is a single execution of its order document. [Required] [Default(false)] [Filter(eq)] [ReadOnly]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Notes

> Notes for this PaymentOrder.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ParentDocumentRelationshipType

> Type of relationship between the current document and the parent document(s). Affects the constraints for execution/completion for the documents. Possible values: 'S' = 'Subtask', 'N' = 'Next task'.

_Type_: **[ParentDocumentRelationshipType](Finance.Payments.PaymentOrders.md#parentdocumentrelationshiptype) (nullable)**  
Relationship between parent and child documents  
_Allowed Values (General.ParentDocumentRelationshipType Enum Members)_  

| Value | Description |
| ---- | --- |
| Subtask | The child document is a sub-task of the parent document. (Complete child to complete parent) <br /> _Database Value:_ 'S' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Subtask' |
| NextTask | The child document is next task of the parent document. (Complete parent to complete child) <br /> _Database Value:_ 'N' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'NextTask' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PlanningOnly

> Indicates that the document is used only for planning (and as consequence its state cannot be greater than Planned) [Required]

_Type_: **boolean (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### ReadOnly

> True - the document is read only; false - the document is not read only [Required]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### RefDocumentDate

> The date of the original document. null means that it is unknown. [Filter(eq)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.RefDocument.DocumentDate`

_Front-End Recalc Expressions:_  
`obj.RefDocument.DocumentDate`
### RefDocumentNo

> The number of the document which has created the payment order and is the basis for the payment. [Required] [Filter(eq)]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.RefDocument.DocumentNo`

_Front-End Recalc Expressions:_  
`obj.RefDocument.DocumentNo`
### ReferenceDate

> The date to which this document refers, i.e. when the action really occurred. If null, Document_Date is taken [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### ReferenceDocumentNo

> The number of the document (issued by the other party), which was the reason for the creation of the current document. The numebr should be unique within the party documents [Filter(eq;like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### RefInvoiceApplyDate

> The apply date of the related invoice. Not specified when the payment order isn't related to any invoice or the apply date is unknown. [Filter(eq;ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`Convert(obj.RefInvoiceDocument, IInvoiceDocument).ApplyDate`

_Front-End Recalc Expressions:_  
`Convert(obj.RefInvoiceDocument, IInvoiceDocument).ApplyDate`
### RefInvoiceDocumentDate

> The date of the related invoice. null means that the payment order isn't related to any invoice or the date is unknown. [Filter(eq;ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.RefInvoiceDocument.DocumentDate`

_Front-End Recalc Expressions:_  
`obj.RefInvoiceDocument.DocumentDate`
### RefInvoiceDocumentNo

> The number of the invoice which has created or is related to the payment order and is the basis for the payment. null means that the payment order isn't created or related to any invoice. [Filter(eq)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.RefInvoiceDocument.DocumentNo`

_Front-End Recalc Expressions:_  
`obj.RefInvoiceDocument.DocumentNo`
### ReleaseTime

> Exact time, when the document was first released [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### State

> 0=New;5=Corrective;10=Computer Planned;20=Human Planned;30=Released;40=Completed;50=Closed [Required][Filter(eq;ge;le)]

_Type_: **[DocumentState](Finance.Payments.PaymentOrders.md#state)**  
Enumeration of document system states  
_Allowed Values (General.DocumentState Enum Members)_  

| Value | Description |
| ---- | --- |
| New | New document, just created. Can be edited. (Stored as 0). <br /> _Database Value:_ 0 <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'New' |
| Adjustment | Document which adjusts other released documents. (Stored as 5). <br /> _Database Value:_ 5 <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'Adjustment' |
| Planned | Planned by the system for future releasing. (Stored as 10). <br /> _Database Value:_ 10 <br /> _Model Value:_ 10 <br /> _Domain API Value:_ 'Planned' |
| FirmPlanned | Planned by operator for future releasing. (Stored as 20). <br /> _Database Value:_ 20 <br /> _Model Value:_ 20 <br /> _Domain API Value:_ 'FirmPlanned' |
| Released | Released document. Changes can be applied only through adjustment documents. (Stored as 30). <br /> _Database Value:_ 30 <br /> _Model Value:_ 30 <br /> _Domain API Value:_ 'Released' |
| Completed | Work has completed. (Stored as 40). <br /> _Database Value:_ 40 <br /> _Model Value:_ 40 <br /> _Domain API Value:_ 'Completed' |
| Closed | The document is audited and closed. Adjustments are not allowed, but reopening is allowed. (Stored as 50). <br /> _Database Value:_ 50 <br /> _Model Value:_ 50 <br /> _Domain API Value:_ 'Closed' |

_Supported Filters_: **Equals, GreaterThanOrLessThan, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### TotalAmount

> Total amount that should be payed. [Currency: TotalAmountCurrency] [Required] [Default(0)] [Filter(eq;ge;le)]

_Type_: **[Amount](../data-types.md#amount)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### Void

> True if the document is null and void [Required][Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### VoidReason

> Reason for voiding the document, entered by the user

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### VoidTime

> Date/time when the document has become void

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### VoidUser

> The user who voided the document

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### AccessKey

> The access key, containing the user permissions for this document. null means that all users have unlimited permissions

_Type_: **[Systems.Security.AccessKeys](Systems.Security.AccessKeys.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### AdjustedDocument

> The primary document, which the current document adjusts. null when this is not an adjustment document

_Type_: **[General.Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### AssignedToUser

> The user to which this document is assigned for handling. null means that the document is not assigned to specific user

_Type_: **[Systems.Security.Users](Systems.Security.Users.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### CurrencyDirectory

> The currency directory, containing all the convertion rates, used by the document. null means that the document does not need currency convertions

_Type_: **[General.CurrencyDirectories](General.CurrencyDirectories.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### DocumentType

> The user defined type of the document. Determines document behaviour, properties, additional amounts, validation, generations, etc. [Required]

_Type_: **[General.DocumentTypes](General.DocumentTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### EnterpriseCompany

> The enterprise company which issued the document [Required]

_Type_: **[General.EnterpriseCompanies](General.EnterpriseCompanies.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### EnterpriseCompanyLocation

> The enterprise company location which issued the document. null means that there is only one location within the enterprise company and locations are not used

_Type_: **[General.Contacts.CompanyLocations](General.Contacts.CompanyLocations.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### FiscalPrinterPosDevice

> When not null, contains suggested fiscal printer for printing fiscal notes upon payment. [Filter(multi eq)] (Introduced in version 19.1.100.0)

_Type_: **[Crm.Pos.Devices](Crm.Pos.Devices.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### FromCompanyDivision

> The division of the company, issuing the document. null when the document is not issued by any specific division

_Type_: **[General.Contacts.CompanyDivisions](General.Contacts.CompanyDivisions.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### FromParty

> The party which issued the document [Required]

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### InvoiceAmountCurrency

> The currency of Invoice Amount. [Filter(multi eq)]

_Type_: **[General.Currencies](General.Currencies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### LocationParty

> Location or sub-party of the Party_Id in the order. [Filter(multi eq)]

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### MasterDocument

> In a multi-document tree, this is the root document, that created the whole tree. If this is the root it is equal to Id [Required]

_Type_: **[General.Documents](General.Documents.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Parent

> In a multi-document tree, this is the direct parent document. If this is the root it is null

_Type_: **[General.Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Party

> The party which is to pay or receive the amount. [Required] [Filter(multi eq)]

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  

_Back-End Default Expression:_  
`obj.LocationParty.ParentParty`

### PaymentAccount

> When not null, specifies the payment account that is expected or will be used by the payment transaction. [Filter(multi eq)]

_Type_: **[Finance.Payments.PaymentAccounts](Finance.Payments.PaymentAccounts.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`obj.PaymentType.GetDefaultPaymentAccount().IfNullThen(obj.PaymentAccount)`
### PaymentType

> Expected payment type. Null when there is no expectation. Can also specify default payment account. [Filter(multi eq)]

_Type_: **[Finance.Payments.PaymentTypes](Finance.Payments.PaymentTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### PrimeCauseDocument

> The document that is the prime cause for creation of the current document

_Type_: **[General.Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **EqualsIn**  

### RefDocument

> The document which has created the payment order and is the basis for the payment. If this column is filled then Ref_Document_Type_Id, Ref_Document_No and Ref_Document_Date must be equal to the type, number and date of the specified document. [Filter(multi eq)]

_Type_: **[General.Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### RefDocumentType

> The type of the document which has created the payment order and is the basis for the payment. [Required] [Filter(multi eq)]

_Type_: **[General.DocumentTypes](General.DocumentTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  

_Back-End Default Expression:_  
`obj.RefDocument.DocumentType`

_Front-End Recalc Expressions:_  
`obj.RefDocument.DocumentType`
### RefInvoiceDocument

> The invoice document which has created or is related to the payment order and is the basis for the payment. null means that the payment order isn't created or related to any invoice or the invoice isn't present in the database. If this column is filled then Ref_Invoice_Document_Type_Id, Ref_Invoice_Document_No and Ref_Invoice_Document_Date must be equal to the type, number and date of the specified invoice document. [Filter(multi eq)]

_Type_: **[General.Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### RefInvoiceDocumentType

> The document type of the invoice which has created or is related to the payment order and is the basis for the payment. null means that the payment order isn't created or related to any invoice. [Filter(multi eq)]

_Type_: **[General.DocumentTypes](General.DocumentTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Back-End Default Expression:_  
`obj.RefInvoiceDocument.DocumentType`

_Front-End Recalc Expressions:_  
`obj.RefInvoiceDocument.DocumentType`
### ResponsiblePerson

> The person that is responsible for this order or transaction. It could be the sales person, the orderer, etc.

_Type_: **[General.Contacts.Persons](General.Contacts.Persons.md) (nullable)**  
_Supported Filters_: **EqualsIn**  

### ReverseOfDocument

> The document which the current document is reverse of

_Type_: **[General.Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **EqualsIn**  

### Sequence

> The sequence that will be used to give new numbers to the documents of this type

_Type_: **[General.Sequences](General.Sequences.md) (nullable)**  
_Supported Filters_: **EqualsIn**  

### ToCompanyDivision

> The division of the company, receiving the document. null when the document is not received by any specific division

_Type_: **[General.Contacts.CompanyDivisions](General.Contacts.CompanyDivisions.md)**  
_Supported Filters_: **NotFilterable**  

### ToParty

> The party which should receive the document

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md) (nullable)**  
_Supported Filters_: **EqualsIn**  

### TotalAmountCurrency

> The currency of Total Amount. [Required] [Filter(multi eq)]

_Type_: **[General.Currencies](General.Currencies.md)**  
_Supported Filters_: **Equals, EqualsIn**  

_Back-End Default Expression:_  
`obj.PaymentAccount.Currency`

### UserStatus

> The user status of this document if applicable for this document type. null means unknown or not yet set

_Type_: **[General.DocumentTypeUserStatuses](General.DocumentTypeUserStatuses.md) (nullable)**  
_Supported Filters_: **EqualsIn**  



## Business Rules

[!list erp.entity=Finance.Payments.PaymentOrders erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Payments.PaymentOrders erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Finance.Payments.PaymentOrders erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Payments_PaymentOrders?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Payments_PaymentOrders?$top=10>
