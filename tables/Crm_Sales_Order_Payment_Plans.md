# Table Crm_Sales_Order_Payment_Plans

Payment plan of a sales order. Entity: Crm_Sales_Order_Payment_Plans

## Owner Tables Hierarchy

* [Crm_Sales_Orders](Crm_Sales_Orders.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Sales_Order_Payment_Plan_Id](#sales_order_payment_plan_id)|`uniqueidentifier` `PK`|Unique identification of the payment plan|
|[Sales_Order_Id](#sales_order_id)|`uniqueidentifier` ||
|[Installment_Number](#installment_number)|`int` |Consequtive installment number. Used for identifying different payments generated according this payment plan.|
|[Due_Date_Form_Method](#due_date_form_method)|`nvarchar(3)` Allowed: `EXP`, `INV`, `SLS`, `SDD`, `IDD`|Method to determine the payment due date. SLS = Use sales order date, INV = Use invoice date, EXP = Specify the date explicitly, SDD = Sales order due date, IDD = Invoice due date|
|[Explicit_Payment_Due_Date](#explicit_payment_due_date)|`datetime` |Explicitly specified payment due date. Must be filled if and only if Due_Date_Form_Method = 'EXP'|
|[Payment_Term_Days](#payment_term_days)|`int` |Payment term in days, which are to be added to form the payment due date. 0 means that the date determined by Due_Date_Form_Method and Explicit_Payment_Due_Date is taken as due date.|
|[Amount_Percent](#amount_percent)|`decimal(7, 6)` |Percent of the sales order amount to be payed.|
|[Remainder](#remainder)|`bit` |Indicates wheather this amount is the remainder of the document. Amount = Total amount of the sales order - explicitly specified amounts in the plan (by Amount_Percent or Amount).|
|[Amount](#amount)|`decimal(14, 2)` |Amount to be payed.|
|[Notes](#notes)|`nvarchar(254)` ||
|[Explicit_Payment_Due_Start_Date](#explicit_payment_due_start_date)|`date` |Explicitly specified date on which the payment becomes executable. Can be specified only when date formation method is 'Set explicit date'.|
|[Payment_Start_Days](#payment_start_days)|`int` |Number of days until the payment becomes executable. The days are counted, starting with the date, specified by due date formation method.|
|[Payment_Type_Id](#payment_type_id)|`uniqueidentifier` |Specifies the expected payment type. NULL means that there is no expected payment type. For POS implementations, this can be used to denote the payment type which actually occurred.|
|[Payment_Account_Id](#payment_account_id)|`uniqueidentifier` |Specifies the payment account towards which the payment is expected. NULL means that there is no expectation for payment account. For POS implementations, this can be used to denote the payment account in which the payment actually occurred.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Sales_Order_Payment_Plan_Id


Sales_Order_Payment_Plan_Id


Unique identification of the payment plan


Unique identification of the payment plan

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
|Derived From|[Crm_Sales_Order_Payment_Plans](Crm_Sales_Order_Payment_Plans.md).[Sales_Order_Payment_Plan_Id](Crm_Sales_Order_Payment_Plans.md#sales_order_payment_plan_id)|
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

### Sales_Order_Id


Sales_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Crm_Sales_Orders](Crm_Sales_Orders.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Order_Payment_Plans](Crm_Sales_Order_Payment_Plans.md).[Sales_Order_Id](Crm_Sales_Order_Payment_Plans.md#sales_order_id)|
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

### Installment_Number


Installment_Number


Consequtive installment number. Used for identifying different payments generated according this payment plan.


Consequtive installment number. Used for identifying different payments generated according this payment plan.

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
|Derived From|[Crm_Sales_Order_Payment_Plans](Crm_Sales_Order_Payment_Plans.md).[Installment_Number](Crm_Sales_Order_Payment_Plans.md#installment_number)|
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

### Due_Date_Form_Method


Due_Date_Form_Method


Method to determine the payment due date. SLS = Use sales order date, INV = Use invoice date, EXP = Specify the date explicitly, SDD = Sales order due date, IDD = Invoice due date


Method to determine the payment due date. SLS = Use sales order date, INV = Use invoice date, EXP = Specify the date explicitly, SDD = Sales order due date, IDD = Invoice due date

| Property | Value |
| - | - |
|Type|nvarchar(3)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`EXP`, `INV`, `SLS`, `SDD`, `IDD`|
|Default Value|None|
|Derived From|[Crm_Sales_Order_Payment_Plans](Crm_Sales_Order_Payment_Plans.md).[Due_Date_Form_Method](Crm_Sales_Order_Payment_Plans.md#due_date_form_method)|
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
|Max Length|3|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|no|

### Explicit_Payment_Due_Date


Explicit_Payment_Due_Date


Explicitly specified payment due date. Must be filled if and only if Due_Date_Form_Method = 'EXP'


Explicitly specified payment due date. Must be filled if and only if Due_Date_Form_Method = 'EXP'

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
|Derived From|[Crm_Sales_Order_Payment_Plans](Crm_Sales_Order_Payment_Plans.md).[Explicit_Payment_Due_Date](Crm_Sales_Order_Payment_Plans.md#explicit_payment_due_date)|
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

### Payment_Term_Days


Payment_Term_Days


Payment term in days, which are to be added to form the payment due date. 0 means that the date determined by Due_Date_Form_Method and Explicit_Payment_Due_Date is taken as due date.


Payment term in days, which are to be added to form the payment due date. 0 means that the date determined by Due_Date_Form_Method and Explicit_Payment_Due_Date is taken as due date.

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Crm_Sales_Order_Payment_Plans](Crm_Sales_Order_Payment_Plans.md).[Payment_Term_Days](Crm_Sales_Order_Payment_Plans.md#payment_term_days)|
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

### Amount_Percent


Amount_Percent


Percent of the sales order amount to be payed.


Percent of the sales order amount to be payed.

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
|Derived From|[Crm_Sales_Order_Payment_Plans](Crm_Sales_Order_Payment_Plans.md).[Amount_Percent](Crm_Sales_Order_Payment_Plans.md#amount_percent)|
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

### Remainder


Remainder


Indicates wheather this amount is the remainder of the document. Amount = Total amount of the sales order - explicitly specified amounts in the plan (by Amount_Percent or Amount).


Indicates wheather this amount is the remainder of the document. Amount = Total amount of the sales order - explicitly specified amounts in the plan (by Amount_Percent or Amount).

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Crm_Sales_Order_Payment_Plans](Crm_Sales_Order_Payment_Plans.md).[Remainder](Crm_Sales_Order_Payment_Plans.md#remainder)|
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

### Amount


Amount


Amount to be payed.


Amount to be payed.

| Property | Value |
| - | - |
|Type|decimal(14, 2)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Order_Payment_Plans](Crm_Sales_Order_Payment_Plans.md).[Amount](Crm_Sales_Order_Payment_Plans.md#amount)|
|Format|N2|
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

### Notes


Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None, IsLongString|
|Default Value|None|
|Derived From|[Crm_Sales_Order_Payment_Plans](Crm_Sales_Order_Payment_Plans.md).[Notes](Crm_Sales_Order_Payment_Plans.md#notes)|
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
|Visible|no|
|Max Length|254|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Explicit_Payment_Due_Start_Date


Explicit_Payment_Due_Start_Date


Explicitly specified date on which the payment becomes executable. Can be specified only when date formation method is 'Set explicit date'.


Explicitly specified date on which the payment becomes executable. Can be specified only when date formation method is 'Set explicit date'.

| Property | Value |
| - | - |
|Type|date|
|DateTime Format|Date|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Order_Payment_Plans](Crm_Sales_Order_Payment_Plans.md).[Explicit_Payment_Due_Start_Date](Crm_Sales_Order_Payment_Plans.md#explicit_payment_due_start_date)|
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

### Payment_Start_Days


Payment_Start_Days


Number of days until the payment becomes executable. The days are counted, starting with the date, specified by due date formation method.


Number of days until the payment becomes executable. The days are counted, starting with the date, specified by due date formation method.

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Crm_Sales_Order_Payment_Plans](Crm_Sales_Order_Payment_Plans.md).[Payment_Start_Days](Crm_Sales_Order_Payment_Plans.md#payment_start_days)|
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

### Payment_Type_Id


Payment_Type_Id


Specifies the expected payment type. NULL means that there is no expected payment type. For POS implementations, this can be used to denote the payment type which actually occurred.


Specifies the expected payment type. NULL means that there is no expected payment type. For POS implementations, this can be used to denote the payment type which actually occurred.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Cash_Payment_Types](Cash_Payment_Types.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Order_Payment_Plans](Crm_Sales_Order_Payment_Plans.md).[Payment_Type_Id](Crm_Sales_Order_Payment_Plans.md#payment_type_id)|
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

### Payment_Account_Id


Payment_Account_Id


Specifies the payment account towards which the payment is expected. NULL means that there is no expectation for payment account. For POS implementations, this can be used to denote the payment account in which the payment actually occurred.


Specifies the payment account towards which the payment is expected. NULL means that there is no expectation for payment account. For POS implementations, this can be used to denote the payment account in which the payment actually occurred.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Cash_Payment_Accounts](Cash_Payment_Accounts.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Sales_Order_Payment_Plans](Crm_Sales_Order_Payment_Plans.md).[Payment_Account_Id](Crm_Sales_Order_Payment_Plans.md#payment_account_id)|
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
|Derived From|[Crm_Sales_Order_Payment_Plans](Crm_Sales_Order_Payment_Plans.md).[Row_Version](Crm_Sales_Order_Payment_Plans.md#row_version)|
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


