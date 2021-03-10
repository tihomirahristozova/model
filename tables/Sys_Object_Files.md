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


Object_File_Id


.


.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|yes|
|Order in Primary Key|1|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|NewGuid|
|Derived From|[Sys_Object_Files](Sys_Object_Files.md).[Object_File_Id](Sys_Object_Files.md#object_file_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Object_Id


Object_Id


The object to which the file is attached


The object to which the file is attached

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Sys_Objects](Sys_Objects.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Object_Files](Sys_Object_Files.md).[Object_Id](Sys_Object_Files.md#object_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Purpose_Code


Purpose_Code


Code, designating the usage purpose of the file. The meaning of each code is up to the application with the exception of 'default/image', which is standartised as the default image for many types of objects.


Code, designating the usage purpose of the file. The meaning of each code is up to the application with the exception of 'default/image', which is standartised as the default image for many types of objects.

| Property | Value |
| - | - |
|Type|nvarchar(32)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Object_Files](Sys_Object_Files.md).[Purpose_Code](Sys_Object_Files.md#purpose_code)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|32|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Embedded_File_Contents


Embedded_File_Contents


Contains the contents of the file, when it is embedded in the database. NULL for linked files


Contains the contents of the file, when it is embedded in the database. NULL for linked files

| Property | Value |
| - | - |
|Type|varbinary|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Object_Files](Sys_Object_Files.md).[Embedded_File_Contents](Sys_Object_Files.md#embedded_file_contents)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Linked_File_Path


Linked_File_Path


When the file is linked, contains the full path (including the file name) to the linked file. NULL for embedded files


When the file is linked, contains the full path (including the file name) to the linked file. NULL for embedded files

| Property | Value |
| - | - |
|Type|nvarchar(1024)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Object_Files](Sys_Object_Files.md).[Linked_File_Path](Sys_Object_Files.md#linked_file_path)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|1024|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|Like|None|no|no|

### File_Name


File_Name


The file name of the linked or embedded file


The file name of the linked or embedded file

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Object_Files](Sys_Object_Files.md).[File_Name](Sys_Object_Files.md#file_name)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|254|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|Like|None|no|no|

### Notes


Notes


User notes for the file attachment


User notes for the file attachment

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None, IsLongString|
|Default Value|None|
|Derived From|[Sys_Object_Files](Sys_Object_Files.md).[Notes](Sys_Object_Files.md#notes)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|2147483647|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Row_Version


Row_Version

| Property | Value |
| - | - |
|Type|timestamp|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Object_Files](Sys_Object_Files.md).[Row_Version](Sys_Object_Files.md#row_version)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Content_Location


Content_Location


The location of the file contents. EMB=Embedded in the database; URL=Internet URL; FSL=File system link.


The location of the file contents. EMB=Embedded in the database; URL=Internet URL; FSL=File system link.

| Property | Value |
| - | - |
|Type|nvarchar(3)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`EMB`, `URL`, `FSL`|
|Default Value|EMB|
|Derived From|[Sys_Object_Files](Sys_Object_Files.md).[Content_Location](Sys_Object_Files.md#content_location)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|3|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Media_Type


Media_Type


For media files, contains the Media Type as per the IANA registry (formerly known as the MIME Type). NULL for non-media files.


For media files, contains the Media Type as per the IANA registry (formerly known as the MIME Type). NULL for non-media files.

| Property | Value |
| - | - |
|Type|nvarchar(128)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Object_Files](Sys_Object_Files.md).[Media_Type](Sys_Object_Files.md#media_type)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|128|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Media_Width


Media_Width


Used (non-null) only for media files. Specifies the width for displaying the media.


Used (non-null) only for media files. Specifies the width for displaying the media.

| Property | Value |
| - | - |
|Type|int|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Object_Files](Sys_Object_Files.md).[Media_Width](Sys_Object_Files.md#media_width)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Media_Height


Media_Height


Used (non-null) only for media files. Specifies the width for displaying the media.


Used (non-null) only for media files. Specifies the width for displaying the media.

| Property | Value |
| - | - |
|Type|int|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Object_Files](Sys_Object_Files.md).[Media_Height](Sys_Object_Files.md#media_height)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Creation_Time_Utc


Creation_Time_Utc


Time (in UTC), when the file was created.


Time (in UTC), when the file was created.

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|CurrentDateTimeUtc|
|Derived From|[Sys_Object_Files](Sys_Object_Files.md).[Creation_Time_Utc](Sys_Object_Files.md#creation_time_utc)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Last_Update_Time_Utc


Last_Update_Time_Utc


Time (in UTC), when the file was last updated.


Time (in UTC), when the file was last updated.

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|CurrentDateTimeUtc|
|Derived From|[Sys_Object_Files](Sys_Object_Files.md).[Last_Update_Time_Utc](Sys_Object_Files.md#last_update_time_utc)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Creation_User_Id


Creation_User_Id


The user, who created the file record. NULL if it is unknown.


The user, who created the file record. NULL if it is unknown.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Sec_Users](Sec_Users.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Object_Files](Sys_Object_Files.md).[Creation_User_Id](Sys_Object_Files.md#creation_user_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Last_Update_User_Id


Last_Update_User_Id


The user, who performed the last update to the file record. NULL if it is unknown.


The user, who performed the last update to the file record. NULL if it is unknown.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Sec_Users](Sec_Users.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Object_Files](Sys_Object_Files.md).[Last_Update_User_Id](Sys_Object_Files.md#last_update_user_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Section


Section


A section name used to group files


A section name used to group files

| Property | Value |
| - | - |
|Type|nvarchar(64)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sys_Object_Files](Sys_Object_Files.md).[Section](Sys_Object_Files.md#section)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|64|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|


