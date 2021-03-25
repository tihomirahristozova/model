---
uid: Crm.PromotionalPackages
---
# Crm.PromotionalPackages Entity

**Namespace:** [Crm](Crm.md)  

Promotional packages are packages of products, which are sold together at a special pricing and discount conditions. Entity: Crm_Promotional_Packages

## Default Visualization
Default Display Text Format:  
_{Code}: {Name:T}_  
Default Search Member:  
_Code_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Crm.PromotionalPackages](Crm.PromotionalPackages.md)  
  * [Crm.PromotionalPackageLines](Crm.PromotionalPackageLines.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Active](Crm.PromotionalPackages.md#active) | boolean | Package status: true = the offer is available for new documents; false = otherwise. `Required` `Default(true)` `Filter(eq)` 
| [Code](Crm.PromotionalPackages.md#code) | string(20) | Unique code of the promotional package. `Required` `Filter(eq;like)` `ORD` 
| [Id](Crm.PromotionalPackages.md#id) | guid |  
| [Name](Crm.PromotionalPackages.md#name) | string(254) | The name of this PromotionalPackage. `Required` `Filter(eq;like)` `ORD` 
| [ValidForCustomerFilterXML](Crm.PromotionalPackages.md#validforcustomerfilterxml) | dataaccessfilter (nullable) | When not null, the package is valid only for the customers, that match the filter. 
| [ValidForDistribution<br />ChannelFilterX<br />ML](Crm.PromotionalPackages.md#validfordistributionchannelfilterxml) | dataaccessfilter (nullable) | When not null, the package is valid only if the specified distribution channel of the sales order fits in the filter criteria. 
| [ValidForShipTo<br />CustomerFilter<br />XML](Crm.PromotionalPackages.md#validforshiptocustomerfilterxml) | dataaccessfilter (nullable) | When not null, specifies validity condition for the Ship To Customer of the sales document. 
| [ValidFromDate](Crm.PromotionalPackages.md#validfromdate) | date (nullable) | When not null specifies the first date when the package is valid for offering. The date is compared against the document date. `Filter(eq;ge;le)` 
| [ValidToDate](Crm.PromotionalPackages.md#validtodate) | date (nullable) | When not null specifies the last date (inclusive) when the package is valid. The date is compared against the document date. `Filter(eq;ge;le)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](Crm.PromotionalPackages.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | When not null, indicates that the package is valid only for the specified enterprise company. `Filter(multi eq)` |
| [EnterpriseCompanyLocation](Crm.PromotionalPackages.md#enterprisecompanylocation) | [CompanyLocations](General.Contacts.CompanyLocations.md) (nullable) | The Enterprise Company Location to which this PromotionalPackage applies, or null if it is for all enterprise company locations. `Filter(multi eq)` |
| [ValidForCustomer](Crm.PromotionalPackages.md#validforcustomer) | [Customers](Crm.Customers.md) (nullable) | When not null, the package is valid only for the specified customer. `Filter(multi eq)` |
| [ValidForDistribution<br />Channel](Crm.PromotionalPackages.md#validfordistributionchannel) | [DistributionChannels](Crm.Marketing.DistributionChannels.md) (nullable) | When not null, the package is valid only for the specified distribution channel of the sales order. `Filter(multi eq)` |
| [ValidForPriceList](Crm.PromotionalPackages.md#validforpricelist) | [PriceLists](Crm.PriceLists.md) (nullable) | When not null, the package is valid only for the specified price list. `Filter(multi eq)` |
| [ValidForShipToCustomer](Crm.PromotionalPackages.md#validforshiptocustomer) | [Customers](Crm.Customers.md) (nullable) | When not null, specifies that the package is valid only when the sales document is for the specified Ship To Customer. `Filter(multi eq)` |
| [ValidForTargetGroup](Crm.PromotionalPackages.md#validfortargetgroup) | [TargetGroups](Crm.Marketing.TargetGroups.md) (nullable) | When not null, the package is valid only for the specified customer target group. `Filter(multi eq)` |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Lines | [PromotionalPackageLines](Crm.PromotionalPackageLines.md) | List of `PromotionalPackageLine`(Crm.PromotionalPackageLines.md) child objects, based on the `Crm.PromotionalPackageLine.PromotionalPackage`(Crm.PromotionalPackageLines.md#promotionalpackage) back reference 


## Attribute Details

### Active

Package status: true = the offer is available for new documents; false = otherwise. `Required` `Default(true)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Code

Unique code of the promotional package. `Required` `Filter(eq;like)` `ORD`

_Type_: **string(20)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  
_Maximum Length_: **20**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The name of this PromotionalPackage. `Required` `Filter(eq;like)` `ORD`

_Type_: **string(254)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  
_Maximum Length_: **254**  

### ValidForCustomerFilterXML

When not null, the package is valid only for the customers, that match the filter.

_Type_: **dataaccessfilter (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ValidForDistributionChannelFilterXML

When not null, the package is valid only if the specified distribution channel of the sales order fits in the filter criteria.

_Type_: **dataaccessfilter (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ValidForShipToCustomerFilterXML

When not null, specifies validity condition for the Ship To Customer of the sales document.

_Type_: **dataaccessfilter (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ValidFromDate

When not null specifies the first date when the package is valid for offering. The date is compared against the document date. `Filter(eq;ge;le)`

_Type_: **date (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### ValidToDate

When not null specifies the last date (inclusive) when the package is valid. The date is compared against the document date. `Filter(eq;ge;le)`

_Type_: **date (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  


## Reference Details

### EnterpriseCompany

When not null, indicates that the package is valid only for the specified enterprise company. `Filter(multi eq)`

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### EnterpriseCompanyLocation

The Enterprise Company Location to which this PromotionalPackage applies, or null if it is for all enterprise company locations. `Filter(multi eq)`

_Type_: **[CompanyLocations](General.Contacts.CompanyLocations.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ValidForCustomer

When not null, the package is valid only for the specified customer. `Filter(multi eq)`

_Type_: **[Customers](Crm.Customers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ValidForDistributionChannel

When not null, the package is valid only for the specified distribution channel of the sales order. `Filter(multi eq)`

_Type_: **[DistributionChannels](Crm.Marketing.DistributionChannels.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ValidForPriceList

When not null, the package is valid only for the specified price list. `Filter(multi eq)`

_Type_: **[PriceLists](Crm.PriceLists.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ValidForShipToCustomer

When not null, specifies that the package is valid only when the sales document is for the specified Ship To Customer. `Filter(multi eq)`

_Type_: **[Customers](Crm.Customers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ValidForTargetGroup

When not null, the package is valid only for the specified customer target group. `Filter(multi eq)`

_Type_: **[TargetGroups](Crm.Marketing.TargetGroups.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Crm.PromotionalPackages erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.PromotionalPackages erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_PromotionalPackages?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_PromotionalPackages?$top=10>

