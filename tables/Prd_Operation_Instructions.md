# Table Prd_Operation_Instructions

Long (full) instructions for performing an operation. The operations point to the instructions and one instruction can be used for different operations. Entity: Prd_Operation_Instructions

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Id|`Guid`|`PK`, Readonly||
|Description|`String`||Short description or notes for the instructions. `Filter(like)` |
|Instructions|`Byte[]`|`BLOB`|The operation instructions in OLE format. |
