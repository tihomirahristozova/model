# Table Inv_Serial_Numbers

Serial numbers, used by the items. Rows are created on first occurrence of the serial number in a document. Rows can be deleted after deleting the last occurence of the serial number in a document. Entity: Inv_Serial_Numbers

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Id|`Guid`|`PK`, Readonly||
|Serial_Number|`String`||The serial number text. `Required` `Filter(multi eq;like)` |
