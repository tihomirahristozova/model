# Query Gen_Resource_Cost_Rates_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Resource_Cost_Rate_Id](#resource_cost_rate_id)|`uniqueidentifier` `PK`||
|[Resource_Id](#resource_id)|`uniqueidentifier` |The resource for which the cost rate is defined.|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The enterprise company for which the cost is defined.|
|[From_Date](#from_date)|`date` |Starting date of validity of the cost rate. The rate is valid until the next cost rate record with later date is defined.|
|[Standard_Rate_Per_Hour](#standard_rate_per_hour)|`decimal(12, 4)` |The standard cost per hour of the resource in the resources costing currency. The standard cost is applied for resource usage during the normal working hours.|
|[Overtime_Rate_Per_Hour](#overtime_rate_per_hour)|`decimal(12, 4)` |The overtime cost of the resource per hour in the resources costing currency. The overtime rate specifies the cost of the resource, when it is used outside the normal working schedule. NULL means that there is no special overtime rate and the standard rate should be applied.|
|[Per_Use_Cost](#per_use_cost)|`decimal(12, 2)` |One-time cost for each usage of the resource in the resources costing currency.|
|[Notes](#notes)|`nvarchar` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Resource_Cost_Rate_Id


Resource_Cost_Rate_Id

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
|Derived From|[Gen_Resource_Cost_Rates](Gen_Resource_Cost_Rates.md).[Resource_Cost_Rate_Id](Gen_Resource_Cost_Rates.md#resource_cost_rate_id)|
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
|Order|0|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Resource_Id


Resource_Id


The resource for which the cost rate is defined.


The resource for which the cost rate is defined.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Resources](Gen_Resources.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Resource_Cost_Rates](Gen_Resource_Cost_Rates.md).[Resource_Id](Gen_Resource_Cost_Rates.md#resource_id)|
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
|Order|1|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Enterprise_Company_Id


Enterprise_Company_Id


The enterprise company for which the cost is defined.


The enterprise company for which the cost is defined.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Enterprise_Companies](Gen_Enterprise_Companies.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Resource_Cost_Rates](Gen_Resource_Cost_Rates.md).[Enterprise_Company_Id](Gen_Resource_Cost_Rates.md#enterprise_company_id)|
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
|Order|2|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### From_Date


From_Date


Starting date of validity of the cost rate. The rate is valid until the next cost rate record with later date is defined.


Starting date of validity of the cost rate. The rate is valid until the next cost rate record with later date is defined.

| Property | Value |
| - | - |
|Type|date|
|DateTime Format|Date|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Resource_Cost_Rates](Gen_Resource_Cost_Rates.md).[From_Date](Gen_Resource_Cost_Rates.md#from_date)|
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
|Order|3|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|GreaterThanOrLessThan|None|no|no|

### Standard_Rate_Per_Hour


Standard_Rate_Per_Hour


The standard cost per hour of the resource in the resources costing currency. The standard cost is applied for resource usage during the normal working hours.


The standard cost per hour of the resource in the resources costing currency. The standard cost is applied for resource usage during the normal working hours.

| Property | Value |
| - | - |
|Type|decimal(12, 4)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Resource_Cost_Rates](Gen_Resource_Cost_Rates.md).[Standard_Rate_Per_Hour](Gen_Resource_Cost_Rates.md#standard_rate_per_hour)|
|Format|N2|
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
|Order|4|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|Like|None|no|no|

### Overtime_Rate_Per_Hour


Overtime_Rate_Per_Hour


The overtime cost of the resource per hour in the resources costing currency. The overtime rate specifies the cost of the resource, when it is used outside the normal working schedule. NULL means that there is no special overtime rate and the standard rate should be applied.


The overtime cost of the resource per hour in the resources costing currency. The overtime rate specifies the cost of the resource, when it is used outside the normal working schedule. NULL means that there is no special overtime rate and the standard rate should be applied.

| Property | Value |
| - | - |
|Type|decimal(12, 4)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Resource_Cost_Rates](Gen_Resource_Cost_Rates.md).[Overtime_Rate_Per_Hour](Gen_Resource_Cost_Rates.md#overtime_rate_per_hour)|
|Format|N2|
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
|Order|5|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|Like|None|no|no|

### Per_Use_Cost


Per_Use_Cost


One-time cost for each usage of the resource in the resources costing currency.


One-time cost for each usage of the resource in the resources costing currency.

| Property | Value |
| - | - |
|Type|decimal(12, 2)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Gen_Resource_Cost_Rates](Gen_Resource_Cost_Rates.md).[Per_Use_Cost](Gen_Resource_Cost_Rates.md#per_use_cost)|
|Format|N2|
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
|Order|6|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|Like|None|no|no|

### Notes


Notes

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Resource_Cost_Rates](Gen_Resource_Cost_Rates.md).[Notes](Gen_Resource_Cost_Rates.md#notes)|
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
|Order|7|
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
|Derived From|[Gen_Resource_Cost_Rates](Gen_Resource_Cost_Rates.md).[Row_Version](Gen_Resource_Cost_Rates.md#row_version)|
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
|Order|8|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|


