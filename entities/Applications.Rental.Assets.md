# Applications.Rental.Assets

Contains the rentable assets. Entity: Rent_Assets

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.Rental.Assets.md#Id) | guid |  
| [IsActive](Applications.Rental.Assets.md#IsActive) | boolean | True if the asset is currently active and may be used in new documents. Deactivated assets are used only in reports. [Required] [Default(true)] [Filter(eq)] 
| [Notes](Applications.Rental.Assets.md#Notes) | string (nullable) | Notes for this Asset. 
| [RentalAssetCode](Applications.Rental.Assets.md#RentalAssetCode) | string | Unique rental asset code. [Required] [Filter(eq;like)] [ORD] 
| [RentalAssetName](Applications.Rental.Assets.md#RentalAssetName) | string | The name of the rental asset. [Required] [Filter(like)] 
| [StandardGuaranteeAmount](Applications.Rental.Assets.md#StandardGuaranteeAmount) | [Amount](../data-types/Amount.md) (nullable) | Standard default amount of the guarantee that is set for this asset when leased. [Currency: StandardGuaranteeAmountCurrency] [Filter(multi eq)] 
| [TimePeriodType](Applications.Rental.Assets.md#TimePeriodType) | [Applications.Rental.AssetsRepository.TimePeriodType](Applications.Rental.Assets.md#TimePeriodType) (nullable) | Specifies the unit by which the periods of renting of this asset are measured. Possible values are: 'by days' or 'by months'. [Filter(multi eq)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AccountingAsset](Applications.Rental.Assets.md#AccountingAsset) | [Finance.Assets.Assets](Finance.Assets.Assets.md) (nullable) | When not null identifies the corresponding accounting asset. [Filter(multi eq)] |
| [EnterpriseCompany](Applications.Rental.Assets.md#EnterpriseCompany) | [General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | When not null, specifies that the asset is specific to a given enterprise company and may be used only in documents from this enterprise company. If null, the asset can be used in all enterprise companies. [Filter(multi eq)] |
| [Product](Applications.Rental.Assets.md#Product) | [General.Products.Products](General.Products.Products.md) (nullable) | Product which is used in the store transactions for this asset. [Filter(multi eq)] |
| [RentalAssetGroup](Applications.Rental.Assets.md#RentalAssetGroup) | [Applications.Rental.AssetGroups](Applications.Rental.AssetGroups.md) | The logical group of the rental asset. [Required] [Filter(multi eq)] [Owner] |
| [RentalAssetType](Applications.Rental.Assets.md#RentalAssetType) | [Applications.Rental.AssetTypes](Applications.Rental.AssetTypes.md) | The type of the asset. [Required] [Filter(multi eq)] |
| [SalesProduct](Applications.Rental.Assets.md#SalesProduct) | [General.Products.Products](General.Products.Products.md) (nullable) | Product which is used in the creation of Sales Orders to form the price of the service of renting this asset. [Filter(multi eq)] |
| [SerialNumber](Applications.Rental.Assets.md#SerialNumber) | [Logistics.Inventory.SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable) | Serial number which in conjunction with the product for store operations allows for more accurate identification of the asset. [Filter(multi eq)] |
| [StandardGuaranteeAmountCurrency](Applications.Rental.Assets.md#StandardGuaranteeAmountCurrency) | [General.Currencies](General.Currencies.md) (nullable) | Currency of the standard guarantee amount. [Filter(multi eq)] |
| [WorkSchedule](Applications.Rental.Assets.md#WorkSchedule) | [General.Resources.WorkSchedules](General.Resources.WorkSchedules.md) (nullable) | Work schedule, which is used to calculate how many days this assets has been rented for (used only when the asset's lease by mode is by days). [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Consumables | [Applications.Rental.AssetConsumables](Applications.Rental.AssetConsumables.md) | List of [AssetConsumable](Applications.Rental.AssetConsumables.md) child objects, based on the [Applications.Rental.AssetConsumable.RentalAsset](Applications.Rental.AssetConsumables.md#RentalAsset) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### IsActive

> True if the asset is currently active and may be used in new documents. Deactivated assets are used only in reports. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Notes

> Notes for this Asset.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### RentalAssetCode

> Unique rental asset code. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### RentalAssetName

> The name of the rental asset. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### StandardGuaranteeAmount

> Standard default amount of the guarantee that is set for this asset when leased. [Currency: StandardGuaranteeAmountCurrency] [Filter(multi eq)]

_Type_: **[Amount](../data-types/Amount.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### TimePeriodType

> Specifies the unit by which the periods of renting of this asset are measured. Possible values are: 'by days' or 'by months'. [Filter(multi eq)]

_Type_: **[Applications.Rental.AssetsRepository.TimePeriodType](Applications.Rental.Assets.md#TimePeriodType) (nullable)**  
Allowed values for the [TimePeriodType](Applications.Rental.Assets.md#TimePeriodType) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Days | Days value. Stored as 'D'. <br /> _Database Value:_ 'D' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Days' |
| Months | Months value. Stored as 'M'. <br /> _Database Value:_ 'M' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Months' |

_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  


## Reference Details

### AccountingAsset

> When not null identifies the corresponding accounting asset. [Filter(multi eq)]

_Type_: **[Finance.Assets.Assets](Finance.Assets.Assets.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### EnterpriseCompany

> When not null, specifies that the asset is specific to a given enterprise company and may be used only in documents from this enterprise company. If null, the asset can be used in all enterprise companies. [Filter(multi eq)]

_Type_: **[General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Product

> Product which is used in the store transactions for this asset. [Filter(multi eq)]

_Type_: **[General.Products.Products](General.Products.Products.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### RentalAssetGroup

> The logical group of the rental asset. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Applications.Rental.AssetGroups](Applications.Rental.AssetGroups.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### RentalAssetType

> The type of the asset. [Required] [Filter(multi eq)]

_Type_: **[Applications.Rental.AssetTypes](Applications.Rental.AssetTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### SalesProduct

> Product which is used in the creation of Sales Orders to form the price of the service of renting this asset. [Filter(multi eq)]

_Type_: **[General.Products.Products](General.Products.Products.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### SerialNumber

> Serial number which in conjunction with the product for store operations allows for more accurate identification of the asset. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### StandardGuaranteeAmountCurrency

> Currency of the standard guarantee amount. [Filter(multi eq)]

_Type_: **[General.Currencies](General.Currencies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### WorkSchedule

> Work schedule, which is used to calculate how many days this assets has been rented for (used only when the asset's lease by mode is by days). [Filter(multi eq)]

_Type_: **[General.Resources.WorkSchedules](General.Resources.WorkSchedules.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Applications.Rental.Assets erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Rental.Assets erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.Rental.Assets erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Rental_Assets?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Rental_Assets?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Rent_Assets?$top=10>

