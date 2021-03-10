# Table Fleet_Maintenance_Plans

Defines the periodic maintenance plans and the conditions for performing the next maintenance. Entity: Fleet_Maintenance_Plans

## Summary

| Name | Type | Description |
| - | - | --- |
|[Maintenance_Plan_Id](#maintenance_plan_id)|`uniqueidentifier` `PK`||
|[Maintenance_Plan_Code](#maintenance_plan_code)|`nvarchar(16)` ||
|[Maintenance_Plan_Name](#maintenance_plan_name)|`nvarchar(254)` |Maintenance plan name (Multilanguage).|
|[Check_Months](#check_months)|`int` |When not null, specifies the number of months between maintenances.|
|[Check_Days](#check_days)|`int` |When not null, specifies the number of days between maintenances.|
|[Mileage_Km](#mileage_km)|`int` |When not null, specifies the number of kilometers that must have passed since the last maintenance, for the next maintenance to occur.|
|[Trip_Count](#trip_count)|`int` |When not null, specifies the number of trips that must be performed since the last maintenance, for the next maintenance to occur.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Is_Active](#is_active)|`bit` |True if the plan is active and can be selected from drop-downs.|

## Columns

### Maintenance_Plan_Id


Maintenance_Plan_Id

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
|Derived From|[Fleet_Maintenance_Plans](Fleet_Maintenance_Plans.md).[Maintenance_Plan_Id](Fleet_Maintenance_Plans.md#maintenance_plan_id)|
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

### Maintenance_Plan_Code


Maintenance_Plan_Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Maintenance_Plans](Fleet_Maintenance_Plans.md).[Maintenance_Plan_Code](Fleet_Maintenance_Plans.md#maintenance_plan_code)|
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
|Max Length|16|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Maintenance_Plan_Name


Maintenance_Plan_Name


Maintenance plan name (Multilanguage).


Maintenance plan name (Multilanguage).

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Maintenance_Plans](Fleet_Maintenance_Plans.md).[Maintenance_Plan_Name](Fleet_Maintenance_Plans.md#maintenance_plan_name)|
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
|Max Length|254|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Check_Months


Check_Months


When not null, specifies the number of months between maintenances.


When not null, specifies the number of months between maintenances.

| Property | Value |
| - | - |
|Type|int|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Maintenance_Plans](Fleet_Maintenance_Plans.md).[Check_Months](Fleet_Maintenance_Plans.md#check_months)|
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

### Check_Days


Check_Days


When not null, specifies the number of days between maintenances.


When not null, specifies the number of days between maintenances.

| Property | Value |
| - | - |
|Type|int|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Maintenance_Plans](Fleet_Maintenance_Plans.md).[Check_Days](Fleet_Maintenance_Plans.md#check_days)|
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

### Mileage_Km


Mileage_Km


When not null, specifies the number of kilometers that must have passed since the last maintenance, for the next maintenance to occur.


When not null, specifies the number of kilometers that must have passed since the last maintenance, for the next maintenance to occur.

| Property | Value |
| - | - |
|Type|int|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Maintenance_Plans](Fleet_Maintenance_Plans.md).[Mileage_Km](Fleet_Maintenance_Plans.md#mileage_km)|
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

### Trip_Count


Trip_Count


When not null, specifies the number of trips that must be performed since the last maintenance, for the next maintenance to occur.


When not null, specifies the number of trips that must be performed since the last maintenance, for the next maintenance to occur.

| Property | Value |
| - | - |
|Type|int|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Maintenance_Plans](Fleet_Maintenance_Plans.md).[Trip_Count](Fleet_Maintenance_Plans.md#trip_count)|
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

### Notes


Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Maintenance_Plans](Fleet_Maintenance_Plans.md).[Notes](Fleet_Maintenance_Plans.md#notes)|
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
|Max Length|2147483647|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Is_Active


Is_Active


True if the plan is active and can be selected from drop-downs.


True if the plan is active and can be selected from drop-downs.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|True|
|Derived From|[Fleet_Maintenance_Plans](Fleet_Maintenance_Plans.md).[Is_Active](Fleet_Maintenance_Plans.md#is_active)|
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


