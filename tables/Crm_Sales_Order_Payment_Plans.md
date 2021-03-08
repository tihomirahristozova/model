# Table Crm_Sales_Order_Payment_Plans

Payment plan of a sales order. Entity: Crm_Sales_Order_Payment_Plans

# Aggregate Hierarchy

* [Crm_Sales_Orders](Crm_Sales_Orders.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Sales_Order_Payment_Plan_Id|`Guid`|`PK`, Readonly||
|Amount_Percent|`Decimal?`||Percent of the sales order amount to be payed. |
|Due_Date_Form_Method|`PaymentPlanDueDateSource`|Allowed: `EXP`, `INV`, `SLS`, `SDD`, `IDD`|Method to determine the payment due date. SLS = Use sales order date, INV = Use invoice date, EXP = Specify the date explicitly, SDD = Sales order due date, IDD = Invoice due date. `Required` |
|Explicit_Payment_Due_Date|`DateTime?`||Explicitly specified payment due date. Must be filled if and only if Due_Date_Form_Method = 'EXP'. |
|Explicit_Payment_Due_Start_Date|`DateTime?`||Explicitly specified date on which the payment becomes executable. Can be specified only when date formation method is 'Set explicit date'. |
|Installment_Number|`Int32`||Consequtive installment number. Used for identifying different payments generated according this payment plan. `Required` |
|Notes|`String`||Notes for this SalesOrderPaymentPlan. |
|Payment_Start_Days|`Int32`||Number of days until the payment becomes executable. The days are counted, starting with the date, specified by due date formation method. `Required` `Default(0)` |
|Payment_Term_Days|`Int32`||Payment term in days, which are to be added to form the payment due date. 0 means that the date determined by Due_Date_Form_Method and Explicit_Payment_Due_Date is taken as due date. `Required` `Default(0)` |
|Remainder|`Boolean`||Indicates wheather this amount is the remainder of the document. Amount = Total amount of the sales order - explicitly specified amounts in the plan (by Amount_Percent or Amount). `Required` `Default(false)` |
