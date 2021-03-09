# Table Crm_Customers

Customer contracts list. For each combination of Enterprise Company and external Party there can be zero or one records of this. Entity: Crm_Customers

## Owner Tables Hierarchy

* [Gen_Parties](Gen_Parties.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Customer_Id](#customer_id)|`uniqueidentifier` `PK`|Unique customer Id|
|[Party_Id](#party_id)|`uniqueidentifier` |Base party Id|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The Enterprise Company for which this customer is recorded. The same external party can be listed with different conditions for the different enterprise companies.|
|[From_Date](#from_date)|`datetime` |Start date of the customer relationship|
|[Thru_Date](#thru_date)|`datetime` |The date of customer relationship termination. NULL for active customers.|
|[Default_Price_List_Id](#default_price_list_id)|`uniqueidentifier` |If not NULL, specifies default price list when selling to this customer|
|[Default_Payment_Term_Days](#default_payment_term_days)|`int` |Default payment term in days when issuing documents for this customer|
|[Default_Delivery_Term_Days](#default_delivery_term_days)|`int` |Default term in days for goods delivery, starting at the day of sale|
|[Customer_Number](#customer_number)|`nvarchar(16)` |Unique customer number|
|[Default_Payment_Type_Id](#default_payment_type_id)|`uniqueidentifier` |If not NULL, specifies default payment type for the sales, offers and invoices for this customer|
|[Credit_Limit](#credit_limit)|`decimal(18, 2)` |Total credit limit for the customer in the customers' default currency. NULL means there is no limit|
|[Sales_Person_Id](#sales_person_id)|`uniqueidentifier` |The default sales person for new sales documents for this customer|
|[Creation_Time](#creation_time)|`datetime` Readonly||
|[Creation_User](#creation_user)|`nvarchar(64)` Readonly||
|[Update_Time](#update_time)|`datetime` Readonly||
|[Update_User](#update_user)|`nvarchar(64)` Readonly||
|[Collections_Responsible_Employee_Id](#collections_responsible_employee_id)|`uniqueidentifier` |The employee, who is responsible for the collections from the customer|
|[Default_Payment_Account_Id](#default_payment_account_id)|`uniqueidentifier` |The default payment account to use when creating new documents for this customer|
|[Default_Currency_Id](#default_currency_id)|`uniqueidentifier` |The primary currency for value calculations for this customer - for credit limit, due amounts, etc.|
|[Customer_Type_Id](#customer_type_id)|`uniqueidentifier` |The user-defined type of this customer. NULL when there is no specific type. Record-level security from the customer type is applied to the individual customers and can be used for security purposes|
|[Persist_Sales_Orders_Lots](#persist_sales_orders_lots)|`bit` |If checked, specifies that the lots set in the Sales orders for this customer, cannot be changed during the execution of the Store transactions for these Sales orders.|
|[Default_Distribution_Channel_Id](#default_distribution_channel_id)|`uniqueidentifier` |The default distribution channel used when selling to the customer|
|[Active](#active)|`bit` |1 if the customer is active, 0 - not to list in combo boxes for choosing in new documents|
|[Default_Payment_Start_Days](#default_payment_start_days)|`int` |Specifies the number of days after the sales order, when the payment becomes due. 0 means that the payment is due immediately.|
|[Grace_Period_Days](#grace_period_days)|`int` |Number of days after the payment deadline, during which the system still allows new sales orders for the customer.|
|[Serviced_By_Enterprise_Company_Location_Id](#serviced_by_enterprise_company_location_id)|`uniqueidentifier` |The enterprise company location, which sells to this client by default.|
|[Allow_Use_As_Primary_Customer](#allow_use_as_primary_customer)|`bit` |Specifies whether to allow the customer to be used as primary customer in a sales deal.|
|[Allow_Use_As_Ship_To_Customer](#allow_use_as_ship_to_customer)|`bit` |True to allow the customer to be used as ship to customer in a sales deal.|
|[Row_Version](#row_version)|`timestamp` ||

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
|Type|nvarchar(16)|

### Default_Payment_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Credit_Limit

| Property | Value |
| - | - |
|Type|decimal(18, 2)|

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
|Type|nvarchar(64)|

### Update_Time

| Property | Value |
| - | - |
|Type|datetime|

### Update_User

| Property | Value |
| - | - |
|Type|nvarchar(64)|

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


