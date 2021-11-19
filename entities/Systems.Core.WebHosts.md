---
uid: Systems.Core.WebHosts
---
# Systems.Core.WebHosts Entity

**Namespace:** [Systems.Core](Systems.Core.md)  

Contains the names and https certificates of the different host names used to host sites. Entity: Sys_Web_Hosts (Introduced in version 19.1)

## Default Visualization
Default Display Text Format:  
_{Name}_  
Default Search Members:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Systems.Core.WebHosts](Systems.Core.WebHosts.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CertificateContents](Systems.Core.WebHosts.md#certificatecontents) | byte[] __nullable__ | The contents of the web host certificate. null means to use the server system certificate. 
| [CertificateExpiryDate](Systems.Core.WebHosts.md#certificateexpirydate) | date __nullable__ | The expiry date of the certificate. Can be used to track the expiration of the web host certificates. When null, the expiry date was not provided by the user, when uploading the certificate. `Filter(multi eq)` 
| [CertificateOriginal<br />Filename](Systems.Core.WebHosts.md#certificateoriginalfilename) | string (254) __nullable__ | The original name of the file, used to upload the certificate. Used only for reference purposes. When null, means that the user did not provide that information when uploading the certificate. `Filter(eq;like)` 
| [CertificatePassword](Systems.Core.WebHosts.md#certificatepassword) | string (max) __nullable__ | The password, which should be used to decrypt the certificate. null when the certificate has no password or the system certificate is used. 
| [CertificateType](Systems.Core.WebHosts.md#certificatetype) | string (3) | The type of certificate uploaded. Currently, only PFX is supported. `Required` `Default("PFX")` `Filter(multi eq)` 
| [Id](Systems.Core.WebHosts.md#id) | guid |  
| [Name](Systems.Core.WebHosts.md#name) | string (max) | The unique Internet name of the host. Should NOT include protocol name and should NOT include any forward slashes. This is just the dot-separated host name. `Required` `Filter(multi eq;like)` 
| [Notes](Systems.Core.WebHosts.md#notes) | string (max) __nullable__ | Notes for this WebHost. 


## Attribute Details

### CertificateContents

The contents of the web host certificate. null means to use the server system certificate.

_Type_: **byte[] __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### CertificateExpiryDate

The expiry date of the certificate. Can be used to track the expiration of the web host certificates. When null, the expiry date was not provided by the user, when uploading the certificate. `Filter(multi eq)`

_Type_: **date __nullable__**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### CertificateOriginalFilename

The original name of the file, used to upload the certificate. Used only for reference purposes. When null, means that the user did not provide that information when uploading the certificate. `Filter(eq;like)`

_Type_: **string (254) __nullable__**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### CertificatePassword

The password, which should be used to decrypt the certificate. null when the certificate has no password or the system certificate is used.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### CertificateType

The type of certificate uploaded. Currently, only PFX is supported. `Required` `Default("PFX")` `Filter(multi eq)`

_Type_: **string (3)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Maximum Length_: **3**  
_Default Value_: **PFX**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The unique Internet name of the host. Should NOT include protocol name and should NOT include any forward slashes. This is just the dot-separated host name. `Required` `Filter(multi eq;like)`

_Type_: **string (max)**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### Notes

Notes for this WebHost.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  



## Business Rules

[!list limit=1000 erp.entity=Systems.Core.WebHosts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Systems.Core.WebHosts erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Core_WebHosts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Core_WebHosts?$top=10>

