# General.Contacts.ContactMechanismPurposes

Contains user-defined purposes for processing contact mechanisms. Used for personal data management. Entity: Cm_Contact_Mechanism_Purposes (Introduced in version 18.2.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.Contacts.ContactMechanismPurposes.md#Id) | guid |  
| [Code](General.Contacts.ContactMechanismPurposes.md#Code) | string | The unique code of the ContactMechanismPurpos. [Required] [Filter(eq;like)] [ORD] 
| [ContactMechanismType](General.Contacts.ContactMechanismPurposes.md#ContactMechanismType) | [General.Contacts.ContactMechanismsRepository.ContactMechanismType](General.Contacts.ContactMechanismPurposes.md#ContactMechanismType) (nullable) | When specified, allows the purpose to be specified only for contact mechanisms of the specified type. [Filter(multi eq)] 
| [Description](General.Contacts.ContactMechanismPurposes.md#Description) | string (nullable) | The description of this ContactMechanismPurpos. [Filter(like)] 
| [Name](General.Contacts.ContactMechanismPurposes.md#Name) | [MultilanguageString](../data-types/MultilanguageString.md) | Name of the contact mechanism purpose (Multilanguage). [Required] [Filter(like)] 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Code

> The unique code of the ContactMechanismPurpos. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### ContactMechanismType

> When specified, allows the purpose to be specified only for contact mechanisms of the specified type. [Filter(multi eq)]

_Type_: **[General.Contacts.ContactMechanismsRepository.ContactMechanismType](General.Contacts.ContactMechanismPurposes.md#ContactMechanismType) (nullable)**  
Allowed values for the [ContactMechanismType](General.Contacts.ContactMechanisms.md#ContactMechanismType) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Address | Address value. Stored as 'A'. <br /> _Database Value:_ 'A' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Address' |
| Mail | Mail value. Stored as 'E'. <br /> _Database Value:_ 'E' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Mail' |
| Fax | Fax value. Stored as 'F'. <br /> _Database Value:_ 'F' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Fax' |
| MobilePhone | MobilePhone value. Stored as 'M'. <br /> _Database Value:_ 'M' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'MobilePhone' |
| Other | Other value. Stored as 'O'. <br /> _Database Value:_ 'O' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'Other' |
| Telephone | Telephone value. Stored as 'T'. <br /> _Database Value:_ 'T' <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'Telephone' |
| WebSite | WebSite value. Stored as 'W'. <br /> _Database Value:_ 'W' <br /> _Model Value:_ 6 <br /> _Domain API Value:_ 'WebSite' |

_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Description

> The description of this ContactMechanismPurpos. [Filter(like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Name

> Name of the contact mechanism purpose (Multilanguage). [Required] [Filter(like)]

_Type_: **[MultilanguageString](../data-types/MultilanguageString.md)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=General.Contacts.ContactMechanismPurposes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Contacts.ContactMechanismPurposes erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.Contacts.ContactMechanismPurposes erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Contacts_ContactMechanismPurposes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Contacts_ContactMechanismPurposes?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Cm_Contact_Mechanism_Purposes?$top=10>

