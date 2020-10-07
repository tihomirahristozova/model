# Applications.PersonalData.ProcessingConsents

Consents of data subjects for processing of their personal data. Entity: Pdm_Processing_Consents (Introduced in version 18.2.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.PersonalData.ProcessingConsents.md#Id) | guid |  
| [AllowAddress](Applications.PersonalData.ProcessingConsents.md#AllowAddress) | boolean | Allows the processing of the physical address. [Required] [Default(false)] [Filter(eq)] 
| [AllowBasicData](Applications.PersonalData.ProcessingConsents.md#AllowBasicData) | boolean | Allows the processing of basic (usually public) data: Name, AgeGroup21+, public profile picture, etc. [Required] [Default(false)] [Filter(eq)] 
| [AllowEmail](Applications.PersonalData.ProcessingConsents.md#AllowEmail) | boolean | Allows the processing of the email address. [Required] [Default(false)] [Filter(eq)] 
| [AllowOtherData](Applications.PersonalData.ProcessingConsents.md#AllowOtherData) | string (nullable) | Comma-separated list of other types of data, which was allowed for processing with this consent. [Filter(eq)] 
| [AllowPhone](Applications.PersonalData.ProcessingConsents.md#AllowPhone) | boolean | Allows the processing of the telephone number. [Required] [Default(false)] [Filter(eq)] 
| [ConsentImage](Applications.PersonalData.ProcessingConsents.md#ConsentImage) | byte[] (nullable) | If not null, it is a graphical image, containing additional information for the consent. 
| [ConsentText](Applications.PersonalData.ProcessingConsents.md#ConsentText) | string (nullable) | The actual text of the consent. [Filter(like)] 
| [ConsentType](Applications.PersonalData.ProcessingConsents.md#ConsentType) | [Applications.PersonalData.ProcessingConsentsRepository.ConsentType](Applications.PersonalData.ProcessingConsents.md#ConsentType) | The way the consent was given. O=Online; I=Implicit; V=Verbal; W=Written; E=Email; T=Other (should be stated in Notes). [Required] [Filter(eq)] 
| [GivenOnUtc](Applications.PersonalData.ProcessingConsents.md#GivenOnUtc) | datetime | The date and time (in Utc), when the consent was given. [Required] [Filter(ge;le)] 
| [IsActive](Applications.PersonalData.ProcessingConsents.md#IsActive) | boolean | Whether the consent is active or retracted. Once retracted, the consent record cannot be modified again and a new consent should be given. [Required] [Default(true)] [Filter(eq)] 
| [IsChild](Applications.PersonalData.ProcessingConsents.md#IsChild) | boolean | Specifies whether the data subject is child, according to the local regulations. General regulations treat all persons below the age of 16 as child. [Required] [Default(false)] [Filter(eq)] 
| [Notes](Applications.PersonalData.ProcessingConsents.md#Notes) | string (nullable) | Notes for this ProcessingConsent. 
| [ParentEmail](Applications.PersonalData.ProcessingConsents.md#ParentEmail) | string (nullable) | When a parental rights holder gives a consent for a child, contains the email of the parent. [Filter(like)] 
| [ParentName](Applications.PersonalData.ProcessingConsents.md#ParentName) | string (nullable) | When a parental rights holder gives a consent for a child, contains the name of the parent. [Filter(eq;like)] 
| [ParentPhone](Applications.PersonalData.ProcessingConsents.md#ParentPhone) | string (nullable) | When a parental rights holder gives a consent for a child, contains the phone number of the parent. [Filter(like)] 
| [RetractedOnUtc](Applications.PersonalData.ProcessingConsents.md#RetractedOnUtc) | datetime (nullable) | The date and time (in Utc), when the consent was retracted. Null if the consent is not retracted. [Filter(ge;le)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Person](Applications.PersonalData.ProcessingConsents.md#Person) | [General.Contacts.Persons](General.Contacts.Persons.md) (nullable) | The person, for which the consent is given. Null when the consent is given by an online user, which is still not linked to a specific person record. [Filter(multi eq)] |
| [PersonalDataProcess](Applications.PersonalData.ProcessingConsents.md#PersonalDataProcess) | [Applications.PersonalData.PersonalDataProcesses](Applications.PersonalData.PersonalDataProcesses.md) (nullable) | The process, which will be used to process the data. Null when the process is unknown, or there are multiple processes (not recommended) processing the data, listed in the Notes. [Filter(multi eq)] |
| [User](Applications.PersonalData.ProcessingConsents.md#User) | [Systems.Security.Users](Systems.Security.Users.md) | The login user, for which the consent is given. Null when a consent is entered for a natural person, not through online user. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### AllowAddress

> Allows the processing of the physical address. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### AllowBasicData

> Allows the processing of basic (usually public) data: Name, AgeGroup21+, public profile picture, etc. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### AllowEmail

> Allows the processing of the email address. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### AllowOtherData

> Comma-separated list of other types of data, which was allowed for processing with this consent. [Filter(eq)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### AllowPhone

> Allows the processing of the telephone number. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### ConsentImage

> If not null, it is a graphical image, containing additional information for the consent.

_Type_: **byte[] (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ConsentText

> The actual text of the consent. [Filter(like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### ConsentType

> The way the consent was given. O=Online; I=Implicit; V=Verbal; W=Written; E=Email; T=Other (should be stated in Notes). [Required] [Filter(eq)]

_Type_: **[Applications.PersonalData.ProcessingConsentsRepository.ConsentType](Applications.PersonalData.ProcessingConsents.md#ConsentType)**  
Allowed values for the [ConsentType](Applications.PersonalData.ProcessingConsents.md#ConsentType) data attribute  
_Allowed Values (Enum Members)_  

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

> The date and time (in Utc), when the consent was given. [Required] [Filter(ge;le)]

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### IsActive

> Whether the consent is active or retracted. Once retracted, the consent record cannot be modified again and a new consent should be given. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### IsChild

> Specifies whether the data subject is child, according to the local regulations. General regulations treat all persons below the age of 16 as child. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Notes

> Notes for this ProcessingConsent.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ParentEmail

> When a parental rights holder gives a consent for a child, contains the email of the parent. [Filter(like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### ParentName

> When a parental rights holder gives a consent for a child, contains the name of the parent. [Filter(eq;like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### ParentPhone

> When a parental rights holder gives a consent for a child, contains the phone number of the parent. [Filter(like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### RetractedOnUtc

> The date and time (in Utc), when the consent was retracted. Null if the consent is not retracted. [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  


## Reference Details

### Person

> The person, for which the consent is given. Null when the consent is given by an online user, which is still not linked to a specific person record. [Filter(multi eq)]

_Type_: **[General.Contacts.Persons](General.Contacts.Persons.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### PersonalDataProcess

> The process, which will be used to process the data. Null when the process is unknown, or there are multiple processes (not recommended) processing the data, listed in the Notes. [Filter(multi eq)]

_Type_: **[Applications.PersonalData.PersonalDataProcesses](Applications.PersonalData.PersonalDataProcesses.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### User

> The login user, for which the consent is given. Null when a consent is entered for a natural person, not through online user. [Required] [Filter(multi eq)]

_Type_: **[Systems.Security.Users](Systems.Security.Users.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Applications.PersonalData.ProcessingConsents erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.PersonalData.ProcessingConsents erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.PersonalData.ProcessingConsents erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_PersonalData_ProcessingConsents?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_PersonalData_ProcessingConsents?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Pdm_Processing_Consents?$top=10>

