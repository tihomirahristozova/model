# Crm.PromotionalPackages

Promotional packages are packages of products, which are sold together at a special pricing and discount conditions. Entity: Crm_Promotional_Packages

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.PromotionalPackages.md#Id) | guid |  
| [Active](Crm.PromotionalPackages.md#Active) | boolean | Package status: true = the offer is available for new documents; false = otherwise. [Required] [Default(true)] [Filter(eq)] 
| [Code](Crm.PromotionalPackages.md#Code) | string | Unique code of the promotional package. [Required] [Filter(eq;like)] [ORD] 
| [Name](Crm.PromotionalPackages.md#Name) | string | The name of this PromotionalPackage. [Required] [Filter(eq;like)] [ORD] 
| [ValidForCustomerFilterXML](Crm.PromotionalPackages.md#ValidForCustomerFilterXML) | dataaccessfilter (nullable) | When not null, the package is valid only for the customers, that match the filter. 
| [ValidForDistributionChannelFilterXML](Crm.PromotionalPackages.md#ValidForDistributionChannelFilterXML) | dataaccessfilter (nullable) | When not null, the package is valid only if the specified distribution channel of the sales order fits in the filter criteria. 
| [ValidForShipToCustomerFilterXML](Crm.PromotionalPackages.md#ValidForShipToCustomerFilterXML) | dataaccessfilter (nullable) | When not null, specifies validity condition for the Ship To Customer of the sales document. 
| [ValidFromDate](Crm.PromotionalPackages.md#ValidFromDate) | date (nullable) | When not null specifies the first date when the package is valid for offering. The date is compared against the document date. [Filter(eq;ge;le)] 
| [ValidToDate](Crm.PromotionalPackages.md#ValidToDate) | date (nullable) | When not null specifies the last date (inclusive) when the package is valid. The date is compared against the document date. [Filter(eq;ge;le)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](Crm.PromotionalPackages.md#EnterpriseCompany) | [General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | When not null, indicates that the package is valid only for the specified enterprise company. [Filter(multi eq)] |
| [EnterpriseCompanyLocation](Crm.PromotionalPackages.md#EnterpriseCompanyLocation) | [General.Contacts.CompanyLocations](General.Contacts.CompanyLocations.md) (nullable) | The Enterprise Company Location to which this PromotionalPackage applies, or null if it is for all enterprise company locations. [Filter(multi eq)] |
| [ValidForCustomer](Crm.PromotionalPackages.md#ValidForCustomer) | [Crm.Customers](Crm.Customers.md) (nullable) | When not null, the package is valid only for the specified customer. [Filter(multi eq)] |
| [ValidForDistributionChannel](Crm.PromotionalPackages.md#ValidForDistributionChannel) | [Crm.Marketing.DistributionChannels](Crm.Marketing.DistributionChannels.md) (nullable) | When not null, the package is valid only for the specified distribution channel of the sales order. [Filter(multi eq)] |
| [ValidForPriceList](Crm.PromotionalPackages.md#ValidForPriceList) | [Crm.PriceLists](Crm.PriceLists.md) (nullable) | When not null, the package is valid only for the specified price list. [Filter(multi eq)] |
| [ValidForShipToCustomer](Crm.PromotionalPackages.md#ValidForShipToCustomer) | [Crm.Customers](Crm.Customers.md) (nullable) | When not null, specifies that the package is valid only when the sales document is for the specified Ship To Customer. [Filter(multi eq)] |
| [ValidForTargetGroup](Crm.PromotionalPackages.md#ValidForTargetGroup) | [Crm.Marketing.TargetGroups](Crm.Marketing.TargetGroups.md) (nullable) | When not null, the package is valid only for the specified customer target group. [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Lines | [Crm.PromotionalPackageLines](Crm.PromotionalPackageLines.md) | List of [PromotionalPackageLine](Crm.PromotionalPackageLines.md) child objects, based on the [Crm.PromotionalPackageLine.PromotionalPackage](Crm.PromotionalPackageLines.md#PromotionalPackage) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Active

> Package status: true = the offer is available for new documents; false = otherwise. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Code

> Unique code of the promotional package. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### Name

> The name of this PromotionalPackage. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### ValidForCustomerFilterXML

> When not null, the package is valid only for the customers, that match the filter.

_Type_: **dataaccessfilter (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ValidForDistributionChannelFilterXML

> When not null, the package is valid only if the specified distribution channel of the sales order fits in the filter criteria.

_Type_: **dataaccessfilter (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ValidForShipToCustomerFilterXML

> When not null, specifies validity condition for the Ship To Customer of the sales document.

_Type_: **dataaccessfilter (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ValidFromDate

> When not null specifies the first date when the package is valid for offering. The date is compared against the document date. [Filter(eq;ge;le)]

_Type_: **date (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### ValidToDate

> When not null specifies the last date (inclusive) when the package is valid. The date is compared against the document date. [Filter(eq;ge;le)]

_Type_: **date (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  


## Reference Details

### EnterpriseCompany

> When not null, indicates that the package is valid only for the specified enterprise company. [Filter(multi eq)]

_Type_: **[General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### EnterpriseCompanyLocation

> The Enterprise Company Location to which this PromotionalPackage applies, or null if it is for all enterprise company locations. [Filter(multi eq)]

_Type_: **[General.Contacts.CompanyLocations](General.Contacts.CompanyLocations.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ValidForCustomer

> When not null, the package is valid only for the specified customer. [Filter(multi eq)]

_Type_: **[Crm.Customers](Crm.Customers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ValidForDistributionChannel

> When not null, the package is valid only for the specified distribution channel of the sales order. [Filter(multi eq)]

_Type_: **[Crm.Marketing.DistributionChannels](Crm.Marketing.DistributionChannels.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ValidForPriceList

> When not null, the package is valid only for the specified price list. [Filter(multi eq)]

_Type_: **[Crm.PriceLists](Crm.PriceLists.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ValidForShipToCustomer

> When not null, specifies that the package is valid only when the sales document is for the specified Ship To Customer. [Filter(multi eq)]

_Type_: **[Crm.Customers](Crm.Customers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ValidForTargetGroup

> When not null, the package is valid only for the specified customer target group. [Filter(multi eq)]

_Type_: **[Crm.Marketing.TargetGroups](Crm.Marketing.TargetGroups.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Crm.PromotionalPackages erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.PromotionalPackages erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Crm.PromotionalPackages erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_PromotionalPackages?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_PromotionalPackages?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Promotional_Packages?$top=10>

