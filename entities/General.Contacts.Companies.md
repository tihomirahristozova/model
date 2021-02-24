---
uid: General.Contacts.Companies
---
# General.Contacts.Companies Entity

Contains company definitions. Entity: Cm_Companies

Default Display Text Format:  
_{PartyCode}: {PartyName:T}_  
Default Search Member:  
_PartyCode_  

## [Aggregate Tree](xref:aggregates)  
* [General.Contacts.Companies](General.Contacts.Companies.md)  
  * [General.Contacts.CompanyDepartments](General.Contacts.CompanyDepartments.md)  
  * [Crm.Customers](Crm.Customers.md)  
    * [Crm.CustomerProducts](Crm.CustomerProducts.md)  
  * [Crm.Dealers](Crm.Dealers.md)  
  * [Crm.Distributors](Crm.Distributors.md)  
  * [General.PartyApplicableLegislations](General.PartyApplicableLegislations.md)  
  * [General.PartyLocationNumbers](General.PartyLocationNumbers.md)  
  * [General.Contacts.ActivityTimeIntervals](General.Contacts.ActivityTimeIntervals.md)  
  * [General.Contacts.PartyContactMechanisms](General.Contacts.PartyContactMechanisms.md)  
  * [General.Contacts.PartyBankAccounts](General.Contacts.PartyBankAccounts.md)  
  * [General.Contacts.PartyPictures](General.Contacts.PartyPictures.md)  
  * [Logistics.Procurement.Suppliers](Logistics.Procurement.Suppliers.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [BranchNumber](General.Contacts.Companies.md#branchnumber) | int32 | Branch number of the company. Companies with equal names and/or registration numbers can be inserted only if their branch numbers are different. [Required] [Default(0)] [Filter(eq)] 
| [City](General.Contacts.Companies.md#city) | [MultilanguageString](../data-types.md#multilanguagestring) (nullable) | The city in which the company is registered. [Filter(like)] 
| [CreationTime](General.Contacts.Companies.md#creationtime) | datetime (nullable) | Date and time when the Company was created. [Filter(ge;le)] [ReadOnly] 
| [CreationUser](General.Contacts.Companies.md#creationuser) | string (nullable) | Login name of the user, who created the Company. [Filter(like)] [ReadOnly] 
| [GLN](General.Contacts.Companies.md#gln) | string (nullable) | Global Location Number used by EDI systems. [Filter(multi eq)] [ORD] (Inherited from [Parties](General.Contacts.Parties.md)) 
| [Id](General.Contacts.Companies.md#id) | guid |  
| [IsActive](General.Contacts.Companies.md#isactive) | boolean | Specifies whether the current party is active in the system or not. [Required] [Default(true)] [Filter(eq)] (Inherited from [Parties](General.Contacts.Parties.md)) 
| [IsVATCashReporting<br />Registered](General.Contacts.Companies.md#isvatcashreportingregistered) | boolean | When true, specifies that the company uses the special VAT Cash Reporting Mode. [Required] [Default(false)] 
| [IsVATRegistered](General.Contacts.Companies.md#isvatregistered) | boolean | Determines wheather the company is included in VAT registers. [Required] [Default(false)] 
| [Name](General.Contacts.Companies.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) (nullable) | The name of this Company. [Filter(eq;like)] [ORD] 
| [PartyCode](General.Contacts.Companies.md#partycode) | string | The unique code of the party. [Required] [Filter(eq;like)] [ORD] [ReadOnly] (Inherited from [Parties](General.Contacts.Parties.md)) 
| [PartyCreationTime](General.Contacts.Companies.md#partycreationtime) | datetime (nullable) | Date and time when the Party was created. [Filter(ge;le)] [ReadOnly] (Inherited from [Parties](General.Contacts.Parties.md)) 
| [PartyCreationUser](General.Contacts.Companies.md#partycreationuser) | string (nullable) | Login name of the user, who created the Party. [Filter(like)] [ReadOnly] (Inherited from [Parties](General.Contacts.Parties.md)) 
| [PartyName](General.Contacts.Companies.md#partyname) | [MultilanguageString](../data-types.md#multilanguagestring) | The name of the party. [Required] [Filter(eq;like)] [ORD] (Inherited from [Parties](General.Contacts.Parties.md)) 
| [PartyNotes](General.Contacts.Companies.md#partynotes) | string (nullable) | Notes for this Party. (Inherited from [Parties](General.Contacts.Parties.md)) 
| [PartyType](General.Contacts.Companies.md#partytype) | [PartyType](General.Contacts.Companies.md#partytype) | Type of party. Currently supported are P=Person, C=Company, S=Store, L=Company Location, V=Division. [Required] [Default("P")] [Filter(multi eq)] (Inherited from [Parties](General.Contacts.Parties.md)) 
| [PartyUniqueNumber](General.Contacts.Companies.md#partyuniquenumber) | string (nullable) | Unique number of the party (National number for persons, Registration number for companies). [Filter(eq;like)] [ReadOnly] (Inherited from [Parties](General.Contacts.Parties.md)) 
| [PartyUpdateTime](General.Contacts.Companies.md#partyupdatetime) | datetime (nullable) | Date and time when the Party was last updated. [Filter(ge;le)] [ReadOnly] (Inherited from [Parties](General.Contacts.Parties.md)) 
| [PartyUpdateUser](General.Contacts.Companies.md#partyupdateuser) | string (nullable) | Login name of the user, who last updated the Party. [Filter(like)] [ReadOnly] (Inherited from [Parties](General.Contacts.Parties.md)) 
| [RegistrationNumber](General.Contacts.Companies.md#registrationnumber) | string (nullable) | Unique, government-assigned registration number. null means unknown. [Filter(eq;like)] [ORD] 
| [RegistrationPrimaryAddress](General.Contacts.Companies.md#registrationprimaryaddress) | [MultilanguageString](../data-types.md#multilanguagestring) (nullable) | The primary registration address of the company. [Filter(like)] 
| [RegistrationType](General.Contacts.Companies.md#registrationtype) | [MultilanguageString](../data-types.md#multilanguagestring) (nullable) | Legal registration type - like LTD., PLC, etc. null means unknown. [Filter(eq)] 
| [RegistrationVATNumber](General.Contacts.Companies.md#registrationvatnumber) | string (nullable) | VAT registration number where applicable. null means that VAT number is not applicable or unknown. [Filter(eq)] [ORD] 
| [ResponsiblePersonName](General.Contacts.Companies.md#responsiblepersonname) | [MultilanguageString](../data-types.md#multilanguagestring) (nullable) | Primary responsible person of the company. null means unknown. [Filter(like)] 
| [UpdateTime](General.Contacts.Companies.md#updatetime) | datetime (nullable) | Date and time when the Company was last updated. [Filter(ge;le)] [ReadOnly] 
| [UpdateUser](General.Contacts.Companies.md#updateuser) | string (nullable) | Login name of the user, who last updated the Company. [Filter(like)] [ReadOnly] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AdministrativeRegion](General.Contacts.Companies.md#administrativeregion) | [AdministrativeRegions](General.Geography.AdministrativeRegions.md) (nullable) | The administrative region in which the party is situated. [Filter(multi eq)] (Inherited from [Parties](General.Contacts.Parties.md)) |
| [Area](General.Contacts.Companies.md#area) | [Areas](General.Geography.Areas.md) (nullable) | The area in which the party is situated. [Filter(multi eq)] (Inherited from [Parties](General.Contacts.Parties.md)) |
| [Country](General.Contacts.Companies.md#country) | [Countries](General.Geography.Countries.md) (nullable) | The country, where the company is registered. [Filter(multi eq)] |
| [DefaultProductCodingSystem](General.Contacts.Companies.md#defaultproductcodingsystem) | [CodingSystems](General.Products.CodingSystems.md) (nullable) | When not null, specifies coding system for products, which is required by the party. The coding system is used primarily for document printouts and document import/exports. [Filter(multi eq)] (Inherited from [Parties](General.Contacts.Parties.md)) |
| [ParentParty](General.Contacts.Companies.md#parentparty) | [Parties](General.Contacts.Parties.md) (nullable) | Organizational unit (branch from the hierarchy of all parties) to which this party is referred to. [Filter(multi eq)] (Inherited from [Parties](General.Contacts.Parties.md)) |
| [RegistrationResponsible<br />Person](General.Contacts.Companies.md#registrationresponsibleperson) | [Persons](General.Contacts.Persons.md) (nullable) | The personal record of the primary responsible person as per registration. null means unknown. [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| ActivityTimeIntervals | [ActivityTimeIntervals](General.Contacts.ActivityTimeIntervals.md) | List of [ActivityTimeInterval](General.Contacts.ActivityTimeIntervals.md) child objects, based on the [General.Contacts.ActivityTimeInterval.Party](General.Contacts.ActivityTimeIntervals.md#party) back reference (Inherited from [Parties](General.Contacts.Parties.md)) 
| ApplicableLegislations | [PartyApplicableLegislations](General.PartyApplicableLegislations.md) | List of [PartyApplicable<br />Legislation](General.PartyApplicable<br />Legislations.md) child objects, based on the [General.PartyApplicableLegislation.Party](General.PartyApplicable<br />Legislations.md#party) back reference (Inherited from [Parties](General.Contacts.Parties.md)) 
| BankAccounts | [PartyBankAccounts](General.Contacts.PartyBankAccounts.md) | List of [PartyBankAccount](General.Contacts.PartyBankAccounts.md) child objects, based on the [General.Contacts.PartyBankAccount.Party](General.Contacts.PartyBankAccounts.md#party) back reference (Inherited from [Parties](General.Contacts.Parties.md)) 
| ContactMechanisms | [PartyContactMechanisms](General.Contacts.PartyContactMechanisms.md) | List of [PartyContactMechanism](General.Contacts.PartyContactMechanisms.md) child objects, based on the [General.Contacts.PartyContactMechanism.Party](General.Contacts.PartyContactMechanisms.md#party) back reference (Inherited from [Parties](General.Contacts.Parties.md)) 
| Customers | [Customers](Crm.Customers.md) | List of [Customer](Crm.Customers.md) child objects, based on the [Crm.Customer.Party](Crm.Customers.md#party) back reference (Inherited from [Parties](General.Contacts.Parties.md)) 
| Dealers | [Dealers](Crm.Dealers.md) | List of [Dealer](Crm.Dealers.md) child objects, based on the [Crm.Dealer.Party](Crm.Dealers.md#party) back reference (Inherited from [Parties](General.Contacts.Parties.md)) 
| Departments | [CompanyDepartments](General.Contacts.CompanyDepartments.md) | List of [CompanyDepartment](General.Contacts.CompanyDepartments.md) child objects, based on the [General.Contacts.CompanyDepartment.Company](General.Contacts.CompanyDepartments.md#company) back reference 
| Distributors | [Distributors](Crm.Distributors.md) | List of [Distributor](Crm.Distributors.md) child objects, based on the [Crm.Distributor.Party](Crm.Distributors.md#party) back reference (Inherited from [Parties](General.Contacts.Parties.md)) 
| LocationNumbers | [PartyLocationNumbers](General.PartyLocationNumbers.md) | List of [PartyLocationNumber](General.PartyLocationNumbers.md) child objects, based on the [General.PartyLocationNumber.Party](General.PartyLocationNumbers.md#party) back reference (Inherited from [Parties](General.Contacts.Parties.md)) 
| Pictures | [PartyPictures](General.Contacts.PartyPictures.md) | List of [PartyPicture](General.Contacts.PartyPictures.md) child objects, based on the [General.Contacts.PartyPicture.Party](General.Contacts.PartyPictures.md#party) back reference (Inherited from [Parties](General.Contacts.Parties.md)) 
| Suppliers | [Suppliers](Logistics.Procurement.Suppliers.md) | List of [Supplier](Logistics.Procurement.Suppliers.md) child objects, based on the [Logistics.Procurement.Supplier.Party](Logistics.Procurement.Suppliers.md#party) back reference (Inherited from [Parties](General.Contacts.Parties.md)) 


## Attribute Details

### BranchNumber

Branch number of the company. Companies with equal names and/or registration numbers can be inserted only if their branch numbers are different. [Required] [Default(0)] [Filter(eq)]

_Type_: **int32**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### City

The city in which the company is registered. [Filter(like)]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring) (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### CreationTime

Date and time when the Company was created. [Filter(ge;le)] [ReadOnly]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### CreationUser

Login name of the user, who created the Company. [Filter(like)] [ReadOnly]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### GLN

Global Location Number used by EDI systems. [Filter(multi eq)] [ORD] (Inherited from [Parties](General.Contacts.Parties.md))

_Type_: **string (nullable)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **True**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

Specifies whether the current party is active in the system or not. [Required] [Default(true)] [Filter(eq)] (Inherited from [Parties](General.Contacts.Parties.md))

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### IsVATCashReportingRegistered

When true, specifies that the company uses the special VAT Cash Reporting Mode. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### IsVATRegistered

Determines wheather the company is included in VAT registers. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Name

The name of this Company. [Filter(eq;like)] [ORD]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring) (nullable)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### PartyCode

The unique code of the party. [Required] [Filter(eq;like)] [ORD] [ReadOnly] (Inherited from [Parties](General.Contacts.Parties.md))

_Type_: **string**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### PartyCreationTime

Date and time when the Party was created. [Filter(ge;le)] [ReadOnly] (Inherited from [Parties](General.Contacts.Parties.md))

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### PartyCreationUser

Login name of the user, who created the Party. [Filter(like)] [ReadOnly] (Inherited from [Parties](General.Contacts.Parties.md))

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### PartyName

The name of the party. [Required] [Filter(eq;like)] [ORD] (Inherited from [Parties](General.Contacts.Parties.md))

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### PartyNotes

Notes for this Party. (Inherited from [Parties](General.Contacts.Parties.md))

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PartyType

Type of party. Currently supported are P=Person, C=Company, S=Store, L=Company Location, V=Division. [Required] [Default("P")] [Filter(multi eq)] (Inherited from [Parties](General.Contacts.Parties.md))

_Type_: **[PartyType](General.Contacts.Companies.md#partytype)**  
Allowed values for the [PartyType](General.Contacts.Parties.md#partytype) data attribute  
_Allowed Values (General.Contacts.PartiesRepository.PartyType Enum Members)_  

| Value | Description |
| ---- | --- |
| Company | Company value. Stored as 'C'. <br /> _Database Value:_ 'C' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Company' |
| CompanyLocation | CompanyLocation value. Stored as 'L'. <br /> _Database Value:_ 'L' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'CompanyLocation' |
| Person | Person value. Stored as 'P'. <br /> _Database Value:_ 'P' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Person' |
| Store | Store value. Stored as 'S'. <br /> _Database Value:_ 'S' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'Store' |
| CompanyDivision | CompanyDivision value. Stored as 'V'. <br /> _Database Value:_ 'V' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'CompanyDivision' |

_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **Person**  

### PartyUniqueNumber

Unique number of the party (National number for persons, Registration number for companies). [Filter(eq;like)] [ReadOnly] (Inherited from [Parties](General.Contacts.Parties.md))

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### PartyUpdateTime

Date and time when the Party was last updated. [Filter(ge;le)] [ReadOnly] (Inherited from [Parties](General.Contacts.Parties.md))

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### PartyUpdateUser

Login name of the user, who last updated the Party. [Filter(like)] [ReadOnly] (Inherited from [Parties](General.Contacts.Parties.md))

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### RegistrationNumber

Unique, government-assigned registration number. null means unknown. [Filter(eq;like)] [ORD]

_Type_: **string (nullable)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### RegistrationPrimaryAddress

The primary registration address of the company. [Filter(like)]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring) (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### RegistrationType

Legal registration type - like LTD., PLC, etc. null means unknown. [Filter(eq)]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring) (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### RegistrationVATNumber

VAT registration number where applicable. null means that VAT number is not applicable or unknown. [Filter(eq)] [ORD]

_Type_: **string (nullable)**  
_Indexed_: **True**  
_Supported Filters_: **Equals**  
_Supports Order By_: **True**  

### ResponsiblePersonName

Primary responsible person of the company. null means unknown. [Filter(like)]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring) (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### UpdateTime

Date and time when the Company was last updated. [Filter(ge;le)] [ReadOnly]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### UpdateUser

Login name of the user, who last updated the Company. [Filter(like)] [ReadOnly]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  


## Reference Details

### AdministrativeRegion

The administrative region in which the party is situated. [Filter(multi eq)] (Inherited from [Parties](General.Contacts.Parties.md))

_Type_: **[AdministrativeRegions](General.Geography.AdministrativeRegions.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Area

The area in which the party is situated. [Filter(multi eq)] (Inherited from [Parties](General.Contacts.Parties.md))

_Type_: **[Areas](General.Geography.Areas.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Country

The country, where the company is registered. [Filter(multi eq)]

_Type_: **[Countries](General.Geography.Countries.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Back-End Default Expression:_  
`obj.Transaction.CurrentEnterpriseCompany.Company.Country`

_Front-End Recalc Expressions:_  
`obj.Transaction.CurrentEnterpriseCompany.Company.Country`
### DefaultProductCodingSystem

When not null, specifies coding system for products, which is required by the party. The coding system is used primarily for document printouts and document import/exports. [Filter(multi eq)] (Inherited from [Parties](General.Contacts.Parties.md))

_Type_: **[CodingSystems](General.Products.CodingSystems.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ParentParty

Organizational unit (branch from the hierarchy of all parties) to which this party is referred to. [Filter(multi eq)] (Inherited from [Parties](General.Contacts.Parties.md))

_Type_: **[Parties](General.Contacts.Parties.md) (nullable)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### RegistrationResponsiblePerson

The personal record of the primary responsible person as per registration. null means unknown. [Filter(multi eq)]

_Type_: **[Persons](General.Contacts.Persons.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=General.Contacts.Companies erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Contacts.Companies erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Contacts_Companies?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Contacts_Companies?$top=10>

