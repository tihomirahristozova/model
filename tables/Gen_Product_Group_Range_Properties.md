# Table Gen_Product_Group_Range_Properties

When specified for a product group, provides a way for automatical creation of new products, based on altering a set of values of some user-defined properties. Each value combination is used to create a new, unique product within the group. Entity: Gen_Product_Group_Range_Properties

## Owner Tables Hierarchy

* [Gen_Product_Groups](Gen_Product_Groups.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Range_Property_Id](#range_property_id)|`uniqueidentifier` `PK`||
|[Product_Group_Id](#product_group_id)|`uniqueidentifier` ||
|[Property_Id](#property_id)|`uniqueidentifier` |The property whose values will be altered.|
|[Range_Type](#range_type)|`nvarchar(1)` Allowed: `R`, `L`|Specifies the method of the creation of the value set: R - by range from-to; E - by enumeration of all values;|
|[From_Property_Value](#from_property_value)|`nvarchar(254)` |Starting value of the range of alternative values. Used only when Rage Type = R (range).|
|[To_Property_Value](#to_property_value)|`nvarchar(254)` |Ending value of the range of alternative values. Used only when Rage Type = R (range).|
|[Property_Values_List](#property_values_list)|`nvarchar(2147483647)` |Contains the enumeration of all values in the alternating value set. Used only when Rage Type = E (enumeratio).|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Range_Property_Id


Range_Property_Id

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
|Derived From|[Gen_Product_Group_Range_Properties](Gen_Product_Group_Range_Properties.md).[Range_Property_Id](Gen_Product_Group_Range_Properties.md#range_property_id)|
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
|Equals|NULL|no|yes|

### Product_Group_Id


Product_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Gen_Product_Groups](Gen_Product_Groups.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Product_Group_Range_Properties](Gen_Product_Group_Range_Properties.md).[Product_Group_Id](Gen_Product_Group_Range_Properties.md#product_group_id)|
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
|Order|1|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Property_Id


Property_Id


The property whose values will be altered.


The property whose values will be altered.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Properties](Gen_Properties.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Product_Group_Range_Properties](Gen_Product_Group_Range_Properties.md).[Property_Id](Gen_Product_Group_Range_Properties.md#property_id)|
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

### Range_Type


Range_Type


Specifies the method of the creation of the value set: R - by range from-to; E - by enumeration of all values;


Specifies the method of the creation of the value set: R - by range from-to; E - by enumeration of all values;

| Property | Value |
| - | - |
|Type|nvarchar(1)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`R`, `L`|
|Default Value|R|
|Derived From|[Gen_Product_Group_Range_Properties](Gen_Product_Group_Range_Properties.md).[Range_Type](Gen_Product_Group_Range_Properties.md#range_type)|
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
|Max Length|1|
|Order|3|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### From_Property_Value


From_Property_Value


Starting value of the range of alternative values. Used only when Rage Type = R (range).


Starting value of the range of alternative values. Used only when Rage Type = R (range).

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Product_Group_Range_Properties](Gen_Product_Group_Range_Properties.md).[From_Property_Value](Gen_Product_Group_Range_Properties.md#from_property_value)|
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
|Order|4|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### To_Property_Value


To_Property_Value


Ending value of the range of alternative values. Used only when Rage Type = R (range).


Ending value of the range of alternative values. Used only when Rage Type = R (range).

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Product_Group_Range_Properties](Gen_Product_Group_Range_Properties.md).[To_Property_Value](Gen_Product_Group_Range_Properties.md#to_property_value)|
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
|Order|5|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Property_Values_List


Property_Values_List


Contains the enumeration of all values in the alternating value set. Used only when Rage Type = E (enumeratio).


Contains the enumeration of all values in the alternating value set. Used only when Rage Type = E (enumeratio).

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
|Derived From|[Gen_Product_Group_Range_Properties](Gen_Product_Group_Range_Properties.md).[Property_Values_List](Gen_Product_Group_Range_Properties.md#property_values_list)|
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
|Order|6|
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
|Derived From|[Gen_Product_Group_Range_Properties](Gen_Product_Group_Range_Properties.md).[Row_Version](Gen_Product_Group_Range_Properties.md#row_version)|
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


