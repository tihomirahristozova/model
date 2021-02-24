---
uid: General.DocumentPrintImages
---
# General.DocumentPrintImages Entity

**Namespace:** [General](General.md)  

Contains the data of a printout of a document as it was obtained from the data source in the moment of printing. Entity: Gen_Document_Print_Images

## Default Visualization
Default Display Text Format:  
_{PrintoutLayout.DocumentEntityName:T}_  
Default Search Member:  
_PrintoutLayout.DocumentEntityName_  

## Aggregate
  @aggregates  
Aggregate Parent:  
[General.PrintoutLayouts](General.PrintoutLayouts.md)  
Aggregate Root:  
[General.PrintoutLayouts](General.PrintoutLayouts.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.DocumentPrintImages.md#id) | guid |  
| [PrintImage](General.DocumentPrintImages.md#printimage) | byte[] | The data of the printout, stored in the format, specified in Print Image Format. [Required] 
| [PrintImageFormat](General.DocumentPrintImages.md#printimageformat) | string | The format, which is used to represent the print image. Currently, only 'CDS' = Compressed Data Set is supported. [Required] [Default("CDS")] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [PrintoutLayout](General.DocumentPrintImages.md#printoutlayout) | [PrintoutLayouts](General.PrintoutLayouts.md) | The print layout, which was used for the current printout. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### PrintImage

The data of the printout, stored in the format, specified in Print Image Format. [Required]

_Type_: **byte[]**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PrintImageFormat

The format, which is used to represent the print image. Currently, only 'CDS' = Compressed Data Set is supported. [Required] [Default("CDS")]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **CDS**  


## Reference Details

### PrintoutLayout

The print layout, which was used for the current printout. [Required] [Filter(multi eq)] [Owner]

_Type_: **[PrintoutLayouts](General.PrintoutLayouts.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=General.DocumentPrintImages erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.DocumentPrintImages erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_DocumentPrintImages?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_DocumentPrintImages?$top=10>

