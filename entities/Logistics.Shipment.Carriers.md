---
uid: Logistics.Shipment.Carriers
---
# Logistics.Shipment.Carriers Entity

**Namespace:** [Logistics.Shipment](Logistics.Shipment.md)  

Represents a carrier agreement. One actual carrier can have different agreements over time or with different enterprise companies. Entity: Log_Carriers

## Default Visualization
Default Display Text Format:  
_{Code}_  
Default Search Member:  
_Code_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Logistics.Shipment.Carriers](Logistics.Shipment.Carriers.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [AgreementEndDate](Logistics.Shipment.Carriers.md#agreementenddate) | date (nullable) | The ending date of the agreement with this carrier. null for agreements which are still active. [Filter(eq;ge;le)] 
| [AgreementStartDate](Logistics.Shipment.Carriers.md#agreementstartdate) | date | The start date of the agreement with this carrier. [Required] [Default(Today)] [Filter(eq;ge;le)] 
| [Code](Logistics.Shipment.Carriers.md#code) | string | Unique carrier code (or call sign). The code is unique within all enterprise companies. [Required] [Filter(eq;like)] [ORD] 
| [Id](Logistics.Shipment.Carriers.md#id) | guid |  
| [IsActive](Logistics.Shipment.Carriers.md#isactive) | boolean | Specifies whether the carrier agreement is active. [Required] [Default(true)] [Filter(eq)] 
| [Notes](Logistics.Shipment.Carriers.md#notes) | string (nullable) | Notes for this Carrier. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](Logistics.Shipment.Carriers.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company which signed the carrier agreement. [Required] [Filter(multi eq)] |
| [Supplier](Logistics.Shipment.Carriers.md#supplier) | [Suppliers](Logistics.Procurement.Suppliers.md) | The supplier contract with the carrier. [Required] [Filter(multi eq)] |


## Attribute Details

### AgreementEndDate

The ending date of the agreement with this carrier. null for agreements which are still active. [Filter(eq;ge;le)]

_Type_: **date (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### AgreementStartDate

The start date of the agreement with this carrier. [Required] [Default(Today)] [Filter(eq;ge;le)]

_Type_: **date**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDate**  

### Code

Unique carrier code (or call sign). The code is unique within all enterprise companies. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

Specifies whether the carrier agreement is active. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Notes

Notes for this Carrier.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### EnterpriseCompany

The enterprise company which signed the carrier agreement. [Required] [Filter(multi eq)]

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Supplier

The supplier contract with the carrier. [Required] [Filter(multi eq)]

_Type_: **[Suppliers](Logistics.Procurement.Suppliers.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Logistics.Shipment.Carriers erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Shipment.Carriers erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Shipment_Carriers?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Shipment_Carriers?$top=10>

