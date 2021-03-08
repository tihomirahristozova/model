# Table Cash_Payment_Slip_Amounts

Mass payment amount. Each record generates one payment transaction. Entity: Cash_Payment_Slip_Amounts

# Aggregate Hierarchy

* [Cash_Payment_Slips](Cash_Payment_Slips.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Payment_Slip_Amount_Id|`Guid`|`PK`, Readonly||
|Description|`String`||Description of the payed amount. The numbers of the documents which are payed for example. |
|Direction|`Direction`|Allowed: `I`, `R`|'I' for Payment issue, 'R' for payment receipt. `Required` `Filter(eq)` |
|Is_Party_Payment|`Boolean`||Indicates whether the amount is payed or received by party or not (i.e. the amount is for fee, tax, etc.). `Required` `Default(true)` |
|Line_No|`Int32`||The number of the line within the payment. `Required` |
|Party_Name|`MultilanguageString`||The name of the party that is paying or receiving the money. The column can be left blank if there is no party involved (e.g. the amount is fee). |
|Payment_Date|`DateTime`||The date on which the payment is done. `Required` `Filter(ge;le)` |
