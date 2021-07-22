---
uid: Finance.Excise.ExciseAdministrativeDocuments
---
# Finance.Excise.ExciseAdministrativeDocuments Entity

**Namespace:** [Finance.Excise](Finance.Excise.md)  

Represents the data, sent to the customs authorities for the movements of excise goods. Entity: Exc_Excise_Administrative_Documents

## Default Visualization
Default Display Text Format:  
_{AdministrativeReferenceCode}_  
Default Search Member:  
_AdministrativeReferenceCode_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.Documents](General.Documents.md)  
Aggregate Root:  
[General.Documents](General.Documents.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Administrative<br />ReferenceCode](Finance.Excise.ExciseAdministrativeDocuments.md#administrativereferencecode) | string (16) __nullable__ | The reference code, returned the customs authorities, when the document is exported to them. null means the document is not yet exported to the authorities. 
| [Id](Finance.Excise.ExciseAdministrativeDocuments.md#id) | guid |  
| [IsDeferredSubmission](Finance.Excise.ExciseAdministrativeDocuments.md#isdeferredsubmission) | boolean | Indicates whether the movement has begun under the cover of a paper administrative document. `Required` `Default(false)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Document](Finance.Excise.ExciseAdministrativeDocuments.md#document) | [Documents](General.Documents.md) | The Document to which this ExciseAdministrative<br />Document belongs. `Required` `Filter(multi eq)` `Owner` |
| [OtherParty](Finance.Excise.ExciseAdministrativeDocuments.md#otherparty) | [Parties](General.Contacts.Parties.md) | The other party, receiving the goods (Consignee). `Required` `Filter(multi eq)` |
| [TaxWarehouse](Finance.Excise.ExciseAdministrativeDocuments.md#taxwarehouse) | [TaxWarehouses](Finance.Excise.TaxWarehouses.md) | Our warehouse, dispatching the goods (Consignor). `Required` `Filter(multi eq)` |
| [TransportationCarrier](Finance.Excise.ExciseAdministrativeDocuments.md#transportationcarrier) | [Carriers](Logistics.Shipment.Carriers.md) | The carrier used for the transportation of the goods. `Required` `Filter(multi eq)` |
| [TransportationVehicle](Finance.Excise.ExciseAdministrativeDocuments.md#transportationvehicle) | [TransportationVehicles](Logistics.Shipment.TransportationVehicles.md) | The vehicle, used for the transportation of the goods. `Required` `Filter(multi eq)` |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Lines | [ExciseAdministrativeDocumentLines](Finance.Excise.ExciseAdministrativeDocumentLines.md) | List of `ExciseAdministrative<br />DocumentLine`(Finance.Excise.ExciseAdministrative<br />DocumentLines.md) child objects, based on the `Finance.Excise.ExciseAdministrative<br />DocumentLine.ExciseAdministrative<br />Document`(Finance.Excise.ExciseAdministrative<br />DocumentLines.md#exciseadministrativedocument) back reference 


## Attribute Details

### AdministrativeReferenceCode

The reference code, returned the customs authorities, when the document is exported to them. null means the document is not yet exported to the authorities.

_Type_: **string (16) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **16**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsDeferredSubmission

Indicates whether the movement has begun under the cover of a paper administrative document. `Required` `Default(false)`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  


## Reference Details

### Document

The Document to which this ExciseAdministrativeDocument belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Documents](General.Documents.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### OtherParty

The other party, receiving the goods (Consignee). `Required` `Filter(multi eq)`

_Type_: **[Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### TaxWarehouse

Our warehouse, dispatching the goods (Consignor). `Required` `Filter(multi eq)`

_Type_: **[TaxWarehouses](Finance.Excise.TaxWarehouses.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### TransportationCarrier

The carrier used for the transportation of the goods. `Required` `Filter(multi eq)`

_Type_: **[Carriers](Logistics.Shipment.Carriers.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### TransportationVehicle

The vehicle, used for the transportation of the goods. `Required` `Filter(multi eq)`

_Type_: **[TransportationVehicles](Logistics.Shipment.TransportationVehicles.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Finance.Excise.ExciseAdministrativeDocuments erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Excise.ExciseAdministrativeDocuments erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Excise_ExciseAdministrativeDocuments?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Excise_ExciseAdministrativeDocuments?$top=10>

