# Query Nat_BG_VAT_Declaring_Persons_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Declaring_Person_Id](#declaring_person_id)|`uniqueidentifier` `PK`|Unique identification of the declaring person.|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The enterprise company for which the person is presenting the declaration.|
|[Person_Id](#person_id)|`uniqueidentifier` |The person that is presenting the declaration.|
|[Declarer_Type](#declarer_type)|`nvarchar` Allowed: `A`, `R`|Type of the declaring person. A=Attorney, R=Representative.|
|[Declaring_Person_City](#declaring_person_city)|`nvarchar` |City from the address for correspondation of the declaring person.|
|[Declaring_Person_Postcode](#declaring_person_postcode)|`nvarchar` |Postcode from the address for correspondation of the declaring person.|
|[Declaring_Person_Address](#declaring_person_address)|`nvarchar` |Address for correspondation of the declaring person.|
|[Declaring_Person_Position](#declaring_person_position)|`nvarchar` |Position of the declaring person in the enterprise company.|
|[Is_Default](#is_default)|`bit` |True if this is the default person, which issues VAT declarations for this Enterprise Company.|

## Columns

### Declaring_Person_Id


Declaring_Person_Id


Unique identification of the declaring person.


Unique identification of the declaring person.

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
|Derived From|[Nat_BG_VAT_Declaring_Persons](Nat_BG_VAT_Declaring_Persons.md).[Declaring_Person_Id](Nat_BG_VAT_Declaring_Persons.md#declaring_person_id)|
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

### Enterprise_Company_Id


Enterprise_Company_Id


The enterprise company for which the person is presenting the declaration.


The enterprise company for which the person is presenting the declaration.

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
|Derived From|[Nat_BG_VAT_Declaring_Persons](Nat_BG_VAT_Declaring_Persons.md).[Enterprise_Company_Id](Nat_BG_VAT_Declaring_Persons.md#enterprise_company_id)|
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
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Person_Id


Person_Id


The person that is presenting the declaration.


The person that is presenting the declaration.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Cm_Persons](Cm_Persons.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Nat_BG_VAT_Declaring_Persons](Nat_BG_VAT_Declaring_Persons.md).[Person_Id](Nat_BG_VAT_Declaring_Persons.md#person_id)|
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
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Declarer_Type


Declarer_Type


Type of the declaring person. A=Attorney, R=Representative.


Type of the declaring person. A=Attorney, R=Representative.

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
|Allowed Values|`A`, `R`|
|Default Value|None|
|Derived From|[Nat_BG_VAT_Declaring_Persons](Nat_BG_VAT_Declaring_Persons.md).[Declarer_Type](Nat_BG_VAT_Declaring_Persons.md#declarer_type)|
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

### Declaring_Person_City


Declaring_Person_City


City from the address for correspondation of the declaring person.


City from the address for correspondation of the declaring person.

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
|Derived From|[Nat_BG_VAT_Declaring_Persons](Nat_BG_VAT_Declaring_Persons.md).[Declaring_Person_City](Nat_BG_VAT_Declaring_Persons.md#declaring_person_city)|
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

### Declaring_Person_Postcode


Declaring_Person_Postcode


Postcode from the address for correspondation of the declaring person.


Postcode from the address for correspondation of the declaring person.

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
|Derived From|[Nat_BG_VAT_Declaring_Persons](Nat_BG_VAT_Declaring_Persons.md).[Declaring_Person_Postcode](Nat_BG_VAT_Declaring_Persons.md#declaring_person_postcode)|
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

### Declaring_Person_Address


Declaring_Person_Address


Address for correspondation of the declaring person.


Address for correspondation of the declaring person.

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
|Derived From|[Nat_BG_VAT_Declaring_Persons](Nat_BG_VAT_Declaring_Persons.md).[Declaring_Person_Address](Nat_BG_VAT_Declaring_Persons.md#declaring_person_address)|
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

### Declaring_Person_Position


Declaring_Person_Position


Position of the declaring person in the enterprise company.


Position of the declaring person in the enterprise company.

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
|Derived From|[Nat_BG_VAT_Declaring_Persons](Nat_BG_VAT_Declaring_Persons.md).[Declaring_Person_Position](Nat_BG_VAT_Declaring_Persons.md#declaring_person_position)|
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
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Is_Default


Is_Default


True if this is the default person, which issues VAT declarations for this Enterprise Company.


True if this is the default person, which issues VAT declarations for this Enterprise Company.

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
|Derived From|[Nat_BG_VAT_Declaring_Persons](Nat_BG_VAT_Declaring_Persons.md).[Is_Default](Nat_BG_VAT_Declaring_Persons.md#is_default)|
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


