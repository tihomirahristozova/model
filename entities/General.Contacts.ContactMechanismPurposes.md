---
uid: General.Contacts.ContactMechanismPurposes
---
# General.Contacts.ContactMechanismPurposes Entity

Contains user-defined purposes for processing contact mechanisms. Used for personal data management. Entity: Cm_Contact_Mechanism_Purposes (Introduced in version 18.2)

Default Display Text Format:  
_{Code}: {Name:T}_  
Default Search Member:  
_Code_  

## [Aggregate Tree](xref:aggregates)  
* [General.Contacts.ContactMechanismPurposes](General.Contacts.ContactMechanismPurposes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](General.Contacts.ContactMechanismPurposes.md#code) | string | The unique code of the ContactMechanismPurpos. [Required] [Filter(eq;like)] [ORD] 
| [ContactMechanismType](General.Contacts.ContactMechanismPurposes.md#contactmechanismtype) | [ContactMechanismType](General.Contacts.ContactMechanismPurposes.md#contactmechanismtype) (nullable) | When specified, allows the purpose to be specified only for contact mechanisms of the specified type. [Filter(multi eq)] 
| [Description](General.Contacts.ContactMechanismPurposes.md#description) | string (nullable) | The description of this ContactMechanismPurpos. [Filter(like)] 
| [Id](General.Contacts.ContactMechanismPurposes.md#id) | guid |  
| [Name](General.Contacts.ContactMechanismPurposes.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | Name of the contact mechanism purpose (Multilanguage). [Required] [Filter(like)] 


## Attribute Details

### Code

The unique code of the ContactMechanismPurpos. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### ContactMechanismType

When specified, allows the purpose to be specified only for contact mechanisms of the specified type. [Filter(multi eq)]

_Type_: **[ContactMechanismType](General.Contacts.ContactMechanismPurposes.md#contactmechanismtype) (nullable)**  
Allowed values for the [ContactMechanismType](General.Contacts.ContactMechanisms.md#contactmechanismtype) data attribute  
_Allowed Values (General.Contacts.ContactMechanismsRepository.ContactMechanismType Enum Members)_  

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

The description of this ContactMechanismPurpos. [Filter(like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Name of the contact mechanism purpose (Multilanguage). [Required] [Filter(like)]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=General.Contacts.ContactMechanismPurposes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Contacts.ContactMechanismPurposes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Contacts_ContactMechanismPurposes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Contacts_ContactMechanismPurposes?$top=10>

