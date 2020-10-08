---
uid: Logistics.Inventory.Stores
---
# Logistics.Inventory.Stores

Represents the physical warehouses. Entity: Inv_Stores

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Inventory.Stores.md#Id) | guid |  
| [IsActive](Logistics.Inventory.Stores.md#IsActive) | boolean | Specifies whether the current party is active in the system or not [Required] 
| [PartyCreationTime](Logistics.Inventory.Stores.md#PartyCreationTime) | datetime (nullable) | Date and time when the Party was created. 
| [PartyCreationUser](Logistics.Inventory.Stores.md#PartyCreationUser) | string (nullable) | Login name of the user, who created the Party. 
| [DefaultProductCodingSystemId](Logistics.Inventory.Stores.md#DefaultProductCodingSystemId) | guid (nullable) |  
| [GLN](Logistics.Inventory.Stores.md#GLN) | string (nullable) | Global Location Number used by EDI systems 
| [PartyNotes](Logistics.Inventory.Stores.md#PartyNotes) | string (nullable) | Notes for this Party 
| [ParentPartyId](Logistics.Inventory.Stores.md#ParentPartyId) | guid (nullable) |  
| [PartyCode](Logistics.Inventory.Stores.md#PartyCode) | string | The unique code of the Party [Required] 
| [PartyName](Logistics.Inventory.Stores.md#PartyName) | [MultilanguageString](../data-types.md#MultilanguageString) | The name of the party [Required] 
| [PartyType](Logistics.Inventory.Stores.md#PartyType) | [General.Contacts.PartiesRepository.PartyType](Logistics.Inventory.Stores.md#PartyType) | Type of party. Currently supported are P=Person, C=Company, S=Store, L=Company Location, V=Division [Required] 
| [PartyUniqueNumber](Logistics.Inventory.Stores.md#PartyUniqueNumber) | string (nullable) | Unique number of the party (National number for persons, Registration number for companies) 
| [PartyUpdateTime](Logistics.Inventory.Stores.md#PartyUpdateTime) | datetime (nullable) | Date and time when the Party was last updated. 
| [PartyUpdateUser](Logistics.Inventory.Stores.md#PartyUpdateUser) | string (nullable) | Login name of the user, who last updated the Party. 
| [CreationTime](Logistics.Inventory.Stores.md#CreationTime) | datetime (nullable) | Date and time when the Store was created. [Filter(ge;le)] [ReadOnly] 
| [CreationUser](Logistics.Inventory.Stores.md#CreationUser) | string (nullable) | Login name of the user, who created the Store. [Filter(like)] [ReadOnly] 
| [DefaultSupplyStoreId](Logistics.Inventory.Stores.md#DefaultSupplyStoreId) | guid (nullable) | The store from which goods are usually supplied to this store. [Filter(multi eq)] 
| [NumberOfDimensions](Logistics.Inventory.Stores.md#NumberOfDimensions) | int32 | Number of dimensions in the coordinate system of the storage bins. 0 means single-bin store. Currently, this is only stored for information and is not used for automatical generation of store bins, as it was intended. [Required] [Default(0)] [Filter(eq)] 
| [SchemaXML](Logistics.Inventory.Stores.md#SchemaXML) | string (nullable) | Obsolete. Not used. 
| [Code](Logistics.Inventory.Stores.md#Code) | string | The unique code of the Store. [Required] [Filter(eq;like)] [ORD] 
| [Name](Logistics.Inventory.Stores.md#Name) | [MultilanguageString](../data-types.md#MultilanguageString) | Name of the store. [Required] [Filter(like)] 
| [Unmanaged](Logistics.Inventory.Stores.md#Unmanaged) | boolean | If false the system will expect the user to process the store transactions. If true the system will auto-generate them. [Required] [Default(true)] 
| [UpdateTime](Logistics.Inventory.Stores.md#UpdateTime) | datetime (nullable) | Date and time when the Store was last updated. [Filter(ge;le)] [ReadOnly] 
| [UpdateUser](Logistics.Inventory.Stores.md#UpdateUser) | string (nullable) | Login name of the user, who last updated the Store. [Filter(like)] [ReadOnly] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AdministrativeRegion](Logistics.Inventory.Stores.md#AdministrativeRegion) | [General.Geography.AdministrativeRegions](General.Geography.AdministrativeRegions.md) (nullable) | The administrative region in which the party is situated. |
| [Area](Logistics.Inventory.Stores.md#Area) | [General.Geography.Areas](General.Geography.Areas.md) (nullable) | The area in which the party is situated. |
| [DefaultProductCodingSystem](Logistics.Inventory.Stores.md#DefaultProductCodingSystem) | [General.Products.CodingSystems](General.Products.CodingSystems.md) (nullable) | When not null, specifies coding system for products, which is required by the party. The coding system is used primarily for document printouts and document import/exports. |
| [ParentParty](Logistics.Inventory.Stores.md#ParentParty) | [General.Contacts.Parties](General.Contacts.Parties.md) (nullable) | Organizational unit (branch from the hierarchy of all parties) to which this party is referred to |
| [AccessKey](Logistics.Inventory.Stores.md#AccessKey) | [Systems.Security.AccessKeys](Systems.Security.AccessKeys.md) (nullable) | The access key, containing the user permissions for this Store. Null means that all users have unlimited permissions. [Filter(multi eq)] |
| [Currency](Logistics.Inventory.Stores.md#Currency) | [General.Currencies](General.Currencies.md) (nullable) | The currency for the warehouse cost calculations. When null, the base currency for the enterprise company will be used. [Filter(multi eq)] |
| [DefaultStoreBin](Logistics.Inventory.Stores.md#DefaultStoreBin) | [Logistics.Inventory.StoreBins](Logistics.Inventory.StoreBins.md) (nullable) | To be used when store bin is unknown. [Filter(multi eq)] |
| [EnterpriseCompany](Logistics.Inventory.Stores.md#EnterpriseCompany) | [General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | The Enterprise Company to which this Store applies, or null if it is for all enterprise companies. [Filter(multi eq)] |
| [EnterpriseCompanyLocation](Logistics.Inventory.Stores.md#EnterpriseCompanyLocation) | [General.Contacts.CompanyLocations](General.Contacts.CompanyLocations.md) (nullable) | The Enterprise Company Location to which this Store applies, or null if it is for all enterprise company locations. [Filter(multi eq)] |
| [Parent](Logistics.Inventory.Stores.md#Parent) | [Logistics.Inventory.Stores](Logistics.Inventory.Stores.md) (nullable) | Obsolete. Not used. (Hierarchy of the stores is now represented by the Store Groups entity). [Filter(multi eq)] |
| [ResponsibleParty](Logistics.Inventory.Stores.md#ResponsibleParty) | [General.Contacts.Parties](General.Contacts.Parties.md) (nullable) | Primary responsible party (usually employee) for the stock in the store. [Filter(multi eq)] |
| [StoreGroup](Logistics.Inventory.Stores.md#StoreGroup) | [Logistics.Inventory.StoreGroups](Logistics.Inventory.StoreGroups.md) | The store group, to which this store belongs. [Required] [Filter(multi eq)] |
| [Warehouse](Logistics.Inventory.Stores.md#Warehouse) | [Logistics.Wms.Warehouses](Logistics.Wms.Warehouses.md) (nullable) | Specifies, the warehouse, which manages the warehouse operations for the store. null for stores, which do not have managed operations. [Filter(multi eq)] (Introduced in version 20.1.100.0) |

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
| Bins | [Logistics.Inventory.StoreBins](Logistics.Inventory.StoreBins.md) | List of [StoreBin](Logistics.Inventory.StoreBins.md) child objects, based on the [Logistics.Inventory.StoreBin.Store](Logistics.Inventory.StoreBins.md#Store) back reference 
| ResponsibleParties | [Logistics.Inventory.StoreResponsibleParties](Logistics.Inventory.StoreResponsibleParties.md) | List of [StoreResponsibleParty](Logistics.Inventory.StoreResponsibleParties.md) child objects, based on the [Logistics.Inventory.StoreResponsibleParty.Store](Logistics.Inventory.StoreResponsibleParties.md#Store) back reference 


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

_Type_: **[MultilanguageString](../data-types.md#MultilanguageString)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### PartyType

> Type of party. Currently supported are P=Person, C=Company, S=Store, L=Company Location, V=Division [Required]

_Type_: **[General.Contacts.PartiesRepository.PartyType](Logistics.Inventory.Stores.md#PartyType)**  
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

### CreationTime

> Date and time when the Store was created. [Filter(ge;le)] [ReadOnly]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### CreationUser

> Login name of the user, who created the Store. [Filter(like)] [ReadOnly]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### DefaultSupplyStoreId

> The store from which goods are usually supplied to this store. [Filter(multi eq)]

_Type_: **guid (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### NumberOfDimensions

> Number of dimensions in the coordinate system of the storage bins. 0 means single-bin store. Currently, this is only stored for information and is not used for automatical generation of store bins, as it was intended. [Required] [Default(0)] [Filter(eq)]

_Type_: **int32**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### SchemaXML

> Obsolete. Not used.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Code

> The unique code of the Store. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### Name

> Name of the store. [Required] [Filter(like)]

_Type_: **[MultilanguageString](../data-types.md#MultilanguageString)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Unmanaged

> If false the system will expect the user to process the store transactions. If true the system will auto-generate them. [Required] [Default(true)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### UpdateTime

> Date and time when the Store was last updated. [Filter(ge;le)] [ReadOnly]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### UpdateUser

> Login name of the user, who last updated the Store. [Filter(like)] [ReadOnly]

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

### AccessKey

> The access key, containing the user permissions for this Store. Null means that all users have unlimited permissions. [Filter(multi eq)]

_Type_: **[Systems.Security.AccessKeys](Systems.Security.AccessKeys.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Currency

> The currency for the warehouse cost calculations. When null, the base currency for the enterprise company will be used. [Filter(multi eq)]

_Type_: **[General.Currencies](General.Currencies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF((obj.EnterpriseCompany != null), obj.EnterpriseCompany.BaseCurrency, obj.Transaction.CurrentEnterpriseCompany.BaseCurrency)`
### DefaultStoreBin

> To be used when store bin is unknown. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.StoreBins](Logistics.Inventory.StoreBins.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### EnterpriseCompany

> The Enterprise Company to which this Store applies, or null if it is for all enterprise companies. [Filter(multi eq)]

_Type_: **[General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### EnterpriseCompanyLocation

> The Enterprise Company Location to which this Store applies, or null if it is for all enterprise company locations. [Filter(multi eq)]

_Type_: **[General.Contacts.CompanyLocations](General.Contacts.CompanyLocations.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Parent

> Obsolete. Not used. (Hierarchy of the stores is now represented by the Store Groups entity). [Filter(multi eq)]

_Type_: **[Logistics.Inventory.Stores](Logistics.Inventory.Stores.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ResponsibleParty

> Primary responsible party (usually employee) for the stock in the store. [Filter(multi eq)]

_Type_: **[General.Contacts.Parties](General.Contacts.Parties.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### StoreGroup

> The store group, to which this store belongs. [Required] [Filter(multi eq)]

_Type_: **[Logistics.Inventory.StoreGroups](Logistics.Inventory.StoreGroups.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Warehouse

> Specifies, the warehouse, which manages the warehouse operations for the store. null for stores, which do not have managed operations. [Filter(multi eq)] (Introduced in version 20.1.100.0)

_Type_: **[Logistics.Wms.Warehouses](Logistics.Wms.Warehouses.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Logistics.Inventory.Stores erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Inventory.Stores erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Inventory.Stores erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Inventory_Stores?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Inventory_Stores?$top=10>

