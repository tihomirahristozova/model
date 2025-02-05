---
uid: Crm.CustomerProducts
---
# Crm.CustomerProducts Entity

**Namespace:** [Crm](Crm.md)  

Contains the products, that are contracted (listed) with a customer. Entity: Crm_Customer_Products (Introduced in version 22.1.6.42)

## Default Visualization
Default Display Text Format:  
_{Customer.Party.PartyName:T}_  
Default Search Members:  
_Customer.Party.PartyName_  
Name Data Member:  
_Customer.Party.PartyName_  

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
| [InStoreLocation](Crm.CustomerProducts.md#instorelocation) | string (32) __nullable__ | Location in store, like row, stand, etc. 
| [InStoreMaxQuantity](Crm.CustomerProducts.md#instoremaxquantity) | [Quantity (10, 3)](../data-types.md#quantity) __nullable__ | Maximum quantity maintained by the customer. Measurement unit is Product.MeasurementUnit. `Unit: InStoreQuantityUnit` `Filter(eq;ge;le)` 
| [InStoreMinQuantity](Crm.CustomerProducts.md#instoreminquantity) | [Quantity (10, 3)](../data-types.md#quantity) __nullable__ | Minimum quantity maintained by the customer. Measurement unit is Product.MeasurementUnit. `Unit: InStoreQuantityUnit` `Filter(eq;ge;le)` 
| [IsActive](Crm.CustomerProducts.md#isactive) | boolean | Indicates whether this customer product definition is active. `Required` `Default(true)` `Filter(eq)` 
| [Notes](Crm.CustomerProducts.md#notes) | string (254) __nullable__ | Notes for the listing. 
| [ObjectVersion](Crm.CustomerProducts.md#objectversion) | int32 | The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking. 
| [OrderMultiple](Crm.CustomerProducts.md#ordermultiple) | [Quantity (10, 3)](../data-types.md#quantity) __nullable__ | Determines the step when the system offers a quantity to order. `Unit: InStoreQuantityUnit` `Filter(eq;ge;le)` 
| [ToDate](Crm.CustomerProducts.md#todate) | date __nullable__ | The final date of the listing. null when the final date is unknown. `Filter(eq;ge;le)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CompanyDivision](Crm.CustomerProducts.md#companydivision) | [CompanyDivisions](General.Contacts.CompanyDivisions.md) (nullable) | When the customer is a company, denotes the division for which the product is listed. null when the customer is not a company or when the listing is not division specific. `Filter(multi eq)` |
| [CompanyLocation](Crm.CustomerProducts.md#companylocation) | [CompanyLocations](General.Contacts.CompanyLocations.md) (nullable) | When the customer is a company, denotes the location for which the product is listed. null when the customer is not a company or when the listing is not location specific. `Filter(multi eq)` |
| [Customer](Crm.CustomerProducts.md#customer) | [Customers](Crm.Customers.md) | Customer, for which the product is listed. `Required` `Filter(multi eq)` `Owner` |
| [InStoreQuantityUnit](Crm.CustomerProducts.md#instorequantityunit) | [MeasurementUnits](General.MeasurementUnits.md) (nullable) |  |
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

### InStoreLocation

Location in store, like row, stand, etc.

_Type_: **string (32) __nullable__**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **32**  

### InStoreMaxQuantity

Maximum quantity maintained by the customer. Measurement unit is Product.MeasurementUnit. `Unit: InStoreQuantityUnit` `Filter(eq;ge;le)`

_Type_: **[Quantity (10, 3)](../data-types.md#quantity) __nullable__**  
_Category_: **System**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### InStoreMinQuantity

Minimum quantity maintained by the customer. Measurement unit is Product.MeasurementUnit. `Unit: InStoreQuantityUnit` `Filter(eq;ge;le)`

_Type_: **[Quantity (10, 3)](../data-types.md#quantity) __nullable__**  
_Category_: **System**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### IsActive

Indicates whether this customer product definition is active. `Required` `Default(true)` `Filter(eq)`

_Type_: **boolean**  
_Category_: **System**  
_Supported Filters_: **Equals**  
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

### OrderMultiple

Determines the step when the system offers a quantity to order. `Unit: InStoreQuantityUnit` `Filter(eq;ge;le)`

_Type_: **[Quantity (10, 3)](../data-types.md#quantity) __nullable__**  
_Category_: **System**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

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

### InStoreQuantityUnit

_Type_: **[MeasurementUnits](General.MeasurementUnits.md) (nullable)**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`obj.Product.MeasurementUnit`
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

[!list limit=1000 erp.entity=Crm.CustomerProducts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Crm.CustomerProducts erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_CustomerProducts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_CustomerProducts?$top=10>

