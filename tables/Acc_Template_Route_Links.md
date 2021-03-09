# Table Acc_Template_Route_Links

When specified denotes that another route uses the template, initially bound to one route. Entity: Acc_Template_Route_Links

## Owner Tables Hierarchy

* [Wf_Routes](Wf_Routes.md)
* [Gen_Document_Types](Gen_Document_Types.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Template_Route_Link_Id](#template_route_link_id)|`uniqueidentifier` `PK`||
|[Route_Id](#route_id)|`uniqueidentifier` |Route for which the specified template will be activated|
|[Template_Id](#template_id)|`uniqueidentifier` |Template that will be activated for the specified route|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Template_Route_Link_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Route_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Template_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


