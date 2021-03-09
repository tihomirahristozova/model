# Table Ast_Assets

The fixed assets. Entity: Ast_Assets

## Owner Tables Hierarchy

* [Gen_Enterprise_Companies](Gen_Enterprise_Companies.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Asset_Id](#asset_id)|`uniqueidentifier` `PK`||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Asset_Group_Id](#asset_group_id)|`uniqueidentifier` |The asset group to which this asset belongs.|
|[Asset_Category_Id](#asset_category_id)|`uniqueidentifier` |The category of this asset. The category may determine default values for the depreciation plans for the different valuation models for this asset.|
|[Asset_Code](#asset_code)|`nvarchar(20)` ||
|[Asset_Name](#asset_name)|`nvarchar(254)` `ML`||
|[Serial_Number](#serial_number)|`nvarchar(30)` |Serial number of the asset.|
|[Primary_Valuation_Model_Id](#primary_valuation_model_id)|`uniqueidentifier` |Obsolete. Not used.|
|[Valuation_Currency_Id](#valuation_currency_id)|`uniqueidentifier` |Currency in which changes of the asset values (purchase value, depreciation value and etc.) are stored.|
|[Purchase_Date](#purchase_date)|`datetime` |Original purchase date of the asset.|
|[Notes](#notes)|`nvarchar(254)` ||
|[Deployment_Date](#deployment_date)|`datetime` |Date, when the asset is first deployed. Null if the asset is not deployed yet|
|[Is_Active](#is_active)|`bit` |Checked if the assets is active and can be used in documents. The inactive assets can be used only for reports.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Asset_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Asset_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Asset_Category_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Asset_Code

| Property | Value |
| - | - |
|Type|nvarchar(20)|

### Asset_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Serial_Number

| Property | Value |
| - | - |
|Type|nvarchar(30)|

### Primary_Valuation_Model_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Valuation_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Purchase_Date

| Property | Value |
| - | - |
|Type|datetime|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Deployment_Date

| Property | Value |
| - | - |
|Type|datetime|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


