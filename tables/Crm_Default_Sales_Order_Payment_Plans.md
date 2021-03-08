# Table Crm_Default_Sales_Order_Payment_Plans

Default payment plan for new documents of the specified document type. Entity: Crm_Default_Sales_Order_Payment_Plans

# Aggregate Hierarchy

* [Gen_Document_Types](Gen_Document_Types.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Default_Sales_Order_Payment_Plan_Id|`Guid`|`PK`, Readonly||
|Amount_Percent|`Decimal?`||Percent of the sales order amount to be payed. |
|Due_Date_Form_Method|`PaymentPlanDueDateSource`|Allowed: `EXP`, `INV`, `SLS`, `SDD`, `IDD`|Method to determine the payment due date. SLS = Use sales order date, INV = Use invoice date, EXP = Specify the date explicitly, SDD = Sales order due date, IDD = Invoice due date. `Required` |
|Installment_Number|`Int32`||Consequtive installment number. Used for identifying different payments generated according this payment plan. `Required` |
|Payment_Term_Days|`Int32`||Payment term in days, which are to be added to form the payment due date. 0 means that the date determined by Due_Date_Form_Method and Explicit_Payment_Due_Date is taken as due date. `Required` `Default(0)` |
|Remainder|`Boolean`||Indicates wheather this amount is the remainder of the document. Amount = Total amount of the sales order - explicitly specified amounts in the plan (by Amount_Percent). `Required` `Default(false)` |
