# Table Crm_Customers

Customer contracts list. For each combination of Enterprise Company and external Party there can be zero or one records of this. Entity: Crm_Customers

# Aggregate Hierarchy

* [Gen_Parties](Gen_Parties.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Customer_Id|`Guid`|`PK`, Readonly||
|Active|`Boolean`||True if the customer is active, false - not to list in combo boxes for choosing in new documents. `Required` `Default(true)` `Filter(eq)` |
|Allow_Use_As_Primary_Customer|`Boolean`||Specifies whether to allow the customer to be used as primary customer in a sales deal. `Required` `Default(false)` `Filter(eq)` |
|Allow_Use_As_Ship_To_Customer|`Boolean`||True to allow the customer to be used as ship to customer in a sales deal. `Required` `Default(false)` `Filter(eq)` |
|Creation_Time|`DateTime?`|Readonly|Date and time when the Customer was created. `Filter(ge;le)` `ReadOnly` |
|Creation_User|`String`|Readonly|Login name of the user, who created the Customer. `Filter(like)` `ReadOnly` |
|Default_Delivery_Term_Days|`Int32`||Default term in days for goods delivery, starting at the day of sale. `Required` `Default(0)` |
|Default_Payment_Start_Days|`Int32`||Specifies the number of days after the sales order, when the payment becomes due. 0 means that the payment is due immediately. `Required` `Default(0)` |
|Default_Payment_Term_Days|`Int32`||Default payment term in days when issuing documents for this customer. `Required` `Default(0)` |
|From_Date|`DateTime?`||Start date of the customer relationship. `Default(Today)` `Filter(ge;le)` |
|Grace_Period_Days|`Int32`||Number of days after the payment deadline, during which the system still allows new sales orders for the customer. `Required` `Default(0)` |
|Customer_Number|`String`||Unique customer number. `Filter(eq;like)` `ORD` |
|Persist_Sales_Orders_Lots|`Boolean`||If checked, specifies that the lots set in the Sales orders for this customer, cannot be changed during the execution of the Store transactions for these Sales orders. `Required` `Default(false)` `Filter(eq)` |
|Thru_Date|`DateTime?`||The date of customer relationship termination. null for active customers. `Filter(ge;le)` |
|Update_Time|`DateTime?`|Readonly|Date and time when the Customer was last updated. `Filter(ge;le)` `ReadOnly` |
|Update_User|`String`|Readonly|Login name of the user, who last updated the Customer. `Filter(like)` `ReadOnly` |
