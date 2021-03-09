# Table Log_Logistic_Unit_Specifications

Specification of a logistic unit. The database can contain any kind of specification, but most client applications and integrated methods process GS1 specifications (application codes). Entity: Log_Logistic_Unit_Specifications (Introduced in version 21.1.0.77)

## Owner Tables Hierarchy

* [Log_Logistic_Units](Log_Logistic_Units.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Logistic_Unit_Specification_Id](#logistic_unit_specification_id)|`uniqueidentifier` `PK`||
|[Logistic_Unit_Id](#logistic_unit_id)|`uniqueidentifier` |The logistic unit, which is detailed by this specification.|
|[Code](#code)|`nvarchar(32)` |The code of the specification, unique within the logistic unit. It can contain only alphanumeric characters and cannot contain spaces.|
|[Name](#name)|`nvarchar(254)` `ML`|Multi-language name of the specification. For some processing purposes, the name might be contained within the client implementation and not saved to the database (NULL).|
|[Value](#value)|`nvarchar(254)` |Text value of the specification. If this is GS1 specification, it can contain only numbers and letters and cannot contain spaces.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Logistic_Unit_Specification_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Logistic_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Code

| Property | Value |
| - | - |
|Type|nvarchar(32)|

### Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Value

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


