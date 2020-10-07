# Systems.Core.WebHosts

Contains the names and https certificates of the different host names used to host sites. Entity: Sys_Web_Hosts (Introduced in version 19.1.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Core.WebHosts.md#Id) | guid |  
| [CertificateContents](Systems.Core.WebHosts.md#CertificateContents) | byte[] (nullable) | The contents of the web host certificate. null means to use the server system certificate. 
| [CertificateExpiryDate](Systems.Core.WebHosts.md#CertificateExpiryDate) | date (nullable) | The expiry date of the certificate. Can be used to track the expiration of the web host certificates. When null, the expiry date was not provided by the user, when uploading the certificate. [Filter(multi eq)] 
| [CertificateOriginalFilename](Systems.Core.WebHosts.md#CertificateOriginalFilename) | string (nullable) | The original name of the file, used to upload the certificate. Used only for reference purposes. When null, means that the user did not provide that information when uploading the certificate. [Filter(eq;like)] 
| [CertificatePassword](Systems.Core.WebHosts.md#CertificatePassword) | string (nullable) | The password, which should be used to decrypt the certificate. null when the certificate has no password or the system certificate is used. 
| [CertificateType](Systems.Core.WebHosts.md#CertificateType) | string | The type of certificate uploaded. Currently, only PFX is supported. [Required] [Default("PFX")] [Filter(multi eq)] 
| [Notes](Systems.Core.WebHosts.md#Notes) | string (nullable) | Notes for this WebHost. 
| [Name](Systems.Core.WebHosts.md#Name) | string | The unique Internet name of the host. Should NOT include protocol name and should NOT include any forward slashes. This is just the dot-separated host name. [Required] [Filter(multi eq;like)] 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### CertificateContents

> The contents of the web host certificate. null means to use the server system certificate.

_Type_: **byte[] (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### CertificateExpiryDate

> The expiry date of the certificate. Can be used to track the expiration of the web host certificates. When null, the expiry date was not provided by the user, when uploading the certificate. [Filter(multi eq)]

_Type_: **date (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### CertificateOriginalFilename

> The original name of the file, used to upload the certificate. Used only for reference purposes. When null, means that the user did not provide that information when uploading the certificate. [Filter(eq;like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### CertificatePassword

> The password, which should be used to decrypt the certificate. null when the certificate has no password or the system certificate is used.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### CertificateType

> The type of certificate uploaded. Currently, only PFX is supported. [Required] [Default("PFX")] [Filter(multi eq)]

_Type_: **string**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **PFX**  

### Notes

> Notes for this WebHost.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Name

> The unique Internet name of the host. Should NOT include protocol name and should NOT include any forward slashes. This is just the dot-separated host name. [Required] [Filter(multi eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Systems.Core.WebHosts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Core.WebHosts erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Systems.Core.WebHosts erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Core_WebHosts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Core_WebHosts?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Sys_Web_Hosts?$top=10>

