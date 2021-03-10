# Table Prd_Resources

Resource types available to production. Entity: Prd_Resources

## Owner Tables Hierarchy

* [Prd_Resource_Groups](Prd_Resource_Groups.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`|Unique resource id|
|[Resource_Group_Id](#resource_group_id)|`uniqueidentifier` |The Id of the containing resource group|
|[Resource_Name](#resource_name)|`nvarchar(64)` |Name of the resource|
|[Primary_Unit_Id](#primary_unit_id)|`uniqueidentifier` |Primary measurement unit for quantities of the resource|
|[Setup_Scrap_Quantity](#setup_scrap_quantity)|`decimal(18, 3)` |The usual quantity of fixed scrap occurring when changing production. |
|[Setup_Scrap_Unit](#setup_scrap_unit)|`uniqueidentifier` |The measurement units of Setup_Scrap_Quantity|
|[Setup_Duration_Hours](#setup_duration_hours)|`decimal(6, 2)` |The usual duration of setup when changing production|
|[Notes](#notes)|`nvarchar(254)` |User notes for the resource|
|[Standard_Price_Per_Hour](#standard_price_per_hour)|`decimal(18, 6)` |Standard price per hour for this resource. It participates in the calculation of standard price for production recipes in which the current resource is used.|
|[Resource_Currency_Id](#resource_currency_id)|`uniqueidentifier` |Currency for this resource. This currency applies for the standard price and cost per hour.|
|[Standard_Cost_Per_Hour](#standard_cost_per_hour)|`decimal(18, 6)` |Standard cost per hour for this resource. It participates in the calculation of standard cost for production recipes in which the current resource is used.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Id


Id


Unique resource id


Unique resource id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|yes|
|Order in Primary Key|1|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|NewGuid|
|Derived From|[Prd_Resources](Prd_Resources.md).[Id](Prd_Resources.md#id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Resource_Group_Id


Resource_Group_Id


The Id of the containing resource group


The Id of the containing resource group

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Prd_Resource_Groups](Prd_Resource_Groups.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Resources](Prd_Resources.md).[Resource_Group_Id](Prd_Resources.md#resource_group_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Resource_Name


Resource_Name


Name of the resource


Name of the resource

| Property | Value |
| - | - |
|Type|nvarchar(64)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Resources](Prd_Resources.md).[Resource_Name](Prd_Resources.md#resource_name)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|64|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Like|None|no|no|

### Primary_Unit_Id


Primary_Unit_Id


Primary measurement unit for quantities of the resource


Primary measurement unit for quantities of the resource

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Measurement_Units](Gen_Measurement_Units.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Resources](Prd_Resources.md).[Primary_Unit_Id](Prd_Resources.md#primary_unit_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Setup_Scrap_Quantity


Setup_Scrap_Quantity


The usual quantity of fixed scrap occurring when changing production. 


The usual quantity of fixed scrap occurring when changing production. 

| Property | Value |
| - | - |
|Type|decimal(18, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Prd_Resources](Prd_Resources.md).[Setup_Scrap_Quantity](Prd_Resources.md#setup_scrap_quantity)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|no|

### Setup_Scrap_Unit


Setup_Scrap_Unit


The measurement units of Setup_Scrap_Quantity


The measurement units of Setup_Scrap_Quantity

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Measurement_Units](Gen_Measurement_Units.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Resources](Prd_Resources.md).[Setup_Scrap_Unit](Prd_Resources.md#setup_scrap_unit)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Setup_Duration_Hours


Setup_Duration_Hours


The usual duration of setup when changing production


The usual duration of setup when changing production

| Property | Value |
| - | - |
|Type|decimal(6, 2)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Prd_Resources](Prd_Resources.md).[Setup_Duration_Hours](Prd_Resources.md#setup_duration_hours)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|no|

### Notes


Notes


User notes for the resource


User notes for the resource

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None, IsLongString|
|Default Value|None|
|Derived From|[Prd_Resources](Prd_Resources.md).[Notes](Prd_Resources.md#notes)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|254|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

### Standard_Price_Per_Hour


Standard_Price_Per_Hour


Standard price per hour for this resource. It participates in the calculation of standard price for production recipes in which the current resource is used.


Standard price per hour for this resource. It participates in the calculation of standard price for production recipes in which the current resource is used.

| Property | Value |
| - | - |
|Type|decimal(18, 6)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Resources](Prd_Resources.md).[Standard_Price_Per_Hour](Prd_Resources.md#standard_price_per_hour)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Resource_Currency_Id


Resource_Currency_Id


Currency for this resource. This currency applies for the standard price and cost per hour.


Currency for this resource. This currency applies for the standard price and cost per hour.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Currencies](Gen_Currencies.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Resources](Prd_Resources.md).[Resource_Currency_Id](Prd_Resources.md#resource_currency_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Standard_Cost_Per_Hour


Standard_Cost_Per_Hour


Standard cost per hour for this resource. It participates in the calculation of standard cost for production recipes in which the current resource is used.


Standard cost per hour for this resource. It participates in the calculation of standard cost for production recipes in which the current resource is used.

| Property | Value |
| - | - |
|Type|decimal(18, 6)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Resources](Prd_Resources.md).[Standard_Cost_Per_Hour](Prd_Resources.md#standard_cost_per_hour)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Row_Version


Row_Version

| Property | Value |
| - | - |
|Type|timestamp|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Resources](Prd_Resources.md).[Row_Version](Prd_Resources.md#row_version)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|


