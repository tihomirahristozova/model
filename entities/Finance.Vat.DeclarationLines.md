---
uid: Finance.Vat.DeclarationLines
---
# Finance.Vat.DeclarationLines Entity

**Namespace:** [Finance.Vat](Finance.Vat.md)  

Contains the VAT declaration lines for declaration, issued by the enterprise company, according to the eligible legislation. Entity: VAT_Declaration_Lines (Introduced in version 22.1.4.22)

## Default Visualization
Default Display Text Format:  
_{LineNo} : {Declaration.DocumentNo} {Declaration.DocumentType.TypeName:T}_  
Default Search Member:  
_Declaration.DocumentNo_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Finance.Vat.Declarations](Finance.Vat.Declarations.md)  
Aggregate Root:  
[Finance.Vat.Declarations](Finance.Vat.Declarations.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [AmountBase](Finance.Vat.DeclarationLines.md#amountbase) | decimal (14, 2) | Declared value in base currency. `Required` `Default(0)` `Filter(eq;ge;le)` 
| [Id](Finance.Vat.DeclarationLines.md#id) | guid |  
| [LineNo](Finance.Vat.DeclarationLines.md#lineno) | int32 | Consecutive line number within the document. `Required` 
| [Notes](Finance.Vat.DeclarationLines.md#notes) | string (max) __nullable__ | Notes for this DeclarationLine. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [BoxType](Finance.Vat.DeclarationLines.md#boxtype) | [BoxTypes](Finance.Vat.BoxTypes.md) | Type of box in VAT declaration. . `Required` `Filter(multi eq)` |
| [Declaration](Finance.Vat.DeclarationLines.md#declaration) | [Declarations](Finance.Vat.Declarations.md) | The `Declaration`(Finance.Vat.DeclarationLines.md#declaration) to which this DeclarationLine belongs. `Required` `Filter(multi eq)` `Owner` |
| [Document](Finance.Vat.DeclarationLines.md#document) | [Declarations](Finance.Vat.Declarations.md) | The `Declaration`(Finance.Vat.DeclarationLines.md#declaration) to which this DeclarationLine belongs. `Required` `Filter(multi eq)` |


## Attribute Details

### AmountBase

Declared value in base currency. `Required` `Default(0)` `Filter(eq;ge;le)`

_Type_: **decimal (14, 2)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LineNo

Consecutive line number within the document. `Required`

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( obj.Declaration.Lines.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.Declaration.Lines.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`
### Notes

Notes for this DeclarationLine.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  


## Reference Details

### BoxType

Type of box in VAT declaration. . `Required` `Filter(multi eq)`

_Type_: **[BoxTypes](Finance.Vat.BoxTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Declaration

The `Declaration`(Finance.Vat.DeclarationLines.md#declaration) to which this DeclarationLine belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Declarations](Finance.Vat.Declarations.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### Document

The `Declaration`(Finance.Vat.DeclarationLines.md#declaration) to which this DeclarationLine belongs. `Required` `Filter(multi eq)`

_Type_: **[Declarations](Finance.Vat.Declarations.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Finance.Vat.DeclarationLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Finance.Vat.DeclarationLines erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Vat_DeclarationLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Vat_DeclarationLines?$top=10>

