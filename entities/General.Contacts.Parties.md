---
uid: General.Contacts.Parties
---
# General.Contacts.Parties

Contains base data for different kind of parties - companies, persons, departments, etc.

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [DefaultProductCodingSystemId](General.Contacts.Parties.md#defaultproductcodingsystemid) | guid (nullable) |  
| [GLN](General.Contacts.Parties.md#gln) | string (nullable) | Global Location Number used by EDI systems 
| [IsActive](General.Contacts.Parties.md#isactive) | boolean | Specifies whether the current party is active in the system or not [Required] 
| [ParentPartyId](General.Contacts.Parties.md#parentpartyid) | guid (nullable) |  
| [PartyCode](General.Contacts.Parties.md#partycode) | string | The unique code of the Party [Required] 
| [PartyCreationTime](General.Contacts.Parties.md#partycreationtime) | datetime (nullable) | Date and time when the Party was created. 
| [PartyCreationUser](General.Contacts.Parties.md#partycreationuser) | string (nullable) | Login name of the user, who created the Party. 
| [PartyId](General.Contacts.Parties.md#partyid) | guid |              Gets the Id of the party row, related to the domain object              
| [PartyName](General.Contacts.Parties.md#partyname) | [MultilanguageString](../data-types.md#multilanguagestring) | The name of the party [Required] 
| [PartyNotes](General.Contacts.Parties.md#partynotes) | string (nullable) | Notes for this Party 
| [PartyType](General.Contacts.Parties.md#partytype) | [PartyType](General.Contacts.Parties.md#partytype) | Type of party. Currently supported are P=Person, C=Company, S=Store, L=Company Location, V=Division [Required] 
| [PartyUniqueNumber](General.Contacts.Parties.md#partyuniquenumber) | string (nullable) | Unique number of the party (National number for persons, Registration number for companies) 
| [PartyUpdateTime](General.Contacts.Parties.md#partyupdatetime) | datetime (nullable) | Date and time when the Party was last updated. 
| [PartyUpdateUser](General.Contacts.Parties.md#partyupdateuser) | string (nullable) | Login name of the user, who last updated the Party. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AdministrativeRegion](General.Contacts.Parties.md#administrativeregion) | [General.Geography.AdministrativeRegions](General.Geography.AdministrativeRegions.md) (nullable) | The administrative region in which the party is situated. |
| [Area](General.Contacts.Parties.md#area) | [General.Geography.Areas](General.Geography.Areas.md) (nullable) | The area in which the party is situated. |
| [DefaultProductCodingSystem](General.Contacts.Parties.md#defaultproductcodingsystem) | [General.Products.CodingSystems](General.Products.CodingSystems.md) (nullable) | When not null, specifies coding system for products, which is required by the party. The coding system is used primarily for document printouts and document import/exports. |
| [ParentParty](General.Contacts.Parties.md#parentparty) | [General.Contacts.Parties](General.Contacts.Parties.md) (nullable) | Organizational unit (branch from the hierarchy of all parties) to which this party is referred to |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| ActivityTimeIntervals | [General.Contacts.ActivityTimeIntervals](General.Contacts.ActivityTimeIntervals.md) | List of [ActivityTimeInterval](General.Contacts.ActivityTimeIntervals.md) child objects, based on the [General.Contacts.ActivityTimeInterval.Party](General.Contacts.ActivityTimeIntervals.md#party) back reference 
| BankAccounts | [General.Contacts.PartyBankAccounts](General.Contacts.PartyBankAccounts.md) | List of [PartyBankAccount](General.Contacts.PartyBankAccounts.md) child objects, based on the [General.Contacts.PartyBankAccount.Party](General.Contacts.PartyBankAccounts.md#party) back reference 
| ContactMechanisms | [General.Contacts.PartyContactMechanisms](General.Contacts.PartyContactMechanisms.md) | List of [PartyContactMechanism](General.Contacts.PartyContactMechanisms.md) child objects, based on the [General.Contacts.PartyContactMechanism.Party](General.Contacts.PartyContactMechanisms.md#party) back reference 
| Customers | [Crm.Customers](Crm.Customers.md) | List of [Customer](Crm.Customers.md) child objects, based on the [Crm.Customer.Party](Crm.Customers.md#party) back reference 
| Dealers | [Crm.Dealers](Crm.Dealers.md) | List of [Dealer](Crm.Dealers.md) child objects, based on the [Crm.Dealer.Party](Crm.Dealers.md#party) back reference 
| Distributors | [Crm.Distributors](Crm.Distributors.md) | List of [Distributor](Crm.Distributors.md) child objects, based on the [Crm.Distributor.Party](Crm.Distributors.md#party) back reference 
| Pictures | [General.Contacts.PartyPictures](General.Contacts.PartyPictures.md) | List of [PartyPicture](General.Contacts.PartyPictures.md) child objects, based on the [General.Contacts.PartyPicture.Party](General.Contacts.PartyPictures.md#party) back reference 
| Suppliers | [Logistics.Procurement.Suppliers](Logistics.Procurement.Suppliers.md) | List of [Supplier](Logistics.Procurement.Suppliers.md) child objects, based on the [Logistics.Procurement.Supplier.Party](Logistics.Procurement.Suppliers.md#party) back reference 
| TargetGroupMembers | [Crm.Marketing.TargetGroupMembers](Crm.Marketing.TargetGroupMembers.md) | List of [TargetGroupMember](Crm.Marketing.TargetGroupMembers.md) child objects, based on the [Crm.Marketing.TargetGroupMember.Party](Crm.Marketing.TargetGroupMembers.md#party) back reference 


## Attribute Details

### DefaultProductCodingSystemId

_Type_: **guid (nullable)**  
_Supported Filters_: **EqualsIn**  

### GLN

> Global Location Number used by EDI systems

_Type_: **string (nullable)**  
_Supported Filters_: **EqualsIn**  
_Supports Order By_: **False**  

### IsActive

> Specifies whether the current party is active in the system or not [Required]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### ParentPartyId

_Type_: **guid (nullable)**  
_Supported Filters_: **EqualsIn**  

### PartyCode

> The unique code of the Party [Required]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

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

### PartyId

> Gets the Id of the party row, related to the domain object

_Type_: **guid**  
_Supported Filters_: **NotFilterable**  

### PartyName

> The name of the party [Required]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### PartyNotes

> Notes for this Party

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PartyType

> Type of party. Currently supported are P=Person, C=Company, S=Store, L=Company Location, V=Division [Required]

_Type_: **[PartyType](General.Contacts.Parties.md#partytype)**  
Allowed values for the [PartyType](General.Contacts.Parties.md#partytype) data attribute  
_Allowed Values (General.Contacts.PartiesRepository.PartyType Enum Members)_  

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


## Reference Details

### AdministrativeRegion

> The administrative region in which the party is situated.

_Type_: **[General.Geography.AdministrativeRegions](General.Geography.AdministrativeRegions.md) (nullable)**  
_Supported Filters_: **EqualsIn**  

### Area

> The area in which the party is situated.

_Type_: **[General.Geography.Areas](General.Geography.Areas.md) (nullable)**  
_Supported Filters_: **EqualsIn**  

### DefaultProductCodingSystem

> When not null, specifies coding system for products, which is required by the party. The coding system is used primarily for document printouts and document import/exports.

_Type_: **[General.Products.CodingSystems](General.Products.CodingSystems.md) (nullable)**  
_Supported Filters_: **EqualsIn**  

### ParentParty

> Organizational unit (branch from the hierarchy of all parties) to which this party is referred to

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md) (nullable)**  
_Supported Filters_: **EqualsIn**  



## Business Rules

[!list erp.entity=General.Contacts.Parties erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Contacts.Parties erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.Contacts.Parties erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Contacts_Parties?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Contacts_Parties?$top=10>

