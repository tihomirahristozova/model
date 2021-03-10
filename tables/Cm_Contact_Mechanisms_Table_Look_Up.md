# Query Cm_Contact_Mechanisms_Table_Look_Up


## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`|Unique contact mechanism Id|
|[Contact_Mechanism_Name](#contact_mechanism_name)|`nvarchar` |Contact mechanism description|
|[Contact_Mechanism_Type](#contact_mechanism_type)|`nvarchar` Allowed: `A`, `E`, `F`, `M`, `O`, `T`, `W`|A=Address; E=e-mail; T=Telephone|

## Columns

### Id


Id


Unique contact mechanism Id


Unique contact mechanism Id

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
|Derived From|[Cm_Contact_Mechanisms](Cm_Contact_Mechanisms.md).[Id](Cm_Contact_Mechanisms.md#id)|
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

### Contact_Mechanism_Name


Contact_Mechanism_Name


Contact mechanism description


Contact mechanism description

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
|Derived From|[Cm_Contact_Mechanisms](Cm_Contact_Mechanisms.md).[Contact_Mechanism_Name](Cm_Contact_Mechanisms.md#contact_mechanism_name)|
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
|Equals|NULL|no|yes|
|Like|None|no|no|

### Contact_Mechanism_Type


Contact_Mechanism_Type


A=Address; E=e-mail; T=Telephone


A=Address; E=e-mail; T=Telephone

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
|Allowed Values|`A`, `E`, `F`, `M`, `O`, `T`, `W`|
|Default Value|A|
|Derived From|[Cm_Contact_Mechanisms](Cm_Contact_Mechanisms.md).[Contact_Mechanism_Type](Cm_Contact_Mechanisms.md#contact_mechanism_type)|
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


