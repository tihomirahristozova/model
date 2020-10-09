---
uid: Logistics.Inventory.CurrentBalances
---
# Logistics.Inventory.CurrentBalances

The current inventory balances, grouped by storage key (Store, Product, Lot, etc.). Entity: Inv_Current_Balances

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [BaseCost](Logistics.Inventory.CurrentBalances.md#basecost) | [Amount](../data-types.md#amount) | The cost of the inventory in base currency of the enterprise company. [Currency: EnterpriseCompany.BaseCurrency] [Required] [Filter(ge;le)] 
| [ProductCost](Logistics.Inventory.CurrentBalances.md#productcost) | [Amount](../data-types.md#amount) | The cost of the inventory in the products currency. [Currency: Product.CostingCurrency] [Required] 
| [QuantityBase](Logistics.Inventory.CurrentBalances.md#quantitybase) | [Quantity](../data-types.md#quantity) | The quantity of the stock received/issued in base measurement unit. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Filter(ge;le)] [ReadOnly] 
| [StoreCost](Logistics.Inventory.CurrentBalances.md#storecost) | [Amount](../data-types.md#amount) | The cost of the inventory in the stores currency. [Currency: Store.Currency] [Required] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](Logistics.Inventory.CurrentBalances.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company which issued the document. [Required] [Filter(multi eq)] |
| [Lot](Logistics.Inventory.CurrentBalances.md#lot) | [Lots](Logistics.Inventory.Lots.md) (nullable) | If non-null, contains the specific lot to use for the movement. [Filter(multi eq)] |
| [Product](Logistics.Inventory.CurrentBalances.md#product) | [Products](General.Products.Products.md) | The item that was received/issued. [Required] [Filter(multi eq)] |
| [ProductVariant](Logistics.Inventory.CurrentBalances.md#productvariant) | [ProductVariants](General.ProductVariants.md) (nullable) | If specified determines which product variant of the current product in this line is used. [Filter(multi eq)] |
| [SerialNumber](Logistics.Inventory.CurrentBalances.md#serialnumber) | [SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable) | Item serial number for serialized items. null for non-serialized items. [Filter(multi eq)] |
| [Store](Logistics.Inventory.CurrentBalances.md#store) | [Stores](Logistics.Inventory.Stores.md) | The store from which the goods are received or issued. [Required] [Filter(multi eq)] |
| [StoreBin](Logistics.Inventory.CurrentBalances.md#storebin) | [StoreBins](Logistics.Inventory.StoreBins.md) (nullable) | Store bin, from/to which the transaction was performed. [Filter(multi eq)] |


## Attribute Details

### BaseCost

> The cost of the inventory in base currency of the enterprise company. [Currency: EnterpriseCompany.BaseCurrency] [Required] [Filter(ge;le)]

_Type_: **[Amount](../data-types.md#amount)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### ProductCost

> The cost of the inventory in the products currency. [Currency: Product.CostingCurrency] [Required]

_Type_: **[Amount](../data-types.md#amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### QuantityBase

> The quantity of the stock received/issued in base measurement unit. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Filter(ge;le)] [ReadOnly]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### StoreCost

> The cost of the inventory in the stores currency. [Currency: Store.Currency] [Required]

_Type_: **[Amount](../data-types.md#amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### EnterpriseCompany

> The enterprise company which issued the document. [Required] [Filter(multi eq)]

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Lot

> If non-null, contains the specific lot to use for the movement. [Filter(multi eq)]

_Type_: **[Lots](Logistics.Inventory.Lots.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Product

> The item that was received/issued. [Required] [Filter(multi eq)]

_Type_: **[Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ProductVariant

> If specified determines which product variant of the current product in this line is used. [Filter(multi eq)]

_Type_: **[ProductVariants](General.ProductVariants.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### SerialNumber

> Item serial number for serialized items. null for non-serialized items. [Filter(multi eq)]

_Type_: **[SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Store

> The store from which the goods are received or issued. [Required] [Filter(multi eq)]

_Type_: **[Stores](Logistics.Inventory.Stores.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### StoreBin

> Store bin, from/to which the transaction was performed. [Filter(multi eq)]

_Type_: **[StoreBins](Logistics.Inventory.StoreBins.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Logistics.Inventory.CurrentBalances erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Inventory.CurrentBalances erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Inventory.CurrentBalances erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Inventory_CurrentBalances?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Inventory_CurrentBalances?$top=10>

