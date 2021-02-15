---
uid: Applications.PersonalData.ProcessingConsents
---
# Applications.PersonalData.ProcessingConsents Entity

Consents of data subjects for processing of their personal data. Entity: Pdm_Processing_Consents (Introduced in version 18.2)

Default Display Text Format:  
_{ParentName:T}_  
Default Search Member:  
_ParentName_  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [AllowAddress](Applications.PersonalData.ProcessingConsents.md#allowaddress) | boolean | Allows the processing of the physical address. [Required] [Default(false)] [Filter(eq)] 
| [AllowBasicData](Applications.PersonalData.ProcessingConsents.md#allowbasicdata) | boolean | Allows the processing of basic (usually public) data: Name, AgeGroup21+, public profile picture, etc. [Required] [Default(false)] [Filter(eq)] 
| [AllowEmail](Applications.PersonalData.ProcessingConsents.md#allowemail) | boolean | Allows the processing of the email address. [Required] [Default(false)] [Filter(eq)] 
| [AllowOtherData](Applications.PersonalData.ProcessingConsents.md#allowotherdata) | string (nullable) | Comma-separated list of other types of data, which was allowed for processing with this consent. [Filter(eq)] 
| [AllowPhone](Applications.PersonalData.ProcessingConsents.md#allowphone) | boolean | Allows the processing of the telephone number. [Required] [Default(false)] [Filter(eq)] 
| [ConsentImage](Applications.PersonalData.ProcessingConsents.md#consentimage) | byte[] (nullable) | If not null, it is a graphical image, containing additional information for the consent. 
| [ConsentText](Applications.PersonalData.ProcessingConsents.md#consenttext) | string (nullable) | The actual text of the consent. [Filter(like)] 
| [ConsentType](Applications.PersonalData.ProcessingConsents.md#consenttype) | [ConsentType](Applications.PersonalData.ProcessingConsents.md#consenttype) | The way the consent was given. O=Online; I=Implicit; V=Verbal; W=Written; E=Email; T=Other (should be stated in Notes). [Required] [Filter(eq)] 
| [GivenOnUtc](Applications.PersonalData.ProcessingConsents.md#givenonutc) | datetime | The date and time (in Utc), when the consent was given. [Required] [Filter(ge;le)] 
| [Id](Applications.PersonalData.ProcessingConsents.md#id) | guid |  
| [IsActive](Applications.PersonalData.ProcessingConsents.md#isactive) | boolean | Whether the consent is active or retracted. Once retracted, the consent record cannot be modified again and a new consent should be given. [Required] [Default(true)] [Filter(eq)] 
| [IsChild](Applications.PersonalData.ProcessingConsents.md#ischild) | boolean | Specifies whether the data subject is child, according to the local regulations. General regulations treat all persons below the age of 16 as child. [Required] [Default(false)] [Filter(eq)] 
| [Notes](Applications.PersonalData.ProcessingConsents.md#notes) | string (nullable) | Notes for this ProcessingConsent. 
| [ParentEmail](Applications.PersonalData.ProcessingConsents.md#parentemail) | string (nullable) | When a parental rights holder gives a consent for a child, contains the email of the parent. [Filter(like)] 
| [ParentName](Applications.PersonalData.ProcessingConsents.md#parentname) | string (nullable) | When a parental rights holder gives a consent for a child, contains the name of the parent. [Filter(eq;like)] 
| [ParentPhone](Applications.PersonalData.ProcessingConsents.md#parentphone) | string (nullable) | When a parental rights holder gives a consent for a child, contains the phone number of the parent. [Filter(like)] 
| [RetractedOnUtc](Applications.PersonalData.ProcessingConsents.md#retractedonutc) | datetime (nullable) | The date and time (in Utc), when the consent was retracted. Null if the consent is not retracted. [Filter(ge;le)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Person](Applications.PersonalData.ProcessingConsents.md#person) | [Persons](General.Contacts.Persons.md) (nullable) | The person, for which the consent is given. Null when the consent is given by an online user, which is still not linked to a specific person record. [Filter(multi eq)] |
| [PersonalDataProcess](Applications.PersonalData.ProcessingConsents.md#personaldataprocess) | [PersonalDataProcesses](Applications.PersonalData.PersonalDataProcesses.md) (nullable) | The process, which will be used to process the data. Null when the process is unknown, or there are multiple processes (not recommended) processing the data, listed in the Notes. [Filter(multi eq)] |
| [User](Applications.PersonalData.ProcessingConsents.md#user) | [Users](Systems.Security.Users.md) | The login user, for which the consent is given. Null when a consent is entered for a natural person, not through online user. [Required] [Filter(multi eq)] |


## Attribute Details

### AllowAddress

Allows the processing of the physical address. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### AllowBasicData

Allows the processing of basic (usually public) data: Name, AgeGroup21+, public profile picture, etc. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### AllowEmail

Allows the processing of the email address. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### AllowOtherData

Comma-separated list of other types of data, which was allowed for processing with this consent. [Filter(eq)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### AllowPhone

Allows the processing of the telephone number. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### ConsentImage

If not null, it is a graphical image, containing additional information for the consent.

_Type_: **byte[] (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ConsentText

The actual text of the consent. [Filter(like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### ConsentType

The way the consent was given. O=Online; I=Implicit; V=Verbal; W=Written; E=Email; T=Other (should be stated in Notes). [Required] [Filter(eq)]

_Type_: **[ConsentType](Applications.PersonalData.ProcessingConsents.md#consenttype)**  
Allowed values for the [ConsentType](Applications.PersonalData.ProcessingConsents.md#consenttype) data attribute  
_Allowed Values (Applications.PersonalData.ProcessingConsentsRepository.ConsentType Enum Members)_  

| Value | Description |
| ---- | --- |
| Online | Online value. Stored as 'O'. <br /> _Database Value:_ 'O' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Online' |
| Implicit | Implicit value. Stored as 'I'. <br /> _Database Value:_ 'I' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Implicit' |
| Verbal | Verbal value. Stored as 'V'. <br /> _Database Value:_ 'V' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Verbal' |
| Written | Written value. Stored as 'W'. <br /> _Database Value:_ 'W' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'Written' |
| Email | Email value. Stored as 'E'. <br /> _Database Value:_ 'E' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'Email' |
| Other | Other value. Stored as 'T'. <br /> _Database Value:_ 'T' <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'Other' |

_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### GivenOnUtc

The date and time (in Utc), when the consent was given. [Required] [Filter(ge;le)]

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

Whether the consent is active or retracted. Once retracted, the consent record cannot be modified again and a new consent should be given. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### IsChild

Specifies whether the data subject is child, according to the local regulations. General regulations treat all persons below the age of 16 as child. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Notes

Notes for this ProcessingConsent.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ParentEmail

When a parental rights holder gives a consent for a child, contains the email of the parent. [Filter(like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### ParentName

When a parental rights holder gives a consent for a child, contains the name of the parent. [Filter(eq;like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### ParentPhone

When a parental rights holder gives a consent for a child, contains the phone number of the parent. [Filter(like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### RetractedOnUtc

The date and time (in Utc), when the consent was retracted. Null if the consent is not retracted. [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  


## Reference Details

### Person

The person, for which the consent is given. Null when the consent is given by an online user, which is still not linked to a specific person record. [Filter(multi eq)]

_Type_: **[Persons](General.Contacts.Persons.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### PersonalDataProcess

The process, which will be used to process the data. Null when the process is unknown, or there are multiple processes (not recommended) processing the data, listed in the Notes. [Filter(multi eq)]

_Type_: **[PersonalDataProcesses](Applications.PersonalData.PersonalDataProcesses.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### User

The login user, for which the consent is given. Null when a consent is entered for a natural person, not through online user. [Required] [Filter(multi eq)]

_Type_: **[Users](Systems.Security.Users.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Applications.PersonalData.ProcessingConsents erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.PersonalData.ProcessingConsents erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_PersonalData_ProcessingConsents?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_PersonalData_ProcessingConsents?$top=10>

