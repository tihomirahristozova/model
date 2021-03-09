# Table Gen_Document_Type_Security_Conditions

Provides rules to conditionally secure new documents. Entity: Gen_Document_Type_Security_Conditions

## Summary

| Name | Type | Description |
| - | - | --- |
|[Document_Type_Security_Condition_Id](#document_type_security_condition_id)|`uniqueidentifier` `PK`||
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` |The document type, whose documents will be secured by the current rule.|
|[Condition_Filter_Xml](#condition_filter_xml)|`nvarchar(2147483647)` |Specifies the documents, for which the current rule is applicable. The XML filter is compared against new documents and the rule is applicable when they match.|
|[Priority](#priority)|`tinyint` Allowed: `1`, `2`, `3`, `4`, `5`|Priority of the rule against other rules, which are also applicable. Only the highest priority rule is selected.|
|[Document_Access_Key_Id](#document_access_key_id)|`uniqueidentifier` |The access key, which will be used to secure new documents, when this rule is selected.|
|[Description](#description)|`nvarchar(254)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Document_Type_Security_Condition_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Condition_Filter_Xml

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Priority

| Property | Value |
| - | - |
|Type|tinyint|

### Document_Access_Key_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Description

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


