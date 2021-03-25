---
uid: General.PrintoutLayouts
---
# General.PrintoutLayouts Entity

**Namespace:** [General](General.md)  

Contains design layouts for document printouts. Entity: Gen_Printout_Layouts

## Default Visualization
Default Display Text Format:  
_{DocumentEntityName:T}_  
Default Search Member:  
_DocumentEntityName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [General.PrintoutLayouts](General.PrintoutLayouts.md)  
  * [General.DocumentPrintImages](General.DocumentPrintImages.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [BinaryLayout](General.PrintoutLayouts.md#binarylayout) | byte[] (nullable) | The printout layout, when the format requires binary storage. Alternative to Layout. 
| [DocumentEntityName](General.PrintoutLayouts.md#documententityname) | string(64) | The entity name of the document type e.g. Crm_Sales_Orders, Inv_Store_Orders etc. `Required` `Filter(eq)` 
| [Id](General.PrintoutLayouts.md#id) | guid |  
| [Layout](General.PrintoutLayouts.md#layout) | string(2147483647) (nullable) | The textual representation of the printout layout, when the format requires text representation. Alternative to Binary_Layout. 
| [LayoutFormat](General.PrintoutLayouts.md#layoutformat) | string(32) | Format specifier of the layout. Recognized by the application. `Required` `Filter(multi eq)` 
| [Name](General.PrintoutLayouts.md#name) | string(64) | The name of this PrintoutLayout. `Required` `Filter(eq;like)` `ORD` 
| [Notes](General.PrintoutLayouts.md#notes) | string(254) (nullable) | Notes for this PrintoutLayout. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DataSource](General.PrintoutLayouts.md#datasource) | [DataSources](Systems.Reporting.DataSources.md) (nullable) | The data source for the printout. `Filter(multi eq)` |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| DocumentPrintImages | [DocumentPrintImages](General.DocumentPrintImages.md) | List of `DocumentPrintImage`(General.DocumentPrintImages.md) child objects, based on the `General.DocumentPrintImage.PrintoutLayout`(General.DocumentPrintImages.md#printoutlayout) back reference 


## Attribute Details

### BinaryLayout

The printout layout, when the format requires binary storage. Alternative to Layout.

_Type_: **byte[] (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DocumentEntityName

The entity name of the document type e.g. Crm_Sales_Orders, Inv_Store_Orders etc. `Required` `Filter(eq)`

_Type_: **string(64)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Layout

The textual representation of the printout layout, when the format requires text representation. Alternative to Binary_Layout.

_Type_: **string(2147483647) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### LayoutFormat

Format specifier of the layout. Recognized by the application. `Required` `Filter(multi eq)`

_Type_: **string(32)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Maximum Length_: **32**  

### Name

The name of this PrintoutLayout. `Required` `Filter(eq;like)` `ORD`

_Type_: **string(64)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  
_Maximum Length_: **64**  

### Notes

Notes for this PrintoutLayout.

_Type_: **string(254) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  


## Reference Details

### DataSource

The data source for the printout. `Filter(multi eq)`

_Type_: **[DataSources](Systems.Reporting.DataSources.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=General.PrintoutLayouts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.PrintoutLayouts erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_PrintoutLayouts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_PrintoutLayouts?$top=10>

