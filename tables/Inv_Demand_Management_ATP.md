# View Inv_Demand_Management_ATP

Quantities available to promise for the different date periods. Also contains the current and projected availability. Entity: Inv_Demand_Management_ATP

## Summary

| Name | Type | Description |
| - | - | --- |
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |Тhe Enterprise Company, for which the quantities are calculated.|
|[Store_Id](#store_id)|`uniqueidentifier` |The Store, for which the quantities are calculated.|
|[Product_Id](#product_id)|`uniqueidentifier` |The Product, for which the quantities are calculated.|
|[From_Date](#from_date)|`datetime` |Тhe date from which the available to promise quantity is valid.|
|[Movements_Base](#movements_base)|`decimal(38, 3)` |The sum of the quantity of all planned stock movements on this date in а base measurement unit. |
|[Movements_To_Date_Base](#movements_to_date_base)|`decimal(38, 3)` |The sum of the quantity of all planned stock movements until this date (inclusive) in а base measurement unit. The value is cumulative.|
|[Current_Availability_Base](#current_availability_base)|`decimal(38, 3)` |The current availability in а base measurement unit.|
|[Projected_Availability_Base](#projected_availability_base)|`decimal(38, 3)` |Projected Availability in а base measurement unit on the particular date. The value is cumulative and includes the sum of all planned stock movements until this date (inclusive) and the current availability.|
|[ATP_Base](#atp_base)|`decimal(38, 3)` |Indicates the quantity available to promise (in a base unit). It is valid from this date on.|

## Columns

### Enterprise_Company_Id


Enterprise_Company_Id


Тhe Enterprise Company, for which the quantities are calculated.


Тhe Enterprise Company, for which the quantities are calculated.

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
|Derived From|[Gen_Documents](Gen_Documents.md).[Enterprise_Company_Id](Gen_Documents.md#enterprise_company_id)|
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
|Equals|NULL|no|yes|

### Store_Id


Store_Id


The Store, for which the quantities are calculated.


The Store, for which the quantities are calculated.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Inv_Stores](Inv_Stores.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Inv_Store_Orders](Inv_Store_Orders.md).[Store_Id](Inv_Store_Orders.md#store_id)|
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

### Product_Id


Product_Id


The Product, for which the quantities are calculated.


The Product, for which the quantities are calculated.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Products](Gen_Products.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Inv_Store_Order_Lines](Inv_Store_Order_Lines.md).[Product_Id](Inv_Store_Order_Lines.md#product_id)|
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
|Equals|NULL|no|yes|

### From_Date


From_Date


Тhe date from which the available to promise quantity is valid.


Тhe date from which the available to promise quantity is valid.

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Inv_Demand_Management_ATP](Inv_Demand_Management_ATP.md).[From_Date](Inv_Demand_Management_ATP.md#from_date)|
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
|GreaterThanOrLessThan|None|no|no|

### Movements_Base


Movements_Base


The sum of the quantity of all planned stock movements on this date in а base measurement unit. 


The sum of the quantity of all planned stock movements on this date in а base measurement unit. 

| Property | Value |
| - | - |
|Type|decimal(38, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Inv_Demand_Management_ATP](Inv_Demand_Management_ATP.md).[Movements_Base](Inv_Demand_Management_ATP.md#movements_base)|
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

### Movements_To_Date_Base


Movements_To_Date_Base


The sum of the quantity of all planned stock movements until this date (inclusive) in а base measurement unit. The value is cumulative.


The sum of the quantity of all planned stock movements until this date (inclusive) in а base measurement unit. The value is cumulative.

| Property | Value |
| - | - |
|Type|decimal(38, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Inv_Demand_Management_ATP](Inv_Demand_Management_ATP.md).[Movements_To_Date_Base](Inv_Demand_Management_ATP.md#movements_to_date_base)|
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

### Current_Availability_Base


Current_Availability_Base


The current availability in а base measurement unit.


The current availability in а base measurement unit.

| Property | Value |
| - | - |
|Type|decimal(38, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Inv_Demand_Management_ATP](Inv_Demand_Management_ATP.md).[Current_Availability_Base](Inv_Demand_Management_ATP.md#current_availability_base)|
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

### Projected_Availability_Base


Projected_Availability_Base


Projected Availability in а base measurement unit on the particular date. The value is cumulative and includes the sum of all planned stock movements until this date (inclusive) and the current availability.


Projected Availability in а base measurement unit on the particular date. The value is cumulative and includes the sum of all planned stock movements until this date (inclusive) and the current availability.

| Property | Value |
| - | - |
|Type|decimal(38, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Inv_Demand_Management_ATP](Inv_Demand_Management_ATP.md).[Projected_Availability_Base](Inv_Demand_Management_ATP.md#projected_availability_base)|
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

### ATP_Base


ATP_Base


Indicates the quantity available to promise (in a base unit). It is valid from this date on.


Indicates the quantity available to promise (in a base unit). It is valid from this date on.

| Property | Value |
| - | - |
|Type|decimal(38, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Inv_Demand_Management_ATP](Inv_Demand_Management_ATP.md).[ATP_Base](Inv_Demand_Management_ATP.md#atp_base)|
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


