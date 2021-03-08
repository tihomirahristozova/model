# Table Cash_Payment_Types

Describes the way of payment. For example: in cash, by bank transfer, with credit card, etc. Entity: Cash_Payment_Types

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Payment_Type_Id|`Guid`|`PK`, Readonly||
|Payment_Type_Code|`String`||The payment type unique code. `Required` `Filter(eq;like)` `ORD` |
|Is_Active|`Boolean`||Indicates wheather the payment type is active and usable for choosing in new documents. `Required` `Default(true)` `Filter(eq)` `Introduced in version 19.1` |
|Payment_Type_Name|`MultilanguageString`||The name of this PaymentType. `Required` `Filter(like)` `ORD` |
|System_Type|`SystemType?`|Allowed: `CH`, `CD`, `BT`, `TK`, `CK`, `U1`, `U2`, `U3`, `PK`, `IU`, `DG`, `OT`|Not null only when this is one of the system payment types. CS=Cash; CD=By Card; BT=Bank Transfer. |
