# Table Crm_Pricing_Model_Costs

List of costs, associated with a pricing model. Entity: Crm_Pricing_Model_Costs

## Owner Tables Hierarchy

* [Crm_Pricing_Models](Crm_Pricing_Models.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Pricing_Model_Cost_Id](#pricing_model_cost_id)|`uniqueidentifier` `PK`|Pricing Model Cost|
|[Pricing_Model_Id](#pricing_model_id)|`uniqueidentifier` |Pricing model, for which the cost is defined|
|[Line_No](#line_no)|`int` |The consequtive number of the cost within the pricing model|
|[Cost_Type_Id](#cost_type_id)|`uniqueidentifier` |The cost type, which is listed for the pricing model|
|[Amount_Percent](#amount_percent)|`decimal(6, 5)` |Used when the cost is calculated as percent of the amount. NULL when the cost is calculated in a different way|
|[Amount_Per_Unit](#amount_per_unit)|`decimal(9, 2)` |Used when the cost is calculated as amount per unit of the product. The unit is defined in Measurement_Unit_Id. NULL when the cost is calculated in a different way|
|[Measurement_Unit_Id](#measurement_unit_id)|`uniqueidentifier` |The measurement unit for which the Amount_Per_Unit is defined. NULL when the cost is calculated in a different way|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Pricing_Model_Cost_Id


Pricing_Model_Cost_Id


Pricing Model Cost


Pricing Model Cost

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
|Derived From|[Crm_Pricing_Model_Costs](Crm_Pricing_Model_Costs.md).[Pricing_Model_Cost_Id](Crm_Pricing_Model_Costs.md#pricing_model_cost_id)|
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

### Pricing_Model_Id


Pricing_Model_Id


Pricing model, for which the cost is defined


Pricing model, for which the cost is defined

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Crm_Pricing_Models](Crm_Pricing_Models.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Pricing_Model_Costs](Crm_Pricing_Model_Costs.md).[Pricing_Model_Id](Crm_Pricing_Model_Costs.md#pricing_model_id)|
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
|Equals|NULL|no|no|

### Line_No


Line_No


The consequtive number of the cost within the pricing model


The consequtive number of the cost within the pricing model

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Autoincrement|1|
|Derived From|[Crm_Pricing_Model_Costs](Crm_Pricing_Model_Costs.md).[Line_No](Crm_Pricing_Model_Costs.md#line_no)|
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

### Cost_Type_Id


Cost_Type_Id


The cost type, which is listed for the pricing model


The cost type, which is listed for the pricing model

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Cost_Types](Cost_Types.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Pricing_Model_Costs](Crm_Pricing_Model_Costs.md).[Cost_Type_Id](Crm_Pricing_Model_Costs.md#cost_type_id)|
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

### Amount_Percent


Amount_Percent


Used when the cost is calculated as percent of the amount. NULL when the cost is calculated in a different way


Used when the cost is calculated as percent of the amount. NULL when the cost is calculated in a different way

| Property | Value |
| - | - |
|Type|decimal(6, 5)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None, IsPercent|
|Default Value|None|
|Derived From|[Crm_Pricing_Model_Costs](Crm_Pricing_Model_Costs.md).[Amount_Percent](Crm_Pricing_Model_Costs.md#amount_percent)|
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

### Amount_Per_Unit


Amount_Per_Unit


Used when the cost is calculated as amount per unit of the product. The unit is defined in Measurement_Unit_Id. NULL when the cost is calculated in a different way


Used when the cost is calculated as amount per unit of the product. The unit is defined in Measurement_Unit_Id. NULL when the cost is calculated in a different way

| Property | Value |
| - | - |
|Type|decimal(9, 2)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Pricing_Model_Costs](Crm_Pricing_Model_Costs.md).[Amount_Per_Unit](Crm_Pricing_Model_Costs.md#amount_per_unit)|
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

### Measurement_Unit_Id


Measurement_Unit_Id


The measurement unit for which the Amount_Per_Unit is defined. NULL when the cost is calculated in a different way


The measurement unit for which the Amount_Per_Unit is defined. NULL when the cost is calculated in a different way

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Measurement_Units](Gen_Measurement_Units.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Pricing_Model_Costs](Crm_Pricing_Model_Costs.md).[Measurement_Unit_Id](Crm_Pricing_Model_Costs.md#measurement_unit_id)|
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
|Derived From|[Crm_Pricing_Model_Costs](Crm_Pricing_Model_Costs.md).[Row_Version](Crm_Pricing_Model_Costs.md#row_version)|
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


