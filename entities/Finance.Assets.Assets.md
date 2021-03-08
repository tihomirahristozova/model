---
uid: Finance.Assets.Assets
---
# Finance.Assets.Assets Entity

**Namespace:** [Finance.Assets](Finance.Assets.md)  

The fixed assets. Entity: Ast_Assets

## Default Visualization
Default Display Text Format:  
_{Code}: {Name:T}_  
Default Search Member:  
_Code_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.EnterpriseCompanies](General.EnterpriseCompanies.md)  
Aggregate Root:  
[General.EnterpriseCompanies](General.EnterpriseCompanies.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Finance.Assets.Assets.md#code) | string | The unique code of the Asset. `Required` `Filter(eq;like)` `ORD` 
| [DeploymentDate](Finance.Assets.Assets.md#deploymentdate) | datetime (nullable) | Date, when the asset is first deployed. Null if the asset is not deployed yet. 
| [Id](Finance.Assets.Assets.md#id) | guid |  
| [IsActive](Finance.Assets.Assets.md#isactive) | boolean | Checked if the assets is active and can be used in documents. The inactive assets can be used only for reports. `Required` `Default(true)` `Filter(eq)` 
| [Name](Finance.Assets.Assets.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | The name of this Asset. `Required` `Filter(like)` 
| [Notes](Finance.Assets.Assets.md#notes) | string (nullable) | Notes for this Asset. 
| [PurchaseDate](Finance.Assets.Assets.md#purchasedate) | datetime | Original purchase date of the asset. `Required` 
| [SerialNumber](Finance.Assets.Assets.md#serialnumber) | string (nullable) | Serial number of the asset. `Filter(eq)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AssetCategory](Finance.Assets.Assets.md#assetcategory) | [AssetCategories](Finance.Assets.AssetCategories.md) | The category of this asset. The category may determine default values for the depreciation plans for the different valuation models for this asset. `Required` `Filter(multi eq)` |
| [AssetGroup](Finance.Assets.Assets.md#assetgroup) | [AssetGroups](Finance.Assets.AssetGroups.md) (nullable) | The asset group to which this asset belongs. `Filter(multi eq)` |
| [EnterpriseCompany](Finance.Assets.Assets.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) | The Enterprise Company to which this Asset applies. `Required` `Filter(multi eq)` `Owner` |
| [PrimaryValuationModel](Finance.Assets.Assets.md#primaryvaluationmodel) | [ValuationModels](Finance.Assets.ValuationModels.md) | Obsolete. Not used. `Required` `Filter(multi eq)` |
| [ValuationCurrency](Finance.Assets.Assets.md#valuationcurrency) | [Currencies](General.Currencies.md) | Currency in which changes of the asset values (purchase value, depreciation value and etc.) are stored. `Required` `Filter(multi eq)` |


## Attribute Details

### Code

The unique code of the Asset. `Required` `Filter(eq;like)` `ORD`

_Type_: **string**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### DeploymentDate

Date, when the asset is first deployed. Null if the asset is not deployed yet.

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

Checked if the assets is active and can be used in documents. The inactive assets can be used only for reports. `Required` `Default(true)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Name

The name of this Asset. `Required` `Filter(like)`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Notes

Notes for this Asset.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PurchaseDate

Original purchase date of the asset. `Required`

_Type_: **datetime**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### SerialNumber

Serial number of the asset. `Filter(eq)`

_Type_: **string (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  


## Reference Details

### AssetCategory

The category of this asset. The category may determine default values for the depreciation plans for the different valuation models for this asset. `Required` `Filter(multi eq)`

_Type_: **[AssetCategories](Finance.Assets.AssetCategories.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### AssetGroup

The asset group to which this asset belongs. `Filter(multi eq)`

_Type_: **[AssetGroups](Finance.Assets.AssetGroups.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### EnterpriseCompany

The Enterprise Company to which this Asset applies. `Required` `Filter(multi eq)` `Owner`

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### PrimaryValuationModel

Obsolete. Not used. `Required` `Filter(multi eq)`

_Type_: **[ValuationModels](Finance.Assets.ValuationModels.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ValuationCurrency

Currency in which changes of the asset values (purchase value, depreciation value and etc.) are stored. `Required` `Filter(multi eq)`

_Type_: **[Currencies](General.Currencies.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Finance.Assets.Assets erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Assets.Assets erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Assets_Assets?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Assets_Assets?$top=10>

