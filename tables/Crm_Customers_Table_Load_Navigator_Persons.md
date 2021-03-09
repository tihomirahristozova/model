# Query Crm_Customers_Table_Load_Navigator_Persons


## Summary

| Name | Type | Description |
| - | - | --- |
|[Customer_Id](#customer_id)|`uniqueidentifier` `PK`||
|[Party_Id](#party_id)|`uniqueidentifier` ||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[From_Date](#from_date)|`datetime` ||
|[Thru_Date](#thru_date)|`datetime` ||
|[Default_Price_List_Id](#default_price_list_id)|`uniqueidentifier` ||
|[Default_Payment_Term_Days](#default_payment_term_days)|`int` ||
|[Default_Delivery_Term_Days](#default_delivery_term_days)|`int` ||
|[Customer_Number](#customer_number)|`nvarchar` ||
|[Default_Payment_Type_Id](#default_payment_type_id)|`uniqueidentifier` ||
|[Credit_Limit](#credit_limit)|`decimal(0, 0)` |Total credit limit for the customer in the customers' default currency. NULL means there is no limit|
|[Sales_Person_Id](#sales_person_id)|`uniqueidentifier` ||
|[Creation_Time](#creation_time)|`datetime` Readonly||
|[Creation_User](#creation_user)|`nvarchar` Readonly||
|[Update_Time](#update_time)|`datetime` Readonly||
|[Update_User](#update_user)|`nvarchar` Readonly||
|[Collections_Responsible_Employee_Id](#collections_responsible_employee_id)|`uniqueidentifier` ||
|[Default_Payment_Account_Id](#default_payment_account_id)|`uniqueidentifier` ||
|[Default_Currency_Id](#default_currency_id)|`uniqueidentifier` ||
|[Customer_Type_Id](#customer_type_id)|`uniqueidentifier` ||
|[Persist_Sales_Orders_Lots](#persist_sales_orders_lots)|`bit` |If checked, specifies that the lots set in the Sales orders for this customer, cannot be changed during the execution of the Store transactions for these Sales orders.|
|[Default_Distribution_Channel_Id](#default_distribution_channel_id)|`uniqueidentifier` ||
|[Active](#active)|`bit` |1 if the customer is active, 0 - not to list in combo boxes for choosing in new documents|
|[Default_Payment_Start_Days](#default_payment_start_days)|`int` |Specifies the number of days after the sales order, when the payment becomes due. 0 means that the payment is due immediately.|
|[Grace_Period_Days](#grace_period_days)|`int` |Number of days after the payment deadline, during which the system still allows new sales orders for the customer.|
|[Serviced_By_Enterprise_Company_Location_Id](#serviced_by_enterprise_company_location_id)|`uniqueidentifier` |The enterprise company location, which sells to this client by default.|
|[Allow_Use_As_Primary_Customer](#allow_use_as_primary_customer)|`bit` |Specifies whether to allow the customer to be used as primary customer in a sales deal.|
|[Allow_Use_As_Ship_To_Customer](#allow_use_as_ship_to_customer)|`bit` |True to allow the customer to be used as ship to customer in a sales deal.|
|[Row_Version](#row_version)|`timestamp` ||
|[Person_Id](#person_id)|`uniqueidentifier` `PK`||
|[First_Name](#first_name)|`nvarchar` `ML`||
|[Middle_Name](#middle_name)|`nvarchar` `ML`||
|[Last_Name](#last_name)|`nvarchar` `ML`||
|[Title](#title)|`nvarchar` `ML`||
|[Gender](#gender)|`nvarchar` Allowed: `F`, `M`||
|[Birth_Date](#birth_date)|`datetime` ||
|[Nationality](#nationality)|`uniqueidentifier` ||
|[Nationality_Text](#nationality_text)|`nvarchar` `ML`||
|[National_Number](#national_number)|`nvarchar` ||
|[Passport_Number](#passport_number)|`nvarchar` ||
|[Passport_Issuing_Date](#passport_issuing_date)|`datetime` ||
|[Parent_Party_Id](#parent_party_id)|`uniqueidentifier` ||
|[Party_Code](#party_code)|`nvarchar` Readonly||
|[Area_Id](#area_id)|`uniqueidentifier` ||
|[GLN](#gln)|`nvarchar` ||
|[Is_Active](#is_active)|`bit` |Specifies whether the current party is active in the system or not.|
|[Notes](#notes)|`nvarchar` ||
|[Sales_Person_Group_Id](#sales_person_group_id)|`uniqueidentifier` ||
|[Area_Id_L1_Name](#area_id_l1_name)|`nvarchar` `ML`||
|[Area_Id_L2_Name](#area_id_l2_name)|`nvarchar` `ML`||
|[Area_Id_L3_Name](#area_id_l3_name)|`nvarchar` `ML`||
|[Area_Id_L4_Name](#area_id_l4_name)|`nvarchar` `ML`||
|[Area_Id_L5_Name](#area_id_l5_name)|`nvarchar` `ML`||
|[Area_Id_L6_Name](#area_id_l6_name)|`nvarchar` `ML`||
|[Sales_Person_Group_Id_L1_Name](#sales_person_group_id_l1_name)|`nvarchar` `ML`||
|[Sales_Person_Group_Id_L2_Name](#sales_person_group_id_l2_name)|`nvarchar` `ML`||
|[Sales_Person_Group_Id_L3_Name](#sales_person_group_id_l3_name)|`nvarchar` `ML`||
|[Sales_Person_Group_Id_L4_Name](#sales_person_group_id_l4_name)|`nvarchar` `ML`||
|[Sales_Person_Group_Id_L5_Name](#sales_person_group_id_l5_name)|`nvarchar` `ML`||
|[Sales_Person_Group_Id_L6_Name](#sales_person_group_id_l6_name)|`nvarchar` `ML`||

## Columns

### Customer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### From_Date

| Property | Value |
| - | - |
|Type|datetime|

### Thru_Date

| Property | Value |
| - | - |
|Type|datetime|

### Default_Price_List_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Default_Payment_Term_Days

| Property | Value |
| - | - |
|Type|int|

### Default_Delivery_Term_Days

| Property | Value |
| - | - |
|Type|int|

### Customer_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### Default_Payment_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Credit_Limit

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Sales_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Creation_Time

| Property | Value |
| - | - |
|Type|datetime|

### Creation_User

| Property | Value |
| - | - |
|Type|nvarchar|

### Update_Time

| Property | Value |
| - | - |
|Type|datetime|

### Update_User

| Property | Value |
| - | - |
|Type|nvarchar|

### Collections_Responsible_Employee_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Default_Payment_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Default_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Customer_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Persist_Sales_Orders_Lots

| Property | Value |
| - | - |
|Type|bit|

### Default_Distribution_Channel_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Active

| Property | Value |
| - | - |
|Type|bit|

### Default_Payment_Start_Days

| Property | Value |
| - | - |
|Type|int|

### Grace_Period_Days

| Property | Value |
| - | - |
|Type|int|

### Serviced_By_Enterprise_Company_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Allow_Use_As_Primary_Customer

| Property | Value |
| - | - |
|Type|bit|

### Allow_Use_As_Ship_To_Customer

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### First_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Middle_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Last_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Title

| Property | Value |
| - | - |
|Type|nvarchar|

### Gender

| Property | Value |
| - | - |
|Type|nvarchar|

### Birth_Date

| Property | Value |
| - | - |
|Type|datetime|

### Nationality

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Nationality_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### National_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### Passport_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### Passport_Issuing_Date

| Property | Value |
| - | - |
|Type|datetime|

### Parent_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Party_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Area_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### GLN

| Property | Value |
| - | - |
|Type|nvarchar|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Sales_Person_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Area_Id_L1_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Area_Id_L2_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Area_Id_L3_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Area_Id_L4_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Area_Id_L5_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Area_Id_L6_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Sales_Person_Group_Id_L1_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Sales_Person_Group_Id_L2_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Sales_Person_Group_Id_L3_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Sales_Person_Group_Id_L4_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Sales_Person_Group_Id_L5_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Sales_Person_Group_Id_L6_Name

| Property | Value |
| - | - |
|Type|nvarchar|


