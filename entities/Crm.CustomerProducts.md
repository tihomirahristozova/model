---
uid: Crm.CustomerProducts
---
# Crm.CustomerProducts

Contains the products, that are contracted (listed) with a customer. Entity: Crm_Customer_Products

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.CustomerProducts.md#Id) | guid |  
| [FromDate](Crm.CustomerProducts.md#FromDate) | date (nullable) | The initial date of the listing. null when the initial date is unknown. [Filter(eq;ge;le)] 
| [Notes](Crm.CustomerProducts.md#Notes) | string (nullable) | Notes for the listing. 
| [ToDate](Crm.CustomerProducts.md#ToDate) | date (nullable) | The final date of the listing. null when the final date is unknown. [Filter(eq;ge;le)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CompanyDivision](Crm.CustomerProducts.md#CompanyDivision) | [General.Contacts.CompanyDivisions](General.Contacts.CompanyDivisions.md) (nullable) | When the customer is a company, denotes the division for which the product is listed. null when the customer is not a company or when the listing is not division specific. [Filter(multi eq)] |
| [CompanyLocation](Crm.CustomerProducts.md#CompanyLocation) | [General.Contacts.CompanyLocations](General.Contacts.CompanyLocations.md) (nullable) | When the customer is a company, denotes the location for which the product is listed. null when the customer is not a company or when the listing is not location specific. [Filter(multi eq)] |
| [Customer](Crm.CustomerProducts.md#Customer) | [Crm.Customers](Crm.Customers.md) | Customer, for which the product is listed. [Required] [Filter(multi eq)] [Owner] |
| [Product](Crm.CustomerProducts.md#Product) | [General.Products.Products](General.Products.Products.md) | The product, which is listed for the customer. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### FromDate

> The initial date of the listing. null when the initial date is unknown. [Filter(eq;ge;le)]

_Type_: **date (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### Notes

> Notes for the listing.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ToDate

> The final date of the listing. null when the final date is unknown. [Filter(eq;ge;le)]

_Type_: **date (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  


## Reference Details

### CompanyDivision

> When the customer is a company, denotes the division for which the product is listed. null when the customer is not a company or when the listing is not division specific. [Filter(multi eq)]

_Type_: **[General.Contacts.CompanyDivisions](General.Contacts.CompanyDivisions.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### CompanyLocation

> When the customer is a company, denotes the location for which the product is listed. null when the customer is not a company or when the listing is not location specific. [Filter(multi eq)]

_Type_: **[General.Contacts.CompanyLocations](General.Contacts.CompanyLocations.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Customer

> Customer, for which the product is listed. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Crm.Customers](Crm.Customers.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Product

> The product, which is listed for the customer. [Required] [Filter(multi eq)]

_Type_: **[General.Products.Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Crm.CustomerProducts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.CustomerProducts erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Crm.CustomerProducts erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_CustomerProducts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_CustomerProducts?$top=10>

