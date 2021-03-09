# Table VAT_Deal_Types

Contains deal types supported by the system as well as user-defined types. Entity: VAT_Deal_Types

## Summary

| Name | Type | Description |
| - | - | --- |
|[Deal_Type_Id](#deal_type_id)|`uniqueidentifier` `PK`|Unique Id for the deal type. Deal_Type_Id should be used for identifyind and updating system deal types.|
|[Deal_Type_Name](#deal_type_name)|`nvarchar(254)` |Description of the deal type.|
|[Entry_Type](#entry_type)|`nvarchar(1)` Allowed: `P`, `S`|Type of the VAT entries, which are made for this deal type. S=Sales, P=Purchases.|
|[Country_Id](#country_id)|`uniqueidentifier` |The country for which this deal type applies. The country is matched against the country of the enterprise company.|
|[Is_System](#is_system)|`bit` Readonly|Is_System is True for those deal types that are managed by the system via update procedures and cannot be edited by the user.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Deal_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Deal_Type_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Entry_Type

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Country_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Is_System

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


