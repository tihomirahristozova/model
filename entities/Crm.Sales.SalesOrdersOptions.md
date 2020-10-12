---
uid: Crm.Sales.SalesOrdersOptions
---
# Crm.Sales.SalesOrdersOptions Entity

Options for sales orders of specific user defined document type. Entity: Crm_Sales_Orders_Options

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [AllowedDirections](Crm.Sales.SalesOrdersOptions.md#alloweddirections) | [AllowedDirections](Crm.Sales.SalesOrdersOptions.md#alloweddirections) | Allowed directions (return or normal sale) for the sales orders of this document type. 'S' = Normal sale, 'R' = Sales return, '*' = No limit, 'A' = Allow any, but not both (default). [Required] [Default("A")] [Filter(multi eq)] 
| [AvailableQuantityOnly](Crm.Sales.SalesOrdersOptions.md#availablequantityonly) | boolean | When true indicates that the sales order can be released only if there is sufficient available quantity (by ATP). [Required] [Default(false)] [Filter(eq)] 
| [Id](Crm.Sales.SalesOrdersOptions.md#id) | guid |  
| [MinimumAmount](Crm.Sales.SalesOrdersOptions.md#minimumamount) | [Amount](../data-types.md#amount) (nullable) | When not null, specifies minimal total amount of the sales order, which is required for order releasing. [Currency: MinimumAmountCurrency] 
| [ShipmentAllowance](Crm.Sales.SalesOrdersOptions.md#shipmentallowance) | [ShipmentAllowance](Crm.Sales.SalesOrdersOptions.md#shipmentallowance) | Terms on which the shipment of the products in the sales order is allowed. [Required] [Default("A")] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DealDocumentType](Crm.Sales.SalesOrdersOptions.md#dealdocumenttype) | [DocumentTypes](General.DocumentTypes.md) (nullable) | If filled then new opportunities (deals) from the specified type are created automatically by the sales orders that aren't assigned to existing opportunities. [Filter(multi eq)] |
| [DocumentType](Crm.Sales.SalesOrdersOptions.md#documenttype) | [DocumentTypes](General.DocumentTypes.md) | The document type for which the sales order option applies. [Required] [Filter(multi eq)] [Owner] |
| [MinimumAmountCurrency](Crm.Sales.SalesOrdersOptions.md#minimumamountcurrency) | [Currencies](General.Currencies.md) (nullable) | The currency of Minimal Amount. [Filter(multi eq)] |
| [VATDeviationDocument<br />AmountType](Crm.Sales.SalesOrdersOptions.md#vatdeviationdocumentamounttype) | [DocumentAmountTypes](General.DocumentAmountTypes.md) (nullable) | Document amount that contains the difference between the total amount of the sales order formed by unit prices with VAT and the amount formed by unit prices without VAT. [Filter(multi eq)] |


## Attribute Details

### AllowedDirections

Allowed directions (return or normal sale) for the sales orders of this document type. 'S' = Normal sale, 'R' = Sales return, '*' = No limit, 'A' = Allow any, but not both (default). [Required] [Default("A")] [Filter(multi eq)]

_Type_: **[AllowedDirections](Crm.Sales.SalesOrdersOptions.md#alloweddirections)**  
Allowed values for the [AllowedDirections](Crm.Sales.SalesOrdersOptions.md#alloweddirections) data attribute  
_Allowed Values (Crm.Sales.SalesOrdersOptionsRepository.AllowedDirections Enum Members)_  

| Value | Description |
| ---- | --- |
| NormalSale | NormalSale value. Stored as 'S'. <br /> _Database Value:_ 'S' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'NormalSale' |
| SalesReturn | SalesReturn value. Stored as 'R'. <br /> _Database Value:_ 'R' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'SalesReturn' |
| NoLimit | NoLimit value. Stored as '*'. <br /> _Database Value:_ '*' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'NoLimit' |
| AllowAnyButNotBoth | AllowAnyButNotBoth value. Stored as 'A'. <br /> _Database Value:_ 'A' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'AllowAnyButNotBoth' |

_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **AllowAnyButNotBoth**  

### AvailableQuantityOnly

When true indicates that the sales order can be released only if there is sufficient available quantity (by ATP). [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### MinimumAmount

When not null, specifies minimal total amount of the sales order, which is required for order releasing. [Currency: MinimumAmountCurrency]

_Type_: **[Amount](../data-types.md#amount) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ShipmentAllowance

Terms on which the shipment of the products in the sales order is allowed. [Required] [Default("A")]

_Type_: **[ShipmentAllowance](Crm.Sales.SalesOrdersOptions.md#shipmentallowance)**  
Allowed values for the [ShipmentAllowance](Crm.Sales.SalesOrdersOptions.md#shipmentallowance) data attribute  
_Allowed Values (Crm.Sales.SalesOrdersOptionsRepository.ShipmentAllowance Enum Members)_  

| Value | Description |
| ---- | --- |
| AlwaysAllow | AlwaysAllow value. Stored as 'A'. <br /> _Database Value:_ 'A' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'AlwaysAllow' |
| WaitForAnyPayment | WaitForAnyPayment value. Stored as 'P'. <br /> _Database Value:_ 'P' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'WaitForAnyPayment' |
| WaitForFullPayment | WaitForFullPayment value. Stored as 'W'. <br /> _Database Value:_ 'W' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'WaitForFullPayment' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **AlwaysAllow**  


## Reference Details

### DealDocumentType

If filled then new opportunities (deals) from the specified type are created automatically by the sales orders that aren't assigned to existing opportunities. [Filter(multi eq)]

_Type_: **[DocumentTypes](General.DocumentTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### DocumentType

The document type for which the sales order option applies. [Required] [Filter(multi eq)] [Owner]

_Type_: **[DocumentTypes](General.DocumentTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### MinimumAmountCurrency

The currency of Minimal Amount. [Filter(multi eq)]

_Type_: **[Currencies](General.Currencies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### VATDeviationDocumentAmountType

Document amount that contains the difference between the total amount of the sales order formed by unit prices with VAT and the amount formed by unit prices without VAT. [Filter(multi eq)]

_Type_: **[DocumentAmountTypes](General.DocumentAmountTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Crm.Sales.SalesOrdersOptions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.Sales.SalesOrdersOptions erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Sales_SalesOrdersOptions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Sales_SalesOrdersOptions?$top=10>

