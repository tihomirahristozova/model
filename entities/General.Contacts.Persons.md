# General.Contacts.Persons

Personal records. Requires related party record. Entity: Cm_Persons

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.Contacts.Persons.md#Id) | guid |  
| [IsActive](General.Contacts.Persons.md#IsActive) | boolean | Specifies whether the current party is active in the system or not [Required] 
| [PartyCreationTime](General.Contacts.Persons.md#PartyCreationTime) | datetime (nullable) | Date and time when the Party was created. 
| [PartyCreationUser](General.Contacts.Persons.md#PartyCreationUser) | string (nullable) | Login name of the user, who created the Party. 
| [DefaultProductCodingSystemId](General.Contacts.Persons.md#DefaultProductCodingSystemId) | guid (nullable) |  
| [GLN](General.Contacts.Persons.md#GLN) | string (nullable) | Global Location Number used by EDI systems 
| [PartyNotes](General.Contacts.Persons.md#PartyNotes) | string (nullable) | Notes for this Party 
| [ParentPartyId](General.Contacts.Persons.md#ParentPartyId) | guid (nullable) |  
| [PartyCode](General.Contacts.Persons.md#PartyCode) | string | The unique code of the Party [Required] 
| [PartyName](General.Contacts.Persons.md#PartyName) | [MultilanguageString](../data-types/MultilanguageString.md) | The name of the party [Required] 
| [PartyType](General.Contacts.Persons.md#PartyType) | [General.Contacts.PartiesRepository.PartyType](General.Contacts.Persons.md#PartyType) | Type of party. Currently supported are P=Person, C=Company, S=Store, L=Company Location, V=Division [Required] 
| [PartyUniqueNumber](General.Contacts.Persons.md#PartyUniqueNumber) | string (nullable) | Unique number of the party (National number for persons, Registration number for companies) 
| [PartyUpdateTime](General.Contacts.Persons.md#PartyUpdateTime) | datetime (nullable) | Date and time when the Party was last updated. 
| [PartyUpdateUser](General.Contacts.Persons.md#PartyUpdateUser) | string (nullable) | Login name of the user, who last updated the Party. 
| [BirthDate](General.Contacts.Persons.md#BirthDate) | datetime (nullable) | Birth date. null means unknown. [Filter(ge;le)] 
| [City](General.Contacts.Persons.md#City) | [MultilanguageString](../data-types/MultilanguageString.md) (nullable) | City from the legal registration address for the person. [Filter(like)] 
| [CreationTime](General.Contacts.Persons.md#CreationTime) | datetime (nullable) | Date and time when the Person was created. [Filter(ge;le)] [ReadOnly] 
| [CreationUser](General.Contacts.Persons.md#CreationUser) | string (nullable) | Login name of the user, who created the Person. [Filter(like)] [ReadOnly] 
| [FirstName](General.Contacts.Persons.md#FirstName) | [MultilanguageString](../data-types/MultilanguageString.md) (nullable) | First name of the person. [Filter(eq;like)] 
| [Gender](General.Contacts.Persons.md#Gender) | [General.Contacts.PersonsRepository.Gender](General.Contacts.Persons.md#Gender) (nullable) | Person gender. M=Male;F=Female;null=not known/not provided. [Filter(eq)] 
| [LastName](General.Contacts.Persons.md#LastName) | [MultilanguageString](../data-types/MultilanguageString.md) (nullable) | Last name of the person. [Filter(eq;like)] 
| [MiddleName](General.Contacts.Persons.md#MiddleName) | [MultilanguageString](../data-types/MultilanguageString.md) (nullable) | Middle name of the person. [Filter(eq;like)] 
| [NationalNumber](General.Contacts.Persons.md#NationalNumber) | string (nullable) | Government assigned unique personal number. null means unknown. [Filter(eq;like)] 
| [Notes](General.Contacts.Persons.md#Notes) | string (nullable) | Internal notes for the person. 
| [PassportIssuingDate](General.Contacts.Persons.md#PassportIssuingDate) | datetime (nullable) | Date of issuing the passport. null means unknown. [Filter(ge;le)] 
| [PassportNumber](General.Contacts.Persons.md#PassportNumber) | string (nullable) | Current passport number. null means unknown. [Filter(eq)] 
| [Title](General.Contacts.Persons.md#Title) | [MultilanguageString](../data-types/MultilanguageString.md) (nullable) | The persons title. It may be one of the standard titles - Mr., Mrs., etc., but it can also contains professional or academic qualification. 
| [UpdateTime](General.Contacts.Persons.md#UpdateTime) | datetime (nullable) | Date and time when the Person was last updated. [Filter(ge;le)] [ReadOnly] 
| [UpdateUser](General.Contacts.Persons.md#UpdateUser) | string (nullable) | Login name of the user, who last updated the Person. [Filter(like)] [ReadOnly] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AdministrativeRegion](General.Contacts.Persons.md#AdministrativeRegion) | [General.Geography.AdministrativeRegions](General.Geography.AdministrativeRegions.md) (nullable) | The administrative region in which the party is situated. |
| [Area](General.Contacts.Persons.md#Area) | [General.Geography.Areas](General.Geography.Areas.md) (nullable) | The area in which the party is situated. |
| [DefaultProductCodingSystem](General.Contacts.Persons.md#DefaultProductCodingSystem) | [General.Products.CodingSystems](General.Products.CodingSystems.md) (nullable) | When not null, specifies coding system for products, which is required by the party. The coding system is used primarily for document printouts and document import/exports. |
| [ParentParty](General.Contacts.Persons.md#ParentParty) | [General.Contacts.Parties](General.Contacts.Parties.md) (nullable) | Organizational unit (branch from the hierarchy of all parties) to which this party is referred to |
| [Nationality](General.Contacts.Persons.md#Nationality) | [General.Geography.Countries](General.Geography.Countries.md) (nullable) | Person's nationality. null means the default (same as enterprise) nationality. [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| ActivityTimeIntervals | [General.Contacts.ActivityTimeIntervals](General.Contacts.ActivityTimeIntervals.md) | List of [ActivityTimeInterval](General.Contacts.ActivityTimeIntervals.md) child objects, based on the [General.Contacts.ActivityTimeInterval.Party](General.Contacts.ActivityTimeIntervals.md#Party) back reference 
| ContactMechanisms | [General.Contacts.PartyContactMechanisms](General.Contacts.PartyContactMechanisms.md) | List of [PartyContactMechanism](General.Contacts.PartyContactMechanisms.md) child objects, based on the [General.Contacts.PartyContactMechanism.Party](General.Contacts.PartyContactMechanisms.md#Party) back reference 
| Customers | [Crm.Customers](Crm.Customers.md) | List of [Customer](Crm.Customers.md) child objects, based on the [Crm.Customer.Party](Crm.Customers.md#Party) back reference 
| Dealers | [Crm.Dealers](Crm.Dealers.md) | List of [Dealer](Crm.Dealers.md) child objects, based on the [Crm.Dealer.Party](Crm.Dealers.md#Party) back reference 
| Distributors | [Crm.Distributors](Crm.Distributors.md) | List of [Distributor](Crm.Distributors.md) child objects, based on the [Crm.Distributor.Party](Crm.Distributors.md#Party) back reference 
| TargetGroupMembers | [Crm.Marketing.TargetGroupMembers](Crm.Marketing.TargetGroupMembers.md) | List of [TargetGroupMember](Crm.Marketing.TargetGroupMembers.md) child objects, based on the [Crm.Marketing.TargetGroupMember.Party](Crm.Marketing.TargetGroupMembers.md#Party) back reference 
| BankAccounts | [General.Contacts.PartyBankAccounts](General.Contacts.PartyBankAccounts.md) | List of [PartyBankAccount](General.Contacts.PartyBankAccounts.md) child objects, based on the [General.Contacts.PartyBankAccount.Party](General.Contacts.PartyBankAccounts.md#Party) back reference 
| Pictures | [General.Contacts.PartyPictures](General.Contacts.PartyPictures.md) | List of [PartyPicture](General.Contacts.PartyPictures.md) child objects, based on the [General.Contacts.PartyPicture.Party](General.Contacts.PartyPictures.md#Party) back reference 
| Suppliers | [Logistics.Procurement.Suppliers](Logistics.Procurement.Suppliers.md) | List of [Supplier](Logistics.Procurement.Suppliers.md) child objects, based on the [Logistics.Procurement.Supplier.Party](Logistics.Procurement.Suppliers.md#Party) back reference 
| CompanyEmployees | [General.Contacts.CompanyEmployees](General.Contacts.CompanyEmployees.md) | List of [CompanyEmployee](General.Contacts.CompanyEmployees.md) child objects, based on the [General.Contacts.CompanyEmployee.Person](General.Contacts.CompanyEmployees.md#Person) back reference 
| SalesPersons | [Crm.SalesPersons](Crm.SalesPersons.md) | List of [SalesPerson](Crm.SalesPersons.md) child objects, based on the [Crm.SalesPerson.Person](Crm.SalesPersons.md#Person) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### IsActive

> Specifies whether the current party is active in the system or not [Required]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### PartyCreationTime

> Date and time when the Party was created.

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### PartyCreationUser

> Login name of the user, who created the Party.

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### DefaultProductCodingSystemId

_Type_: **guid (nullable)**  
_Supported Filters_: **EqualsIn**  
_Supports Order By_: **False**  

### GLN

> Global Location Number used by EDI systems

_Type_: **string (nullable)**  
_Supported Filters_: **EqualsIn**  
_Supports Order By_: **False**  

### PartyNotes

> Notes for this Party

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ParentPartyId

_Type_: **guid (nullable)**  
_Supported Filters_: **EqualsIn**  
_Supports Order By_: **False**  

### PartyCode

> The unique code of the Party [Required]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### PartyName

> The name of the party [Required]

_Type_: **[MultilanguageString](../data-types/MultilanguageString.md)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### PartyType

> Type of party. Currently supported are P=Person, C=Company, S=Store, L=Company Location, V=Division [Required]

_Type_: **[General.Contacts.PartiesRepository.PartyType](General.Contacts.Persons.md#PartyType)**  
Allowed values for the [PartyType](General.Contacts.Parties.md#PartyType) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Company | Company value. Stored as 'C'. <br /> _Database Value:_ 'C' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Company' |
| CompanyLocation | CompanyLocation value. Stored as 'L'. <br /> _Database Value:_ 'L' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'CompanyLocation' |
| Person | Person value. Stored as 'P'. <br /> _Database Value:_ 'P' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Person' |
| Store | Store value. Stored as 'S'. <br /> _Database Value:_ 'S' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'Store' |
| CompanyDivision | CompanyDivision value. Stored as 'V'. <br /> _Database Value:_ 'V' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'CompanyDivision' |

_Supported Filters_: **EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **Person**  

### PartyUniqueNumber

> Unique number of the party (National number for persons, Registration number for companies)

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### PartyUpdateTime

> Date and time when the Party was last updated.

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### PartyUpdateUser

> Login name of the user, who last updated the Party.

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### BirthDate

> Birth date. null means unknown. [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### City

> City from the legal registration address for the person. [Filter(like)]

_Type_: **[MultilanguageString](../data-types/MultilanguageString.md) (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### CreationTime

> Date and time when the Person was created. [Filter(ge;le)] [ReadOnly]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### CreationUser

> Login name of the user, who created the Person. [Filter(like)] [ReadOnly]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### FirstName

> First name of the person. [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types/MultilanguageString.md) (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Gender

> Person gender. M=Male;F=Female;null=not known/not provided. [Filter(eq)]

_Type_: **[General.Contacts.PersonsRepository.Gender](General.Contacts.Persons.md#Gender) (nullable)**  
Allowed values for the [Gender](General.Contacts.Persons.md#Gender) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Female | Female value. Stored as 'F'. <br /> _Database Value:_ 'F' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Female' |
| Male | Male value. Stored as 'M'. <br /> _Database Value:_ 'M' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Male' |

_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### LastName

> Last name of the person. [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types/MultilanguageString.md) (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### MiddleName

> Middle name of the person. [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types/MultilanguageString.md) (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### NationalNumber

> Government assigned unique personal number. null means unknown. [Filter(eq;like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Notes

> Internal notes for the person.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PassportIssuingDate

> Date of issuing the passport. null means unknown. [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### PassportNumber

> Current passport number. null means unknown. [Filter(eq)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### Title

> The persons title. It may be one of the standard titles - Mr., Mrs., etc., but it can also contains professional or academic qualification.

_Type_: **[MultilanguageString](../data-types/MultilanguageString.md) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### UpdateTime

> Date and time when the Person was last updated. [Filter(ge;le)] [ReadOnly]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### UpdateUser

> Login name of the user, who last updated the Person. [Filter(like)] [ReadOnly]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  


## Reference Details

### AdministrativeRegion

> The administrative region in which the party is situated.

_Type_: **[General.Geography.AdministrativeRegions](General.Geography.AdministrativeRegions.md) (nullable)**  
_Supported Filters_: **EqualsIn**  
_Supports Order By_: **False**  

### Area

> The area in which the party is situated.

_Type_: **[General.Geography.Areas](General.Geography.Areas.md) (nullable)**  
_Supported Filters_: **EqualsIn**  
_Supports Order By_: **False**  

### DefaultProductCodingSystem

> When not null, specifies coding system for products, which is required by the party. The coding system is used primarily for document printouts and document import/exports.

_Type_: **[General.Products.CodingSystems](General.Products.CodingSystems.md) (nullable)**  
_Supported Filters_: **EqualsIn**  
_Supports Order By_: **False**  

### ParentParty

> Organizational unit (branch from the hierarchy of all parties) to which this party is referred to

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md) (nullable)**  
_Supported Filters_: **EqualsIn**  
_Supports Order By_: **False**  

### Nationality

> Person's nationality. null means the default (same as enterprise) nationality. [Filter(multi eq)]

_Type_: **[General.Geography.Countries](General.Geography.Countries.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=General.Contacts.Persons erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Contacts.Persons erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.Contacts.Persons erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Contacts_Persons?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Contacts_Persons?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Cm_Persons?$top=10>

