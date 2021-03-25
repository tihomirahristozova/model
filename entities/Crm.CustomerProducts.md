---
uid: Crm.CustomerProducts
---
# Crm.CustomerProducts Entity

**Namespace:** [Crm](Crm.md)  

Contains the products, that are contracted (listed) with a customer. Entity: Crm_Customer_Products

## Default Visualization
Default Display Text Format:  
_{Customer.Number}_  
Default Search Member:  
_Customer.Number_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Crm.Customers](Crm.Customers.md)  
Aggregate Root:  
[General.Contacts.Parties](General.Contacts.Parties.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [FromDate](Crm.CustomerProducts.md#fromdate) | date (nullable) | The initial date of the listing. null when the initial date is unknown. `Filter(eq;ge;le)` 
| [Id](Crm.CustomerProducts.md#id) | guid |  
| [Notes](Crm.CustomerProducts.md#notes) | string(254) (nullable) | Notes for the listing. 
| [ToDate](Crm.CustomerProducts.md#todate) | date (nullable) | The final date of the listing. null when the final date is unknown. `Filter(eq;ge;le)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CompanyDivision](Crm.CustomerProducts.md#companydivision) | [CompanyDivisions](General.Contacts.CompanyDivisions.md) (nullable) | When the customer is a company, denotes the division for which the product is listed. null when the customer is not a company or when the listing is not division specific. `Filter(multi eq)` |
| [CompanyLocation](Crm.CustomerProducts.md#companylocation) | [CompanyLocations](General.Contacts.CompanyLocations.md) (nullable) | When the customer is a company, denotes the location for which the product is listed. null when the customer is not a company or when the listing is not location specific. `Filter(multi eq)` |
| [Customer](Crm.CustomerProducts.md#customer) | [Customers](Crm.Customers.md) | Customer, for which the product is listed. `Required` `Filter(multi eq)` `Owner` |
| [Product](Crm.CustomerProducts.md#product) | [Products](General.Products.Products.md) | The product, which is listed for the customer. `Required` `Filter(multi eq)` |


## Attribute Details

### FromDate

The initial date of the listing. null when the initial date is unknown. `Filter(eq;ge;le)`

_Type_: **date (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

Notes for the listing.

_Type_: **string(254) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### ToDate

The final date of the listing. null when the final date is unknown. `Filter(eq;ge;le)`

_Type_: **date (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  


## Reference Details

### CompanyDivision

When the customer is a company, denotes the division for which the product is listed. null when the customer is not a company or when the listing is not division specific. `Filter(multi eq)`

_Type_: **[CompanyDivisions](General.Contacts.CompanyDivisions.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### CompanyLocation

When the customer is a company, denotes the location for which the product is listed. null when the customer is not a company or when the listing is not location specific. `Filter(multi eq)`

_Type_: **[CompanyLocations](General.Contacts.CompanyLocations.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Customer

Customer, for which the product is listed. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Customers](Crm.Customers.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### Product

The product, which is listed for the customer. `Required` `Filter(multi eq)`

_Type_: **[Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Crm.CustomerProducts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.CustomerProducts erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_CustomerProducts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_CustomerProducts?$top=10>

