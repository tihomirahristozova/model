# Table Cash_Payment_Reasons

Represents reasons for the payments. Contains both system and user-defined reasons. Entity: Cash_Payment_Reasons

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Payment_Reason_Id|`Guid`|`PK`, Readonly||
|Is_Active|`Boolean`||Specifies whether the payment reason is active and usable for choosing in new documents. `Required` `Default(true)` `Filter(eq)` |
|Is_System|`Boolean`|Readonly|Specifies whether the payment reason is defined by the system. The system defined records are created by the system and are read-only for the user. `Required` `Default(false)` `Filter(eq)` `ReadOnly` |
|Payment_Reason_Name|`MultilanguageString`||The name of this PaymentReason. `Required` `Filter(eq;like)` `ORD` |
