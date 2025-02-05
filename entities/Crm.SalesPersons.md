---
uid: Crm.SalesPersons
---
# Crm.SalesPersons Entity

**Namespace:** [Crm](Crm.md)  

Sales persons (or representatives) are sellers inside the enterprise company who sell the products to customers. Entity: Crm_Sales_Persons

## Default Visualization
Default Display Text Format:  
_{Person.PartyName:T}_  
Default Search Members:  
_Person.PartyName_  
Name Data Member:  
_Person.PartyName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.Contacts.Persons](General.Contacts.Persons.md)  
Aggregate Root:  
[General.Contacts.Persons](General.Contacts.Persons.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CommissionPercent](Crm.SalesPersons.md#commissionpercent) | decimal (7, 6) __nullable__ | The percentage (0..1) of commission percent. null means that there is no commission percent. 
| [CommissionPolicyId](Crm.SalesPersons.md#commissionpolicyid) | guid __nullable__ | Current commission policy for the sales person. null means there is no commission policy. `Filter(multi eq)` 
| [ContractEndDate](Crm.SalesPersons.md#contractenddate) | datetime __nullable__ | The ending date of the contract with the sales person. null when the sales person is still active. `Filter(ge;le)` 
| [ContractStartDate](Crm.SalesPersons.md#contractstartdate) | datetime __nullable__ | The starting date of the contract with the sales person. null when it is unknown. `Filter(ge;le)` 
| [DisplayText](Crm.SalesPersons.md#displaytext) | string | Uses the repository DisplayTextFormat to build the display text from the attributes and references of current object. 
| [Id](Crm.SalesPersons.md#id) | guid |  
| [IsActive](Crm.SalesPersons.md#isactive) | boolean | Specifies whether the sales person is active and should be included in the list when choosing sales person through drop-downs, lists, etc. `Required` `Default(true)` `Filter(eq)` 
| [ObjectVersion](Crm.SalesPersons.md#objectversion) | int32 | The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](Crm.SalesPersons.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | The Enterprise Company to which this SalesPerson applies, or null if it is for all enterprise companies. `Filter(multi eq)` |
| [EnterpriseCompanyLocation](Crm.SalesPersons.md#enterprisecompanylocation) | [CompanyLocations](General.Contacts.CompanyLocations.md) (nullable) | The enterprise company location, to which the sales person is assigned. The sales person is allowed to sell to other locations, but this is the default location. null means that the sales person is not assigned to any enterprise location. `Filter(multi eq)` |
| [Person](Crm.SalesPersons.md#person) | [Persons](General.Contacts.Persons.md) | Base personal record. `Required` `Filter(multi eq)` `Owner` |
| [SalesPersonGroup](Crm.SalesPersons.md#salespersongroup) | [SalesPersonGroups](Crm.Distribution.SalesPersonGroups.md) | The sales person group to which this sales person is assigned. `Required` `Filter(multi eq)` |


## Attribute Details

### CommissionPercent

The percentage (0..1) of commission percent. null means that there is no commission percent.

_Type_: **decimal (7, 6) __nullable__**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### CommissionPolicyId

Current commission policy for the sales person. null means there is no commission policy. `Filter(multi eq)`

_Type_: **guid __nullable__**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  

### ContractEndDate

The ending date of the contract with the sales person. null when the sales person is still active. `Filter(ge;le)`

_Type_: **datetime __nullable__**  
_Category_: **System**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### ContractStartDate

The starting date of the contract with the sales person. null when it is unknown. `Filter(ge;le)`

_Type_: **datetime __nullable__**  
_Category_: **System**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### DisplayText

Uses the repository DisplayTextFormat to build the display text from the attributes and references of current object.

_Type_: **string**  
_Category_: **Calculated Attributes**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

Specifies whether the sales person is active and should be included in the list when choosing sales person through drop-downs, lists, etc. `Required` `Default(true)` `Filter(eq)`

_Type_: **boolean**  
_Category_: **System**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### ObjectVersion

The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking.

_Type_: **int32**  
_Category_: **Extensible Data Object**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  


## Reference Details

### EnterpriseCompany

The Enterprise Company to which this SalesPerson applies, or null if it is for all enterprise companies. `Filter(multi eq)`

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  

### EnterpriseCompanyLocation

The enterprise company location, to which the sales person is assigned. The sales person is allowed to sell to other locations, but this is the default location. null means that the sales person is not assigned to any enterprise location. `Filter(multi eq)`

_Type_: **[CompanyLocations](General.Contacts.CompanyLocations.md) (nullable)**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  

### Person

Base personal record. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Persons](General.Contacts.Persons.md)**  
_Indexed_: **True**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### SalesPersonGroup

The sales person group to which this sales person is assigned. `Required` `Filter(multi eq)`

_Type_: **[SalesPersonGroups](Crm.Distribution.SalesPersonGroups.md)**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  


## API Methods

Methods that can be invoked in public APIs.

### GetAllowedCustomPropertyValues

Gets the allowed values for the specified custom property for this entity object.              If supported the result is ordered by property value. Some property value sources do not support ordering - in that case the result is not ordered.  
_Return Type_: **Collection Of [CustomPropertyValue](../data-types.md#general.custompropertyvalue)**  
_Declaring Type_: **EntityObject**  
_Domain API Request_: **GET**  

**Parameters**  
  * **customPropertyCode**  
    The code of the custom property  
    _Type_: string  

  * **search**  
    The search text - searches by value or description. Can contain wildcard character %.  
    _Type_: string  
     _Optional_: True  
    _Default Value_: null  

  * **exactMatch**  
    If true the search text should be equal to the property value  
    _Type_: boolean  
     _Optional_: True  
    _Default Value_: False  

  * **orderByDescription**  
    If true the result is ordered by Description instead of Value. Note that ordering is not always possible.  
    _Type_: boolean  
     _Optional_: True  
    _Default Value_: False  

  * **top**  
    The top clause - default is 10  
    _Type_: int32  
     _Optional_: True  
    _Default Value_: 10  

  * **skip**  
    The skip clause - default is 0  
    _Type_: int32  
     _Optional_: True  
    _Default Value_: 0  


### CreateNotification

Creates a notification a sends a real time event to the user.  
_Return Type_: **void**  
_Declaring Type_: **EntityObject**  
_Domain API Request_: **POST**  

**Parameters**  
  * **user**  
    The user.  
    _Type_: [Users](Systems.Security.Users.md)  

  * **notificationClass**  
    The notification class.  
    _Type_: string  

  * **subject**  
    The subject.  
    _Type_: string  


### CreateCopy

Duplicates the object and its child objects belonging to the same aggregate.              The duplicated objects are not saved to the data source but remain in the same transaction as the original object.  
_Return Type_: **EntityObject**  
_Declaring Type_: **EntityObject**  
_Domain API Request_: **POST**  


## Business Rules

[!list limit=1000 erp.entity=Crm.SalesPersons erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Crm.SalesPersons erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_SalesPersons?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_SalesPersons?$top=10>

