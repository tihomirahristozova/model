# Table Sys_Object_Files

Contains files attached to objects. Entity: Sys_Object_Files

# Aggregate Hierarchy

* [Sys_Objects](Sys_Objects.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Object_File_Id|`Guid`|`PK`, Readonly||
|Content_Location|`ContentLocation`|Allowed: `EMB`, `URL`, `FSL`|The location of the file contents. EMB=Embedded in the database; URL=Internet URL; FSL=File system link. `Required` `Default("EMB")` `Filter(multi eq)` `Introduced in version 20.1` |
|Creation_Time_Utc|`DateTime`||Time (in UTC), when the file was created. `Required` `Default(NowUtc)` `Introduced in version 20.1` |
|Embedded_File_Contents|`Byte[]`|`BLOB`|Contains the contents of the file, when it is embedded in the database. null for linked files. |
|File_Name|`String`||The file name of the linked or embedded file. `Required` `Filter(eq;like)` |
|Last_Update_Time_Utc|`DateTime`||Time (in UTC), when the file was last updated. `Required` `Default(NowUtc)` `Introduced in version 20.1` |
|Linked_File_Path|`String`||When the file is linked, contains the full path (including the file name) to the linked file. null for embedded files. `Filter(eq;like)` |
|Media_Height|`Int32?`||Used (non-null) only for media files. Specifies the width for displaying the media. `Introduced in version 20.1` |
|Media_Type|`String`||For media files, contains the Media Type as per the IANA registry (formerly known as the MIME Type). null for non-media files. `Introduced in version 20.1` |
|Media_Width|`Int32?`||Used (non-null) only for media files. Specifies the width for displaying the media. `Introduced in version 20.1` |
|Notes|`String`||User notes for the file attachment. |
|Purpose_Code|`String`||Code, designating the usage purpose of the file. The meaning of each code is up to the application with the exception of 'default/image', which is standartised as the default image for many types of objects. `Filter(eq)` |
|Section|`String`||A section name used to group files. `Introduced in version 21.1.1.84` |
