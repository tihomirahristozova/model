# Table Crm_Sales_Persons

Sales persons (or representatives) are sellers inside the enterprise company who sell the products to customers. Entity: Crm_Sales_Persons

## Owner Tables Hierarchy

* [Cm_Persons](Cm_Persons.md)
* [Gen_Parties](Gen_Parties.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Sales_Person_Id](#sales_person_id)|`uniqueidentifier` `PK`|Unique sales person Id|
|[Person_Id](#person_id)|`uniqueidentifier` |Base personal record|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Commission_Policy_Id](#commission_policy_id)|`uniqueidentifier` |Current commission policy for the sales person. NULL means there is no commission policy|
|[Commission_Percent](#commission_percent)|`decimal(7, 6)` |The percentage (0..1) of commission percent. NULL means that there is no commission percent.|
|[Sales_Person_Group_Id](#sales_person_group_id)|`uniqueidentifier` |The sales person group to which this sales person is assigned.|
|[Contract_Start_Date](#contract_start_date)|`datetime` |The starting date of the contract with the sales person. NULL when it is unknown.|
|[Contract_End_Date](#contract_end_date)|`datetime` |The ending date of the contract with the sales person. NULL when the sales person is still active.|
|[Enterprise_Company_Location_Id](#enterprise_company_location_id)|`uniqueidentifier` |The enterprise company location, to which the sales person is assigned. The sales person is allowed to sell to other locations, but this is the default location. NULL means that the sales person is not assigned to any enterprise location.|
|[Is_Active](#is_active)|`bit` |Specifies whether the sales person is active and should be included in the list when choosing sales person through drop-downs, lists, etc.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Sales_Person_Id


Sales_Person_Id


Unique sales person Id


Unique sales person Id

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
|Derived From|[Crm_Sales_Persons](Crm_Sales_Persons.md).[Sales_Person_Id](Crm_Sales_Persons.md#sales_person_id)|
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

### Person_Id


Person_Id


Base personal record


Base personal record

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Cm_Persons](Cm_Persons.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Persons](Crm_Sales_Persons.md).[Person_Id](Crm_Sales_Persons.md#person_id)|
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
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Enterprise_Company_Id


Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Enterprise_Companies](Gen_Enterprise_Companies.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Persons](Crm_Sales_Persons.md).[Enterprise_Company_Id](Crm_Sales_Persons.md#enterprise_company_id)|
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
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Commission_Policy_Id


Commission_Policy_Id


Current commission policy for the sales person. NULL means there is no commission policy


Current commission policy for the sales person. NULL means there is no commission policy

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Persons](Crm_Sales_Persons.md).[Commission_Policy_Id](Crm_Sales_Persons.md#commission_policy_id)|
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
|Equals|NULL|yes|no|

### Commission_Percent


Commission_Percent


The percentage (0..1) of commission percent. NULL means that there is no commission percent.


The percentage (0..1) of commission percent. NULL means that there is no commission percent.

| Property | Value |
| - | - |
|Type|decimal(7, 6)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None, IsPercent|
|Default Value|None|
|Derived From|[Crm_Sales_Persons](Crm_Sales_Persons.md).[Commission_Percent](Crm_Sales_Persons.md#commission_percent)|
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
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|no|

### Sales_Person_Group_Id


Sales_Person_Group_Id


The sales person group to which this sales person is assigned.


The sales person group to which this sales person is assigned.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Crm_Sales_Person_Groups](Crm_Sales_Person_Groups.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Persons](Crm_Sales_Persons.md).[Sales_Person_Group_Id](Crm_Sales_Persons.md#sales_person_group_id)|
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

### Contract_Start_Date


Contract_Start_Date


The starting date of the contract with the sales person. NULL when it is unknown.


The starting date of the contract with the sales person. NULL when it is unknown.

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Persons](Crm_Sales_Persons.md).[Contract_Start_Date](Crm_Sales_Persons.md#contract_start_date)|
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
|GreaterThanOrLessThan|None|yes|no|

### Contract_End_Date


Contract_End_Date


The ending date of the contract with the sales person. NULL when the sales person is still active.


The ending date of the contract with the sales person. NULL when the sales person is still active.

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Persons](Crm_Sales_Persons.md).[Contract_End_Date](Crm_Sales_Persons.md#contract_end_date)|
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
|GreaterThanOrLessThan|None|yes|no|

### Enterprise_Company_Location_Id


Enterprise_Company_Location_Id


The enterprise company location, to which the sales person is assigned. The sales person is allowed to sell to other locations, but this is the default location. NULL means that the sales person is not assigned to any enterprise location.


The enterprise company location, to which the sales person is assigned. The sales person is allowed to sell to other locations, but this is the default location. NULL means that the sales person is not assigned to any enterprise location.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Cm_Company_Locations](Cm_Company_Locations.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Persons](Crm_Sales_Persons.md).[Enterprise_Company_Location_Id](Crm_Sales_Persons.md#enterprise_company_location_id)|
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

### Is_Active


Is_Active


Specifies whether the sales person is active and should be included in the list when choosing sales person through drop-downs, lists, etc.


Specifies whether the sales person is active and should be included in the list when choosing sales person through drop-downs, lists, etc.

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
|Derived From|[Crm_Sales_Persons](Crm_Sales_Persons.md).[Is_Active](Crm_Sales_Persons.md#is_active)|
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
|Derived From|[Crm_Sales_Persons](Crm_Sales_Persons.md).[Row_Version](Crm_Sales_Persons.md#row_version)|
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


