---
uid: General.PrintoutLayouts
---
# General.PrintoutLayouts

Contains design layouts for document printouts. Entity: Gen_Printout_Layouts

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [BinaryLayout](General.PrintoutLayouts.md#binarylayout) | byte[] (nullable) | The printout layout, when the format requires binary storage. Alternative to Layout. 
| [DocumentEntityName](General.PrintoutLayouts.md#documententityname) | string | The entity name of the document type e.g. Crm_Sales_Orders, Inv_Store_Orders etc. [Required] [Filter(eq)] 
| [Id](General.PrintoutLayouts.md#id) | guid |  
| [Layout](General.PrintoutLayouts.md#layout) | string (nullable) | The textual representation of the printout layout, when the format requires text representation. Alternative to Binary_Layout. 
| [LayoutFormat](General.PrintoutLayouts.md#layoutformat) | string | Format specifier of the layout. Recognized by the application. [Required] [Filter(multi eq)] 
| [Name](General.PrintoutLayouts.md#name) | string | The name of this PrintoutLayout. [Required] [Filter(eq;like)] [ORD] 
| [Notes](General.PrintoutLayouts.md#notes) | string (nullable) | Notes for this PrintoutLayout. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DataSource](General.PrintoutLayouts.md#datasource) | [DataSources](Systems.Reporting.DataSources.md) (nullable) | The data source for the printout. [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| DocumentPrintImages | [DocumentPrintImages](General.DocumentPrintImages.md) | List of [DocumentPrintImage](General.DocumentPrintImages.md) child objects, based on the [General.DocumentPrintImage.PrintoutLayout](General.DocumentPrintImages.md#printoutlayout) back reference 


## Attribute Details

### BinaryLayout

> The printout layout, when the format requires binary storage. Alternative to Layout.

_Type_: **byte[] (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DocumentEntityName

> The entity name of the document type e.g. Crm_Sales_Orders, Inv_Store_Orders etc. [Required] [Filter(eq)]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Layout

> The textual representation of the printout layout, when the format requires text representation. Alternative to Binary_Layout.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### LayoutFormat

> Format specifier of the layout. Recognized by the application. [Required] [Filter(multi eq)]

_Type_: **string**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Name

> The name of this PrintoutLayout. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### Notes

> Notes for this PrintoutLayout.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### DataSource

> The data source for the printout. [Filter(multi eq)]

_Type_: **[DataSources](Systems.Reporting.DataSources.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=General.PrintoutLayouts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.PrintoutLayouts erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.PrintoutLayouts erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_PrintoutLayouts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_PrintoutLayouts?$top=10>

