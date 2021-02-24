---
uid: Crm.PromotionalPackageLines
---
# Crm.PromotionalPackageLines Entity

Detail records (lines) of promotional package definition. Entity: Crm_Promotional_Package_Lines

Default Display Text Format:  
_{PromotionalPackage.Code}: {PromotionalPackage.Name:T}_  
Default Search Member:  
_PromotionalPackage.Code_  

[Aggregate](xref:aggregates) Parent:  
[Crm.PromotionalPackages](Crm.PromotionalPackages.md)  
[Aggregate](xref:aggregates) Root:  
[Crm.PromotionalPackages](Crm.PromotionalPackages.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.PromotionalPackageLines.md#id) | guid |  
| [LineNumber](Crm.PromotionalPackageLines.md#linenumber) | int32 | Consecutive line number. [Required] 
| [Quantity](Crm.PromotionalPackageLines.md#quantity) | [Quantity](../data-types.md#quantity) | The quantity of the product in the package in the base measurement unit of the Product. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(1)] [Filter(ge;le)] 
| [StandardDiscount<br />AdjustOrReplace](Crm.PromotionalPackageLines.md#standarddiscountadjustorreplace) | [StandardDiscount<br />AdjustOrReplace](Crm.PromotionalPackageLines.md#standarddiscountadjustorreplace) | Specifies standard discount change action: A=ADD, M=Mark down - apply after standard discount; R=REPLACE the standard discount. [Required] [Default("R")] 
| [StandardDiscount<br />PercentAdjust](Crm.PromotionalPackageLines.md#standarddiscountpercentadjust) | decimal | The value of change (in percents) for the standard discount. [Required] [Default(0)] 
| [UnitPrice](Crm.PromotionalPackageLines.md#unitprice) | [Amount](../data-types.md#amount) (nullable) | When not null specifies directly unit price for the product. When null, the package specifies only discount. [Currency: UnitPriceCurrency] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Lot](Crm.PromotionalPackageLines.md#lot) | [Lots](Logistics.Inventory.Lots.md) (nullable) | The Product lot number in the promotional package. [Filter(multi eq)] [Introduced in version 19.1] |
| [Product](Crm.PromotionalPackageLines.md#product) | [Products](General.Products.Products.md) | The product, which is included in the promotional package. [Required] [Filter(multi eq)] |
| [PromotionalPackage](Crm.PromotionalPackageLines.md#promotionalpackage) | [PromotionalPackages](Crm.PromotionalPackages.md) | The [PromotionalPackage](Crm.PromotionalPackageLines.md#promotionalpackage) to which this PromotionalPackageLine belongs. [Required] [Filter(multi eq)] [Owner] |
| [UnitPriceCurrency](Crm.PromotionalPackageLines.md#unitpricecurrency) | [Currencies](General.Currencies.md) (nullable) | Currency of the unit price. null if the package specifies only discount. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LineNumber

Consecutive line number. [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( obj.PromotionalPackage.Lines.Select( c => c.LineNumber).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.PromotionalPackage.Lines.Select( c => c.LineNumber).DefaultIfEmpty( 0).Max( ) + 10)`
### Quantity

The quantity of the product in the package in the base measurement unit of the Product. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(1)] [Filter(ge;le)]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### StandardDiscountAdjustOrReplace

Specifies standard discount change action: A=ADD, M=Mark down - apply after standard discount; R=REPLACE the standard discount. [Required] [Default("R")]

_Type_: **[StandardDiscount<br />AdjustOrReplace](Crm.PromotionalPackageLines.md#standarddiscountadjustorreplace)**  
Allowed values for the [StandardDiscountAdjustOrReplace](Crm.PromotionalPackageLines.md#standarddiscountadjustorreplace) data attribute  
_Allowed Values (Crm.PromotionalPackageLinesRepository.StandardDiscountAdjustOrReplace Enum Members)_  

| Value | Description |
| ---- | --- |
| Add | Add value. Stored as 'A'. <br /> _Database Value:_ 'A' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Add' |
| Replace | Replace value. Stored as 'R'. <br /> _Database Value:_ 'R' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Replace' |
| MarkDown | MarkDown value. Stored as 'M'. <br /> _Database Value:_ 'M' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'MarkDown' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Replace**  

### StandardDiscountPercentAdjust

The value of change (in percents) for the standard discount. [Required] [Default(0)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### UnitPrice

When not null specifies directly unit price for the product. When null, the package specifies only discount. [Currency: UnitPriceCurrency]

_Type_: **[Amount](../data-types.md#amount) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Lot

The Product lot number in the promotional package. [Filter(multi eq)] [Introduced in version 19.1]

_Type_: **[Lots](Logistics.Inventory.Lots.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Product

The product, which is included in the promotional package. [Required] [Filter(multi eq)]

_Type_: **[Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### PromotionalPackage

The [PromotionalPackage](Crm.PromotionalPackageLines.md#promotionalpackage) to which this PromotionalPackageLine belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[PromotionalPackages](Crm.PromotionalPackages.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### UnitPriceCurrency

Currency of the unit price. null if the package specifies only discount. [Filter(multi eq)]

_Type_: **[Currencies](General.Currencies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Crm.PromotionalPackageLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.PromotionalPackageLines erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_PromotionalPackageLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_PromotionalPackageLines?$top=10>

