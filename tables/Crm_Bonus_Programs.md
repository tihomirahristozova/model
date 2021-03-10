# Table Crm_Bonus_Programs

Bonus programs allow automatic adding of new line with bonus product or automatic application of discount in a sales document. Entity: Crm_Bonus_Programs

## Summary

| Name | Type | Description |
| - | - | --- |
|[Bonus_Program_Id](#bonus_program_id)|`uniqueidentifier` `PK`||
|[Bonus_Program_Name](#bonus_program_name)|`nvarchar(254)` `ML`|The name of the bonus program|
|[Condition_Product_Id](#condition_product_id)|`uniqueidentifier` |When not NULL, specifies a conditional product, which is required to exist in the sales document in order for the bonus program to be applied. If a condition with multiple products is required, additional products can be added to Bonus Program Products. If NULL the other conditions should be evaluated against the whole order.|
|[Condition_Min_Quantity](#condition_min_quantity)|`decimal(12, 3)` |When not NULL, specifies condition for the bonus - minimal quantity of the condition product. If the condition product is null, this cannot be specified|
|[Condition_Max_Quantity](#condition_max_quantity)|`decimal(12, 3)` |When not NULL, specifies condition for the bonus - maximal quantity of the condition product. If the condition product is null, this cannot be specified|
|[Condition_Min_Amount](#condition_min_amount)|`decimal(12, 2)` |If not NULL specifies the minimal amount for which the bonus is valid. NULL means that there is no minimal amount condition for the bonus|
|[Condition_Max_Amount](#condition_max_amount)|`decimal(12, 2)` |If not NULL specifies the maximal amount for which the bonus is valid. NULL means that there is no maximal amount condition for the bonus|
|[Condition_Document_Currency_Id](#condition_document_currency_id)|`uniqueidentifier` |Condition for the document amount. Should be not NULL if any of the amount conditions are not NULL|
|[Condition_From_Date](#condition_from_date)|`datetime` |Starting date of the bonus. NULL means that there is no starting date restriction|
|[Condition_To_Date](#condition_to_date)|`datetime` |Ending date (inclusive) of the bonus. NULL means that there is no ending date restriction|
|[Condition_Target_Group_Id](#condition_target_group_id)|`uniqueidentifier` |When not NULL, specifies that the bonus should be applied only to the specified target customer group|
|[Condition_Customer_Id](#condition_customer_id)|`uniqueidentifier` |When not NULL, specifies that the bonus should be applied only to the specified customer|
|[Condition_Customer_Filter_XML](#condition_customer_filter_xml)|`nvarchar(2147483647)` |When not NULL, specifies that the bonus should be applied only to customers who meet the specified criteria. The criteria could include custom properties|
|[Condition_Ship_To_Customer_Id](#condition_ship_to_customer_id)|`uniqueidentifier` |When not NULL, specifies that the bonus should be applied only when shipping to the specified customer|
|[Condition_Ship_To_Customer_Filter_XML](#condition_ship_to_customer_filter_xml)|`nvarchar(2147483647)` |When not NULL, specifies that the bonus should be applied only when shipping to customer with the specified characteristics|
|[Condition_Price_List_Id](#condition_price_list_id)|`uniqueidentifier` |When not NULL, specifies that the bonus should be applied only when the sales order is based on the speicfied price list|
|[Active](#active)|`bit` |General condition if the bonus is active. The other conditions are verified only for active bonus programs|
|[Bonus_Action](#bonus_action)|`nvarchar(1)` Allowed: `P`, `D`|Bonus action: P-Add product to the order, A-Add amount, D-Give discount|
|[Bonus_Product_Id](#bonus_product_id)|`uniqueidentifier` |The product that is rewarded if the bonus conditions are met. NULL means that the bonus reward is not product|
|[Bonus_Product_Quantity](#bonus_product_quantity)|`decimal(12, 3)` |The quantity rewarded of the bonus product. Should be not NULL if and only when the bonus product is not NULL|
|[Bonus_Product_Quantity_Unit_Id](#bonus_product_quantity_unit_id)|`uniqueidentifier` |The measurement unit of the quantity rewarded of the bonus product. Should be not NULL if and only when the bonus product is not NULL|
|[Bonus_Product_Quantity_Multiplier_For_Each_Lot_Size](#bonus_product_quantity_multiplier_for_each_lot_size)|`decimal(12, 3)` |When not NULL, specifies that the bonus quantity should be multiplied for each of the specified lot size. Can be non-NULL only when condition product is specified|
|[Bonus_Document_Amount_Type_Id](#bonus_document_amount_type_id)|`uniqueidentifier` |When not NULL specifies that a document amount should be added to the order when the bonus conditions are met. NULL means that the bonus reward is not a document amount|
|[Bonus_Document_Amount_Percent](#bonus_document_amount_percent)|`decimal(7, 6)` |The percent of the document amount that is rewarded. Should be NULL if and only if the bonus document amount is NULL|
|[Bonus_Line_Discount_Percent](#bonus_line_discount_percent)|`decimal(7, 6)` |The percent discount to be applied to bonus lines. Used only for bonus programs with Action = D (Discount)|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |When set, specifies that the sales document must be of the specified enterprise company.|
|[Priority](#priority)|`tinyint` Allowed: `0`, `1`, `2`, `3`, `4`|Priority (1-5) of the bonus program comparative to the other bonus programs. 1 is the lowest priority|
|[Condition_Distribution_Channel_Id](#condition_distribution_channel_id)|`uniqueidentifier` |When not NULL, specifies that the bonus should be applied only when the specified channel is used|
|[Condition_Distribution_Channel_Filter_XML](#condition_distribution_channel_filter_xml)|`nvarchar(2147483647)` |When not NULL, specifies that the bonus should be applied only when the distribution channel of the sales order has the specified characteristics|
|[Condition_Product_Group_Id](#condition_product_group_id)|`uniqueidentifier` |When not NULL, specifies that the bonus should be applied only to products from the specified product group or its subgroups|
|[Row_Version](#row_version)|`timestamp` ||
|[Company_Location_Id](#company_location_id)|`uniqueidentifier` |When set, specifies that the sales document must be of the specified enterprise company location.|

## Columns

### Bonus_Program_Id


Bonus_Program_Id

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
|Derived From|[Crm_Bonus_Programs](Crm_Bonus_Programs.md).[Bonus_Program_Id](Crm_Bonus_Programs.md#bonus_program_id)|
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

### Bonus_Program_Name


Bonus_Program_Name


The name of the bonus program


The name of the bonus program

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|yes|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Bonus_Programs](Crm_Bonus_Programs.md).[Bonus_Program_Name](Crm_Bonus_Programs.md#bonus_program_name)|
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
|Order|1|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|Like|None|no|no|

### Condition_Product_Id


Condition_Product_Id


When not NULL, specifies a conditional product, which is required to exist in the sales document in order for the bonus program to be applied. If a condition with multiple products is required, additional products can be added to Bonus Program Products. If NULL the other conditions should be evaluated against the whole order.


When not NULL, specifies a conditional product, which is required to exist in the sales document in order for the bonus program to be applied. If a condition with multiple products is required, additional products can be added to Bonus Program Products. If NULL the other conditions should be evaluated against the whole order.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Products](Gen_Products.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Bonus_Programs](Crm_Bonus_Programs.md).[Condition_Product_Id](Crm_Bonus_Programs.md#condition_product_id)|
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
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Condition_Min_Quantity


Condition_Min_Quantity


When not NULL, specifies condition for the bonus - minimal quantity of the condition product. If the condition product is null, this cannot be specified


When not NULL, specifies condition for the bonus - minimal quantity of the condition product. If the condition product is null, this cannot be specified

| Property | Value |
| - | - |
|Type|decimal(12, 3)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Bonus_Programs](Crm_Bonus_Programs.md).[Condition_Min_Quantity](Crm_Bonus_Programs.md#condition_min_quantity)|
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
|UI Width|100|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|yes|
|GreaterThanOrLessThan|None|yes|no|

### Condition_Max_Quantity


Condition_Max_Quantity


When not NULL, specifies condition for the bonus - maximal quantity of the condition product. If the condition product is null, this cannot be specified


When not NULL, specifies condition for the bonus - maximal quantity of the condition product. If the condition product is null, this cannot be specified

| Property | Value |
| - | - |
|Type|decimal(12, 3)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Bonus_Programs](Crm_Bonus_Programs.md).[Condition_Max_Quantity](Crm_Bonus_Programs.md#condition_max_quantity)|
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
|Order|4|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|yes|
|GreaterThanOrLessThan|None|yes|no|

### Condition_Min_Amount


Condition_Min_Amount


If not NULL specifies the minimal amount for which the bonus is valid. NULL means that there is no minimal amount condition for the bonus


If not NULL specifies the minimal amount for which the bonus is valid. NULL means that there is no minimal amount condition for the bonus

| Property | Value |
| - | - |
|Type|decimal(12, 2)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Bonus_Programs](Crm_Bonus_Programs.md).[Condition_Min_Amount](Crm_Bonus_Programs.md#condition_min_amount)|
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
|Order|5|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|yes|
|GreaterThanOrLessThan|None|yes|no|

### Condition_Max_Amount


Condition_Max_Amount


If not NULL specifies the maximal amount for which the bonus is valid. NULL means that there is no maximal amount condition for the bonus


If not NULL specifies the maximal amount for which the bonus is valid. NULL means that there is no maximal amount condition for the bonus

| Property | Value |
| - | - |
|Type|decimal(12, 2)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Bonus_Programs](Crm_Bonus_Programs.md).[Condition_Max_Amount](Crm_Bonus_Programs.md#condition_max_amount)|
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
|Order|6|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|yes|
|GreaterThanOrLessThan|None|yes|no|

### Condition_Document_Currency_Id


Condition_Document_Currency_Id


Condition for the document amount. Should be not NULL if any of the amount conditions are not NULL


Condition for the document amount. Should be not NULL if any of the amount conditions are not NULL

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
|Derived From|[Crm_Bonus_Programs](Crm_Bonus_Programs.md).[Condition_Document_Currency_Id](Crm_Bonus_Programs.md#condition_document_currency_id)|
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
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Condition_From_Date


Condition_From_Date


Starting date of the bonus. NULL means that there is no starting date restriction


Starting date of the bonus. NULL means that there is no starting date restriction

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
|Derived From|[Crm_Bonus_Programs](Crm_Bonus_Programs.md).[Condition_From_Date](Crm_Bonus_Programs.md#condition_from_date)|
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
|Order|8|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|yes|
|GreaterThanOrLessThan|None|yes|no|

### Condition_To_Date


Condition_To_Date


Ending date (inclusive) of the bonus. NULL means that there is no ending date restriction


Ending date (inclusive) of the bonus. NULL means that there is no ending date restriction

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
|Derived From|[Crm_Bonus_Programs](Crm_Bonus_Programs.md).[Condition_To_Date](Crm_Bonus_Programs.md#condition_to_date)|
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
|Order|9|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|yes|
|GreaterThanOrLessThan|None|yes|no|

### Condition_Target_Group_Id


Condition_Target_Group_Id


When not NULL, specifies that the bonus should be applied only to the specified target customer group


When not NULL, specifies that the bonus should be applied only to the specified target customer group

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Crm_Target_Groups](Crm_Target_Groups.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Bonus_Programs](Crm_Bonus_Programs.md).[Condition_Target_Group_Id](Crm_Bonus_Programs.md#condition_target_group_id)|
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
|Order|10|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Condition_Customer_Id


Condition_Customer_Id


When not NULL, specifies that the bonus should be applied only to the specified customer


When not NULL, specifies that the bonus should be applied only to the specified customer

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Crm_Customers](Crm_Customers.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Bonus_Programs](Crm_Bonus_Programs.md).[Condition_Customer_Id](Crm_Bonus_Programs.md#condition_customer_id)|
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
|Order|11|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Condition_Customer_Filter_XML


Condition_Customer_Filter_XML


When not NULL, specifies that the bonus should be applied only to customers who meet the specified criteria. The criteria could include custom properties


When not NULL, specifies that the bonus should be applied only to customers who meet the specified criteria. The criteria could include custom properties

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
|Derived From|[Crm_Bonus_Programs](Crm_Bonus_Programs.md).[Condition_Customer_Filter_XML](Crm_Bonus_Programs.md#condition_customer_filter_xml)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|yes|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|2147483647|
|Order|12|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

### Condition_Ship_To_Customer_Id


Condition_Ship_To_Customer_Id


When not NULL, specifies that the bonus should be applied only when shipping to the specified customer


When not NULL, specifies that the bonus should be applied only when shipping to the specified customer

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Crm_Customers](Crm_Customers.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Bonus_Programs](Crm_Bonus_Programs.md).[Condition_Ship_To_Customer_Id](Crm_Bonus_Programs.md#condition_ship_to_customer_id)|
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
|Order|13|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Condition_Ship_To_Customer_Filter_XML


Condition_Ship_To_Customer_Filter_XML


When not NULL, specifies that the bonus should be applied only when shipping to customer with the specified characteristics


When not NULL, specifies that the bonus should be applied only when shipping to customer with the specified characteristics

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
|Derived From|[Crm_Bonus_Programs](Crm_Bonus_Programs.md).[Condition_Ship_To_Customer_Filter_XML](Crm_Bonus_Programs.md#condition_ship_to_customer_filter_xml)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|yes|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|2147483647|
|Order|14|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

### Condition_Price_List_Id


Condition_Price_List_Id


When not NULL, specifies that the bonus should be applied only when the sales order is based on the speicfied price list


When not NULL, specifies that the bonus should be applied only when the sales order is based on the speicfied price list

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Crm_Price_Lists](Crm_Price_Lists.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Bonus_Programs](Crm_Bonus_Programs.md).[Condition_Price_List_Id](Crm_Bonus_Programs.md#condition_price_list_id)|
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
|Order|15|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Active


Active


General condition if the bonus is active. The other conditions are verified only for active bonus programs


General condition if the bonus is active. The other conditions are verified only for active bonus programs

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|True|
|Derived From|[Crm_Bonus_Programs](Crm_Bonus_Programs.md).[Active](Crm_Bonus_Programs.md#active)|
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
|Order|16|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Bonus_Action


Bonus_Action


Bonus action: P-Add product to the order, A-Add amount, D-Give discount


Bonus action: P-Add product to the order, A-Add amount, D-Give discount

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
|Allowed Values|`P`, `D`|
|Default Value|D|
|Derived From|[Crm_Bonus_Programs](Crm_Bonus_Programs.md).[Bonus_Action](Crm_Bonus_Programs.md#bonus_action)|
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
|Order|17|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Bonus_Product_Id


Bonus_Product_Id


The product that is rewarded if the bonus conditions are met. NULL means that the bonus reward is not product


The product that is rewarded if the bonus conditions are met. NULL means that the bonus reward is not product

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Products](Gen_Products.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Bonus_Programs](Crm_Bonus_Programs.md).[Bonus_Product_Id](Crm_Bonus_Programs.md#bonus_product_id)|
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
|Order|18|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Bonus_Product_Quantity


Bonus_Product_Quantity


The quantity rewarded of the bonus product. Should be not NULL if and only when the bonus product is not NULL


The quantity rewarded of the bonus product. Should be not NULL if and only when the bonus product is not NULL

| Property | Value |
| - | - |
|Type|decimal(12, 3)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Bonus_Programs](Crm_Bonus_Programs.md).[Bonus_Product_Quantity](Crm_Bonus_Programs.md#bonus_product_quantity)|
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
|Order|19|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

### Bonus_Product_Quantity_Unit_Id


Bonus_Product_Quantity_Unit_Id


The measurement unit of the quantity rewarded of the bonus product. Should be not NULL if and only when the bonus product is not NULL


The measurement unit of the quantity rewarded of the bonus product. Should be not NULL if and only when the bonus product is not NULL

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
|Derived From|[Crm_Bonus_Programs](Crm_Bonus_Programs.md).[Bonus_Product_Quantity_Unit_Id](Crm_Bonus_Programs.md#bonus_product_quantity_unit_id)|
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
|Order|20|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Bonus_Product_Quantity_Multiplier_For_Each_Lot_Size


Bonus_Product_Quantity_Multiplier_For_Each_Lot_Size


When not NULL, specifies that the bonus quantity should be multiplied for each of the specified lot size. Can be non-NULL only when condition product is specified


When not NULL, specifies that the bonus quantity should be multiplied for each of the specified lot size. Can be non-NULL only when condition product is specified

| Property | Value |
| - | - |
|Type|decimal(12, 3)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Bonus_Programs](Crm_Bonus_Programs.md).[Bonus_Product_Quantity_Multiplier_For_Each_Lot_Size](Crm_Bonus_Programs.md#bonus_product_quantity_multiplier_for_each_lot_size)|
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
|Order|21|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

### Bonus_Document_Amount_Type_Id


Bonus_Document_Amount_Type_Id


When not NULL specifies that a document amount should be added to the order when the bonus conditions are met. NULL means that the bonus reward is not a document amount


When not NULL specifies that a document amount should be added to the order when the bonus conditions are met. NULL means that the bonus reward is not a document amount

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Document_Amount_Types](Gen_Document_Amount_Types.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Bonus_Programs](Crm_Bonus_Programs.md).[Bonus_Document_Amount_Type_Id](Crm_Bonus_Programs.md#bonus_document_amount_type_id)|
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
|Order|22|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Bonus_Document_Amount_Percent


Bonus_Document_Amount_Percent


The percent of the document amount that is rewarded. Should be NULL if and only if the bonus document amount is NULL


The percent of the document amount that is rewarded. Should be NULL if and only if the bonus document amount is NULL

| Property | Value |
| - | - |
|Type|decimal(7, 6)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Bonus_Programs](Crm_Bonus_Programs.md).[Bonus_Document_Amount_Percent](Crm_Bonus_Programs.md#bonus_document_amount_percent)|
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
|Order|23|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Bonus_Line_Discount_Percent


Bonus_Line_Discount_Percent


The percent discount to be applied to bonus lines. Used only for bonus programs with Action = D (Discount)


The percent discount to be applied to bonus lines. Used only for bonus programs with Action = D (Discount)

| Property | Value |
| - | - |
|Type|decimal(7, 6)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None, IsPercent|
|Default Value|0|
|Derived From|[Crm_Bonus_Programs](Crm_Bonus_Programs.md).[Bonus_Line_Discount_Percent](Crm_Bonus_Programs.md#bonus_line_discount_percent)|
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
|Order|24|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Enterprise_Company_Id


Enterprise_Company_Id


When set, specifies that the sales document must be of the specified enterprise company.


When set, specifies that the sales document must be of the specified enterprise company.

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
|Derived From|[Crm_Bonus_Programs](Crm_Bonus_Programs.md).[Enterprise_Company_Id](Crm_Bonus_Programs.md#enterprise_company_id)|
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

### Priority


Priority


Priority (1-5) of the bonus program comparative to the other bonus programs. 1 is the lowest priority


Priority (1-5) of the bonus program comparative to the other bonus programs. 1 is the lowest priority

| Property | Value |
| - | - |
|Type|tinyint|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`0`, `1`, `2`, `3`, `4`|
|Default Value|2|
|Derived From|[Crm_Bonus_Programs](Crm_Bonus_Programs.md).[Priority](Crm_Bonus_Programs.md#priority)|
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

### Condition_Distribution_Channel_Id


Condition_Distribution_Channel_Id


When not NULL, specifies that the bonus should be applied only when the specified channel is used


When not NULL, specifies that the bonus should be applied only when the specified channel is used

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Crm_Distribution_Channels](Crm_Distribution_Channels.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Bonus_Programs](Crm_Bonus_Programs.md).[Condition_Distribution_Channel_Id](Crm_Bonus_Programs.md#condition_distribution_channel_id)|
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

### Condition_Distribution_Channel_Filter_XML


Condition_Distribution_Channel_Filter_XML


When not NULL, specifies that the bonus should be applied only when the distribution channel of the sales order has the specified characteristics


When not NULL, specifies that the bonus should be applied only when the distribution channel of the sales order has the specified characteristics

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
|Derived From|[Crm_Bonus_Programs](Crm_Bonus_Programs.md).[Condition_Distribution_Channel_Filter_XML](Crm_Bonus_Programs.md#condition_distribution_channel_filter_xml)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|yes|
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

### Condition_Product_Group_Id


Condition_Product_Group_Id


When not NULL, specifies that the bonus should be applied only to products from the specified product group or its subgroups


When not NULL, specifies that the bonus should be applied only to products from the specified product group or its subgroups

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Product_Groups](Gen_Product_Groups.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Bonus_Programs](Crm_Bonus_Programs.md).[Condition_Product_Group_Id](Crm_Bonus_Programs.md#condition_product_group_id)|
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
|Derived From|[Crm_Bonus_Programs](Crm_Bonus_Programs.md).[Row_Version](Crm_Bonus_Programs.md#row_version)|
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

### Company_Location_Id


Company_Location_Id


When set, specifies that the sales document must be of the specified enterprise company location.


When set, specifies that the sales document must be of the specified enterprise company location.

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
|Derived From|[Crm_Bonus_Programs](Crm_Bonus_Programs.md).[Company_Location_Id](Crm_Bonus_Programs.md#company_location_id)|
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


