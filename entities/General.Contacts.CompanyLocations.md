---
uid: General.Contacts.CompanyLocations
---
# General.Contacts.CompanyLocations Entity

Stores company locations. The locations are parties and as such, can be organized hierarchically mixed with other structuring mechanisms. The locations, departments and divisions are parallel and different structuring mechanisms for the companies. Entity: Cm_Company_Locations

Default Display Text Format:  
_{PartyCode}: {PartyName:T}_  
Default Search Member:  
_PartyCode_  

## [Aggregate Tree](xref:aggregates)  
* [General.Contacts.CompanyLocations](General.Contacts.CompanyLocations.md)  
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
| [BillTo](General.Contacts.CompanyLocations.md#billto) | [BillTo](General.Contacts.CompanyLocations.md#billto) (nullable) | If filled indicates which party is billed for the amounts from documents that require payments. This setting is used in CRM module when the company and the location are customers. Possible values: 'C' = Company, 'L' = Company location, null = unidentified. 
| [GLN](General.Contacts.CompanyLocations.md#gln) | string (nullable) | Global Location Number used by EDI systems. [Filter(multi eq)] [ORD] (Inherited from [Parties](General.Contacts.Parties.md)) 
| [Id](General.Contacts.CompanyLocations.md#id) | guid |  
| [IsActive](General.Contacts.CompanyLocations.md#isactive) | boolean | Specifies whether the current party is active in the system or not. [Required] [Default(true)] [Filter(eq)] (Inherited from [Parties](General.Contacts.Parties.md)) 
| [LocationName](General.Contacts.CompanyLocations.md#locationname) | [MultilanguageString](../data-types.md#multilanguagestring) | The name of the company location. [Required] [Filter(eq;like)] 
| [PartyCode](General.Contacts.CompanyLocations.md#partycode) | string | The unique code of the party. [Required] [Filter(eq;like)] [ORD] [ReadOnly] (Inherited from [Parties](General.Contacts.Parties.md)) 
| [PartyCreationTime](General.Contacts.CompanyLocations.md#partycreationtime) | datetime (nullable) | Date and time when the Party was created. [Filter(ge;le)] [ReadOnly] (Inherited from [Parties](General.Contacts.Parties.md)) 
| [PartyCreationUser](General.Contacts.CompanyLocations.md#partycreationuser) | string (nullable) | Login name of the user, who created the Party. [Filter(like)] [ReadOnly] (Inherited from [Parties](General.Contacts.Parties.md)) 
| [PartyName](General.Contacts.CompanyLocations.md#partyname) | [MultilanguageString](../data-types.md#multilanguagestring) | The name of the party. [Required] [Filter(eq;like)] [ORD] (Inherited from [Parties](General.Contacts.Parties.md)) 
| [PartyNotes](General.Contacts.CompanyLocations.md#partynotes) | string (nullable) | Notes for this Party. (Inherited from [Parties](General.Contacts.Parties.md)) 
| [PartyType](General.Contacts.CompanyLocations.md#partytype) | [PartyType](General.Contacts.CompanyLocations.md#partytype) | Type of party. Currently supported are P=Person, C=Company, S=Store, L=Company Location, V=Division. [Required] [Default("P")] [Filter(multi eq)] (Inherited from [Parties](General.Contacts.Parties.md)) 
| [PartyUniqueNumber](General.Contacts.CompanyLocations.md#partyuniquenumber) | string (nullable) | Unique number of the party (National number for persons, Registration number for companies). [Filter(eq;like)] [ReadOnly] (Inherited from [Parties](General.Contacts.Parties.md)) 
| [PartyUpdateTime](General.Contacts.CompanyLocations.md#partyupdatetime) | datetime (nullable) | Date and time when the Party was last updated. [Filter(ge;le)] [ReadOnly] (Inherited from [Parties](General.Contacts.Parties.md)) 
| [PartyUpdateUser](General.Contacts.CompanyLocations.md#partyupdateuser) | string (nullable) | Login name of the user, who last updated the Party. [Filter(like)] [ReadOnly] (Inherited from [Parties](General.Contacts.Parties.md)) 
| [WorkingTime](General.Contacts.CompanyLocations.md#workingtime) | string (nullable) | Textual representation of the working time of the location. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AccessKey](General.Contacts.CompanyLocations.md#accesskey) | [AccessKeys](Systems.Security.AccessKeys.md) (nullable) | The access key, containing the user permissions for this CompanyLocation. Null means that all users have unlimited permissions. [Filter(multi eq)] |
| [AdministrativeRegion](General.Contacts.CompanyLocations.md#administrativeregion) | [AdministrativeRegions](General.Geography.AdministrativeRegions.md) (nullable) | The administrative region in which the party is situated. [Filter(multi eq)] (Inherited from [Parties](General.Contacts.Parties.md)) |
| [Area](General.Contacts.CompanyLocations.md#area) | [Areas](General.Geography.Areas.md) (nullable) | The area in which the party is situated. [Filter(multi eq)] (Inherited from [Parties](General.Contacts.Parties.md)) |
| [Company](General.Contacts.CompanyLocations.md#company) | [Companies](General.Contacts.Companies.md) | The company to which this location belongs. [Required] [Filter(multi eq)] |
| [DefaultProductCodingSystem](General.Contacts.CompanyLocations.md#defaultproductcodingsystem) | [CodingSystems](General.Products.CodingSystems.md) (nullable) | When not null, specifies coding system for products, which is required by the party. The coding system is used primarily for document printouts and document import/exports. [Filter(multi eq)] (Inherited from [Parties](General.Contacts.Parties.md)) |
| [ParentParty](General.Contacts.CompanyLocations.md#parentparty) | [Parties](General.Contacts.Parties.md) (nullable) | Organizational unit (branch from the hierarchy of all parties) to which this party is referred to. [Filter(multi eq)] (Inherited from [Parties](General.Contacts.Parties.md)) |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| ActivityTimeIntervals | [ActivityTimeIntervals](General.Contacts.ActivityTimeIntervals.md) | List of [ActivityTimeInterval](General.Contacts.ActivityTimeIntervals.md) child objects, based on the [General.Contacts.ActivityTimeInterval.Party](General.Contacts.ActivityTimeIntervals.md#party) back reference (Inherited from [Parties](General.Contacts.Parties.md)) 
| ApplicableLegislations | [PartyApplicableLegislations](General.PartyApplicableLegislations.md) | List of [PartyApplicable<br />Legislation](General.PartyApplicable<br />Legislations.md) child objects, based on the [General.PartyApplicableLegislation.Party](General.PartyApplicable<br />Legislations.md#party) back reference (Inherited from [Parties](General.Contacts.Parties.md)) 
| BankAccounts | [PartyBankAccounts](General.Contacts.PartyBankAccounts.md) | List of [PartyBankAccount](General.Contacts.PartyBankAccounts.md) child objects, based on the [General.Contacts.PartyBankAccount.Party](General.Contacts.PartyBankAccounts.md#party) back reference (Inherited from [Parties](General.Contacts.Parties.md)) 
| ContactMechanisms | [PartyContactMechanisms](General.Contacts.PartyContactMechanisms.md) | List of [PartyContactMechanism](General.Contacts.PartyContactMechanisms.md) child objects, based on the [General.Contacts.PartyContactMechanism.Party](General.Contacts.PartyContactMechanisms.md#party) back reference (Inherited from [Parties](General.Contacts.Parties.md)) 
| Customers | [Customers](Crm.Customers.md) | List of [Customer](Crm.Customers.md) child objects, based on the [Crm.Customer.Party](Crm.Customers.md#party) back reference (Inherited from [Parties](General.Contacts.Parties.md)) 
| Dealers | [Dealers](Crm.Dealers.md) | List of [Dealer](Crm.Dealers.md) child objects, based on the [Crm.Dealer.Party](Crm.Dealers.md#party) back reference (Inherited from [Parties](General.Contacts.Parties.md)) 
| Distributors | [Distributors](Crm.Distributors.md) | List of [Distributor](Crm.Distributors.md) child objects, based on the [Crm.Distributor.Party](Crm.Distributors.md#party) back reference (Inherited from [Parties](General.Contacts.Parties.md)) 
| LocationNumbers | [PartyLocationNumbers](General.PartyLocationNumbers.md) | List of [PartyLocationNumber](General.PartyLocationNumbers.md) child objects, based on the [General.PartyLocationNumber.Party](General.PartyLocationNumbers.md#party) back reference (Inherited from [Parties](General.Contacts.Parties.md)) 
| Pictures | [PartyPictures](General.Contacts.PartyPictures.md) | List of [PartyPicture](General.Contacts.PartyPictures.md) child objects, based on the [General.Contacts.PartyPicture.Party](General.Contacts.PartyPictures.md#party) back reference (Inherited from [Parties](General.Contacts.Parties.md)) 
| Suppliers | [Suppliers](Logistics.Procurement.Suppliers.md) | List of [Supplier](Logistics.Procurement.Suppliers.md) child objects, based on the [Logistics.Procurement.Supplier.Party](Logistics.Procurement.Suppliers.md#party) back reference (Inherited from [Parties](General.Contacts.Parties.md)) 


## Attribute Details

### BillTo

If filled indicates which party is billed for the amounts from documents that require payments. This setting is used in CRM module when the company and the location are customers. Possible values: 'C' = Company, 'L' = Company location, null = unidentified.

_Type_: **[BillTo](General.Contacts.CompanyLocations.md#billto) (nullable)**  
Allowed values for the [BillTo](General.Contacts.CompanyLocations.md#billto) data attribute  
_Allowed Values (General.Contacts.CompanyLocationsRepository.BillTo Enum Members)_  

| Value | Description |
| ---- | --- |
| Company | Company value. Stored as 'C'. <br /> _Database Value:_ 'C' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Company' |
| CompanyLocation | CompanyLocation value. Stored as 'L'. <br /> _Database Value:_ 'L' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'CompanyLocation' |

_Supported Filters_: **NotFilterable**  
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

### LocationName

The name of the company location. [Required] [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

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

_Type_: **[PartyType](General.Contacts.CompanyLocations.md#partytype)**  
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

### WorkingTime

Textual representation of the working time of the location.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### AccessKey

The access key, containing the user permissions for this CompanyLocation. Null means that all users have unlimited permissions. [Filter(multi eq)]

_Type_: **[AccessKeys](Systems.Security.AccessKeys.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### AdministrativeRegion

The administrative region in which the party is situated. [Filter(multi eq)] (Inherited from [Parties](General.Contacts.Parties.md))

_Type_: **[AdministrativeRegions](General.Geography.AdministrativeRegions.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Area

The area in which the party is situated. [Filter(multi eq)] (Inherited from [Parties](General.Contacts.Parties.md))

_Type_: **[Areas](General.Geography.Areas.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Company

The company to which this location belongs. [Required] [Filter(multi eq)]

_Type_: **[Companies](General.Contacts.Companies.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### DefaultProductCodingSystem

When not null, specifies coding system for products, which is required by the party. The coding system is used primarily for document printouts and document import/exports. [Filter(multi eq)] (Inherited from [Parties](General.Contacts.Parties.md))

_Type_: **[CodingSystems](General.Products.CodingSystems.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ParentParty

Organizational unit (branch from the hierarchy of all parties) to which this party is referred to. [Filter(multi eq)] (Inherited from [Parties](General.Contacts.Parties.md))

_Type_: **[Parties](General.Contacts.Parties.md) (nullable)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=General.Contacts.CompanyLocations erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Contacts.CompanyLocations erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Contacts_CompanyLocations?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Contacts_CompanyLocations?$top=10>

