# Query VAT_Deal_Types_Table_Look_Up


## Summary

| Name | Type | Description |
| - | - | --- |
|[Deal_Type_Id](#deal_type_id)|`uniqueidentifier` `PK`|Unique Id for the deal type. Deal_Type_Id should be used for identifyind and updating system deal types.|
|[Deal_Type_Name](#deal_type_name)|`nvarchar` |Description of the deal type.|
|[Entry_Type](#entry_type)|`nvarchar` Allowed: `P`, `S`|Type of the VAT entries, which are made for this deal type. S=Sales, P=Purchases.|

## Columns

### Deal_Type_Id


Deal_Type_Id


Unique Id for the deal type. Deal_Type_Id should be used for identifyind and updating system deal types.


Unique Id for the deal type. Deal_Type_Id should be used for identifyind and updating system deal types.

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
|Derived From|[VAT_Deal_Types](VAT_Deal_Types.md).[Deal_Type_Id](VAT_Deal_Types.md#deal_type_id)|
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
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Deal_Type_Name


Deal_Type_Name


Description of the deal type.


Description of the deal type.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[VAT_Deal_Types](VAT_Deal_Types.md).[Deal_Type_Name](VAT_Deal_Types.md#deal_type_name)|
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
|UI Width|Long|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|Like|None|no|no|

### Entry_Type


Entry_Type


Type of the VAT entries, which are made for this deal type. S=Sales, P=Purchases.


Type of the VAT entries, which are made for this deal type. S=Sales, P=Purchases.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`P`, `S`|
|Default Value|None|
|Derived From|[VAT_Deal_Types](VAT_Deal_Types.md).[Entry_Type](VAT_Deal_Types.md#entry_type)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|


