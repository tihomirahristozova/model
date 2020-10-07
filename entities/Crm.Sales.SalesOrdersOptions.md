# Crm.Sales.SalesOrdersOptions

Options for sales orders of specific user defined document type. Entity: Crm_Sales_Orders_Options

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.Sales.SalesOrdersOptions.md#Id) | guid |  
| [AllowedDirections](Crm.Sales.SalesOrdersOptions.md#AllowedDirections) | [Crm.Sales.SalesOrdersOptionsRepository.AllowedDirections](Crm.Sales.SalesOrdersOptions.md#AllowedDirections) | Allowed directions (return or normal sale) for the sales orders of this document type. 'S' = Normal sale, 'R' = Sales return, '*' = No limit, 'A' = Allow any, but not both (default). [Required] [Default("A")] [Filter(multi eq)] 
| [AvailableQuantityOnly](Crm.Sales.SalesOrdersOptions.md#AvailableQuantityOnly) | boolean | When true indicates that the sales order can be released only if there is sufficient available quantity (by ATP). [Required] [Default(false)] [Filter(eq)] 
| [MinimumAmount](Crm.Sales.SalesOrdersOptions.md#MinimumAmount) | [Amount](../data-types/Amount.md) (nullable) | When not null, specifies minimal total amount of the sales order, which is required for order releasing. [Currency: MinimumAmountCurrency] 
| [ShipmentAllowance](Crm.Sales.SalesOrdersOptions.md#ShipmentAllowance) | [Crm.Sales.SalesOrdersOptionsRepository.ShipmentAllowance](Crm.Sales.SalesOrdersOptions.md#ShipmentAllowance) | Terms on which the shipment of the products in the sales order is allowed. [Required] [Default("A")] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DealDocumentType](Crm.Sales.SalesOrdersOptions.md#DealDocumentType) | [General.DocumentTypes](General.DocumentTypes.md) (nullable) | If filled then new opportunities (deals) from the specified type are created automatically by the sales orders that aren't assigned to existing opportunities. [Filter(multi eq)] |
| [DocumentType](Crm.Sales.SalesOrdersOptions.md#DocumentType) | [General.DocumentTypes](General.DocumentTypes.md) | The document type for which the sales order option applies. [Required] [Filter(multi eq)] [Owner] |
| [MinimumAmountCurrency](Crm.Sales.SalesOrdersOptions.md#MinimumAmountCurrency) | [General.Currencies](General.Currencies.md) (nullable) | The currency of Minimal Amount. [Filter(multi eq)] |
| [VATDeviationDocumentAmountType](Crm.Sales.SalesOrdersOptions.md#VATDeviationDocumentAmountType) | [General.DocumentAmountTypes](General.DocumentAmountTypes.md) (nullable) | Document amount that contains the difference between the total amount of the sales order formed by unit prices with VAT and the amount formed by unit prices without VAT. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### AllowedDirections

> Allowed directions (return or normal sale) for the sales orders of this document type. 'S' = Normal sale, 'R' = Sales return, '*' = No limit, 'A' = Allow any, but not both (default). [Required] [Default("A")] [Filter(multi eq)]

_Type_: **[Crm.Sales.SalesOrdersOptionsRepository.AllowedDirections](Crm.Sales.SalesOrdersOptions.md#AllowedDirections)**  
Allowed values for the [AllowedDirections](Crm.Sales.SalesOrdersOptions.md#AllowedDirections) data attribute  
_Allowed Values (Enum Members)_  

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

> When true indicates that the sales order can be released only if there is sufficient available quantity (by ATP). [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### MinimumAmount

> When not null, specifies minimal total amount of the sales order, which is required for order releasing. [Currency: MinimumAmountCurrency]

_Type_: **[Amount](../data-types/Amount.md) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ShipmentAllowance

> Terms on which the shipment of the products in the sales order is allowed. [Required] [Default("A")]

_Type_: **[Crm.Sales.SalesOrdersOptionsRepository.ShipmentAllowance](Crm.Sales.SalesOrdersOptions.md#ShipmentAllowance)**  
Allowed values for the [ShipmentAllowance](Crm.Sales.SalesOrdersOptions.md#ShipmentAllowance) data attribute  
_Allowed Values (Enum Members)_  

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

> If filled then new opportunities (deals) from the specified type are created automatically by the sales orders that aren't assigned to existing opportunities. [Filter(multi eq)]

_Type_: **[General.DocumentTypes](General.DocumentTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### DocumentType

> The document type for which the sales order option applies. [Required] [Filter(multi eq)] [Owner]

_Type_: **[General.DocumentTypes](General.DocumentTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### MinimumAmountCurrency

> The currency of Minimal Amount. [Filter(multi eq)]

_Type_: **[General.Currencies](General.Currencies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### VATDeviationDocumentAmountType

> Document amount that contains the difference between the total amount of the sales order formed by unit prices with VAT and the amount formed by unit prices without VAT. [Filter(multi eq)]

_Type_: **[General.DocumentAmountTypes](General.DocumentAmountTypes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Crm.Sales.SalesOrdersOptions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.Sales.SalesOrdersOptions erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Crm.Sales.SalesOrdersOptions erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Sales_SalesOrdersOptions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Sales_SalesOrdersOptions?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Sales_Orders_Options?$top=10>

