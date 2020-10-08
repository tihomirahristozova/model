---
uid: Systems.Core.ObjectFiles
---
# Systems.Core.ObjectFiles

Contains files attached to objects. Entity: Sys_Object_Files

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Core.ObjectFiles.md#Id) | guid |  
| [ContentLocation](Systems.Core.ObjectFiles.md#ContentLocation) | [Systems.Core.ObjectFilesRepository.ContentLocation](Systems.Core.ObjectFiles.md#ContentLocation) | The location of the file contents. EMB=Embedded in the database; URL=Internet URL; FSL=File system link. [Required] [Default("EMB")] (Introduced in version 20.1.100.0) 
| [CreationTimeUtc](Systems.Core.ObjectFiles.md#CreationTimeUtc) | datetime | Time (in UTC), when the file was created. [Required] [Default(NowUtc)] (Introduced in version 20.1.100.0) 
| [EmbeddedFileContents](Systems.Core.ObjectFiles.md#EmbeddedFileContents) | byte[] (nullable) | Contains the contents of the file, when it is embedded in the database. null for linked files. 
| [FileName](Systems.Core.ObjectFiles.md#FileName) | string | The file name of the linked or embedded file. [Required] [Filter(eq;like)] 
| [LastUpdateTimeUtc](Systems.Core.ObjectFiles.md#LastUpdateTimeUtc) | datetime | Time (in UTC), when the file was last updated. [Required] [Default(NowUtc)] (Introduced in version 20.1.100.0) 
| [LinkedFilePath](Systems.Core.ObjectFiles.md#LinkedFilePath) | string (nullable) | When the file is linked, contains the full path (including the file name) to the linked file. null for embedded files. [Filter(eq;like)] 
| [MediaHeight](Systems.Core.ObjectFiles.md#MediaHeight) | int32 (nullable) | Used (non-null) only for media files. Specifies the width for displaying the media. (Introduced in version 20.1.100.0) 
| [MediaType](Systems.Core.ObjectFiles.md#MediaType) | string (nullable) | For media files, contains the Media Type as per the IANA registry (formerly known as the MIME Type). null for non-media files. (Introduced in version 20.1.100.0) 
| [MediaWidth](Systems.Core.ObjectFiles.md#MediaWidth) | int32 (nullable) | Used (non-null) only for media files. Specifies the width for displaying the media. (Introduced in version 20.1.100.0) 
| [Notes](Systems.Core.ObjectFiles.md#Notes) | string (nullable) | User notes for the file attachment. 
| [PurposeCode](Systems.Core.ObjectFiles.md#PurposeCode) | string (nullable) | Code, designating the usage purpose of the file. The meaning of each code is up to the application with the exception of 'default/image', which is standartised as the default image for many types of objects. [Filter(eq)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CreationUser](Systems.Core.ObjectFiles.md#CreationUser) | [Systems.Security.Users](Systems.Security.Users.md) (nullable) | The user, who created the file record. null if it is unknown. [Filter(multi eq)] (Introduced in version 20.1.100.0) |
| [LastUpdateUser](Systems.Core.ObjectFiles.md#LastUpdateUser) | [Systems.Security.Users](Systems.Security.Users.md) (nullable) | The user, who performed the last update to the file record. null if it is unknown. [Filter(multi eq)] (Introduced in version 20.1.100.0) |
| [Object](Systems.Core.ObjectFiles.md#Object) | [Systems.Core.ExtensibleDataObjects](Systems.Core.ExtensibleDataObjects.md) | The object to which the file is attached. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### ContentLocation

> The location of the file contents. EMB=Embedded in the database; URL=Internet URL; FSL=File system link. [Required] [Default("EMB")] (Introduced in version 20.1.100.0)

_Type_: **[Systems.Core.ObjectFilesRepository.ContentLocation](Systems.Core.ObjectFiles.md#ContentLocation)**  
Allowed values for the [ContentLocation](Systems.Core.ObjectFiles.md#ContentLocation) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Embedded | Embedded value. Stored as 'EMB'. <br /> _Database Value:_ 'EMB' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Embedded' |
| InternetUrl | InternetUrl value. Stored as 'URL'. <br /> _Database Value:_ 'URL' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'InternetUrl' |
| FileSystemLink | FileSystemLink value. Stored as 'FSL'. <br /> _Database Value:_ 'FSL' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'FileSystemLink' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Embedded**  

### CreationTimeUtc

> Time (in UTC), when the file was created. [Required] [Default(NowUtc)] (Introduced in version 20.1.100.0)

_Type_: **datetime**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTimeUtc**  

### EmbeddedFileContents

> Contains the contents of the file, when it is embedded in the database. null for linked files.

_Type_: **byte[] (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### FileName

> The file name of the linked or embedded file. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### LastUpdateTimeUtc

> Time (in UTC), when the file was last updated. [Required] [Default(NowUtc)] (Introduced in version 20.1.100.0)

_Type_: **datetime**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTimeUtc**  

### LinkedFilePath

> When the file is linked, contains the full path (including the file name) to the linked file. null for embedded files. [Filter(eq;like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### MediaHeight

> Used (non-null) only for media files. Specifies the width for displaying the media. (Introduced in version 20.1.100.0)

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### MediaType

> For media files, contains the Media Type as per the IANA registry (formerly known as the MIME Type). null for non-media files. (Introduced in version 20.1.100.0)

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### MediaWidth

> Used (non-null) only for media files. Specifies the width for displaying the media. (Introduced in version 20.1.100.0)

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Notes

> User notes for the file attachment.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PurposeCode

> Code, designating the usage purpose of the file. The meaning of each code is up to the application with the exception of 'default/image', which is standartised as the default image for many types of objects. [Filter(eq)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  


## Reference Details

### CreationUser

> The user, who created the file record. null if it is unknown. [Filter(multi eq)] (Introduced in version 20.1.100.0)

_Type_: **[Systems.Security.Users](Systems.Security.Users.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### LastUpdateUser

> The user, who performed the last update to the file record. null if it is unknown. [Filter(multi eq)] (Introduced in version 20.1.100.0)

_Type_: **[Systems.Security.Users](Systems.Security.Users.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Object

> The object to which the file is attached. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Systems.Core.ExtensibleDataObjects](Systems.Core.ExtensibleDataObjects.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Systems.Core.ObjectFiles erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Core.ObjectFiles erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Systems.Core.ObjectFiles erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Core_ObjectFiles?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Core_ObjectFiles?$top=10>

