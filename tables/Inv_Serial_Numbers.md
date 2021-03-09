# Table Inv_Serial_Numbers

Serial numbers, used by the items. Rows are created on first occurrence of the serial number in a document. Rows can be deleted after deleting the last occurence of the serial number in a document. Entity: Inv_Serial_Numbers

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`|Unique serial number Id|
|[Product_Id](#product_id)|`uniqueidentifier` |The product, to which the serial number is bound|
|[Serial_Number](#serial_number)|`nvarchar(40)` |The serial number text|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Serial_Number

| Property | Value |
| - | - |
|Type|nvarchar(40)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


