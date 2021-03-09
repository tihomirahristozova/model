# Table Sys_Object_Files

Contains files attached to objects. Entity: Sys_Object_Files

## Owner Tables Hierarchy

* [Sys_Objects](Sys_Objects.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Object_File_Id](#object_file_id)|`uniqueidentifier` `PK`|.|
|[Object_Id](#object_id)|`uniqueidentifier` |The object to which the file is attached|
|[Purpose_Code](#purpose_code)|`nvarchar(32)` |Code, designating the usage purpose of the file. The meaning of each code is up to the application with the exception of 'default/image', which is standartised as the default image for many types of objects.|
|[Embedded_File_Contents](#embedded_file_contents)|`varbinary` |Contains the contents of the file, when it is embedded in the database. NULL for linked files|
|[Linked_File_Path](#linked_file_path)|`nvarchar(1024)` |When the file is linked, contains the full path (including the file name) to the linked file. NULL for embedded files|
|[File_Name](#file_name)|`nvarchar(254)` |The file name of the linked or embedded file|
|[Notes](#notes)|`nvarchar(2147483647)` |User notes for the file attachment|
|[Row_Version](#row_version)|`timestamp` ||
|[Content_Location](#content_location)|`nvarchar(3)` Allowed: `EMB`, `URL`, `FSL`|The location of the file contents. EMB=Embedded in the database; URL=Internet URL; FSL=File system link.|
|[Media_Type](#media_type)|`nvarchar(128)` |For media files, contains the Media Type as per the IANA registry (formerly known as the MIME Type). NULL for non-media files.|
|[Media_Width](#media_width)|`int` |Used (non-null) only for media files. Specifies the width for displaying the media.|
|[Media_Height](#media_height)|`int` |Used (non-null) only for media files. Specifies the width for displaying the media.|
|[Creation_Time_Utc](#creation_time_utc)|`datetime` |Time (in UTC), when the file was created.|
|[Last_Update_Time_Utc](#last_update_time_utc)|`datetime` |Time (in UTC), when the file was last updated.|
|[Creation_User_Id](#creation_user_id)|`uniqueidentifier` |The user, who created the file record. NULL if it is unknown.|
|[Last_Update_User_Id](#last_update_user_id)|`uniqueidentifier` |The user, who performed the last update to the file record. NULL if it is unknown.|
|[Section](#section)|`nvarchar(64)` |A section name used to group files|

## Columns

### Object_File_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Object_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Purpose_Code

| Property | Value |
| - | - |
|Type|nvarchar(32)|

### Embedded_File_Contents

| Property | Value |
| - | - |
|Type|varbinary|

### Linked_File_Path

| Property | Value |
| - | - |
|Type|nvarchar(1024)|

### File_Name

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

### Content_Location

| Property | Value |
| - | - |
|Type|nvarchar(3)|

### Media_Type

| Property | Value |
| - | - |
|Type|nvarchar(128)|

### Media_Width

| Property | Value |
| - | - |
|Type|int|

### Media_Height

| Property | Value |
| - | - |
|Type|int|

### Creation_Time_Utc

| Property | Value |
| - | - |
|Type|datetime|

### Last_Update_Time_Utc

| Property | Value |
| - | - |
|Type|datetime|

### Creation_User_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Last_Update_User_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Section

| Property | Value |
| - | - |
|Type|nvarchar(64)|


