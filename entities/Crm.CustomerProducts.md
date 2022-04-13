---
uid: Crm.CustomerProducts
---
# Crm.CustomerProducts Entity

**Namespace:** [Crm](Crm.md)  

Contains the products, that are contracted (listed) with a customer. Entity: Crm_Customer_Products

## Default Visualization
Default Display Text Format:  
_{Customer}_  
Default Search Members:  
_Customer_  
Name Data Member:  
_Customer_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Crm.Customers](Crm.Customers.md)  
Aggregate Root:  
[Crm.Customers](Crm.Customers.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [DisplayText](Crm.CustomerProducts.md#displaytext) | string | Uses the repository DisplayTextFormat to build the display text from the attributes and references of current object. 
| [FromDate](Crm.CustomerProducts.md#fromdate) | date __nullable__ | The initial date of the listing. null when the initial date is unknown. `Filter(eq;ge;le)` 
| [Id](Crm.CustomerProducts.md#id) | guid |  
| [IsActive](Crm.CustomerProducts.md#isactive) | boolean |  
| [Notes](Crm.CustomerProducts.md#notes) | string (254) __nullable__ | Notes for the listing. 
| [ObjectVersion](Crm.CustomerProducts.md#objectversion) | int32 | The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking. 
| [ToDate](Crm.CustomerProducts.md#todate) | date __nullable__ | The final date of the listing. null when the final date is unknown. `Filter(eq;ge;le)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CompanyDivision](Crm.CustomerProducts.md#companydivision) | [CompanyDivisions](General.Contacts.CompanyDivisions.md) (nullable) | When the customer is a company, denotes the division for which the product is listed. null when the customer is not a company or when the listing is not division specific. `Filter(multi eq)` |
| [CompanyLocation](Crm.CustomerProducts.md#companylocation) | [CompanyLocations](General.Contacts.CompanyLocations.md) (nullable) | When the customer is a company, denotes the location for which the product is listed. null when the customer is not a company or when the listing is not location specific. `Filter(multi eq)` |
| [Customer](Crm.CustomerProducts.md#customer) | [Customers](Crm.Customers.md) | Customer, for which the product is listed. `Required` `Filter(multi eq)` `Owner` |
| [Product](Crm.CustomerProducts.md#product) | [Products](General.Products.Products.md) | The product, which is listed for the customer. `Required` `Filter(multi eq)` |


## Attribute Details

### DisplayText

Uses the repository DisplayTextFormat to build the display text from the attributes and references of current object.

_Type_: **string**  
_Category_: **Calculated Attributes**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### FromDate

The initial date of the listing. null when the initial date is unknown. `Filter(eq;ge;le)`

_Type_: **date __nullable__**  
_Category_: **System**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

_Type_: **boolean**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Notes

Notes for the listing.

_Type_: **string (254) __nullable__**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### ObjectVersion

The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking.

_Type_: **int32**  
_Category_: **Extensible Data Object**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### ToDate

The final date of the listing. null when the final date is unknown. `Filter(eq;ge;le)`

_Type_: **date __nullable__**  
_Category_: **System**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  


## Reference Details

### CompanyDivision

When the customer is a company, denotes the division for which the product is listed. null when the customer is not a company or when the listing is not division specific. `Filter(multi eq)`

_Type_: **[CompanyDivisions](General.Contacts.CompanyDivisions.md) (nullable)**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  

### CompanyLocation

When the customer is a company, denotes the location for which the product is listed. null when the customer is not a company or when the listing is not location specific. `Filter(multi eq)`

_Type_: **[CompanyLocations](General.Contacts.CompanyLocations.md) (nullable)**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  

### Customer

Customer, for which the product is listed. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Customers](Crm.Customers.md)**  
_Indexed_: **True**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### Product

The product, which is listed for the customer. `Required` `Filter(multi eq)`

_Type_: **[Products](General.Products.Products.md)**  
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



## Business Rules

[!list limit=1000 erp.entity=Crm.CustomerProducts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Crm.CustomerProducts erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_CustomerProducts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_CustomerProducts?$top=10>

