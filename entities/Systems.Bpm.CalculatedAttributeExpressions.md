---
uid: Systems.Bpm.CalculatedAttributeExpressions
---
# Systems.Bpm.CalculatedAttributeExpressions Entity

**Namespace:** [Systems.Bpm](Systems.Bpm.md)  

Represent an expression within the calculation of a calculated attribute. Entity: Sys_Calculated_Attribute_Expressions

## Default Visualization
Default Display Text Format:  
_{CalculatedAttribute.Name:T}_  
Default Search Member:  
_CalculatedAttribute.Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Systems.Bpm.CalculatedAttributes](Systems.Bpm.CalculatedAttributes.md)  
Aggregate Root:  
[Systems.Bpm.CalculatedAttributes](Systems.Bpm.CalculatedAttributes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ExpressionNo](Systems.Bpm.CalculatedAttributeExpressions.md#expressionno) | int32 | Unique number of the expression within the attribute. Expression No 0 is the default expression, which provides the result value of the attribute. `Required` 
| [Id](Systems.Bpm.CalculatedAttributeExpressions.md#id) | guid |  
| [Notes](Systems.Bpm.CalculatedAttributeExpressions.md#notes) | string (max) __nullable__ | Notes for this CalculatedAttribute<br />Expression. 
| [Operator](Systems.Bpm.CalculatedAttributeExpressions.md#operator) | [ExpressionOperator](Systems.Bpm.CalculatedAttributeExpressions.md#operator) | The exprssion operator. Available operators are limited to a pre-selected list of operators. `Required` 
| [Parameter1Type](Systems.Bpm.CalculatedAttributeExpressions.md#parameter1type) | [ExpressionParameterType](Systems.Bpm.CalculatedAttributeExpressions.md#parameter1type) __nullable__ | The type of the parameter specifies how to obtain the parameter value. 
| [Parameter1Value](Systems.Bpm.CalculatedAttributeExpressions.md#parameter1value) | string (256) __nullable__ | The actual value of parameter 1. 
| [Parameter2Type](Systems.Bpm.CalculatedAttributeExpressions.md#parameter2type) | [ExpressionParameterType](Systems.Bpm.CalculatedAttributeExpressions.md#parameter2type) __nullable__ | The type of the parameter specifies how to obtain the parameter value. 
| [Parameter2Value](Systems.Bpm.CalculatedAttributeExpressions.md#parameter2value) | string (256) __nullable__ | The actual value of the parameter. 
| [Parameter3Type](Systems.Bpm.CalculatedAttributeExpressions.md#parameter3type) | [ExpressionParameterType](Systems.Bpm.CalculatedAttributeExpressions.md#parameter3type) __nullable__ | The type of the parameter specifies how to obtain the parameter value. 
| [Parameter3Value](Systems.Bpm.CalculatedAttributeExpressions.md#parameter3value) | string (256) __nullable__ | The actual value of the parameter. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CalculatedAttribute](Systems.Bpm.CalculatedAttributeExpressions.md#calculatedattribute) | [CalculatedAttributes](Systems.Bpm.CalculatedAttributes.md) | The `CalculatedAttribute`(Systems.Bpm.CalculatedAttribute<br />Expressions.md#calculatedattribute) to which this CalculatedAttribute<br />Expression belongs. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### ExpressionNo

Unique number of the expression within the attribute. Expression No 0 is the default expression, which provides the result value of the attribute. `Required`

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( obj.CalculatedAttribute.Expressions.Select( c => c.ExpressionNo).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.CalculatedAttribute.Expressions.Select( c => c.ExpressionNo).DefaultIfEmpty( 0).Max( ) + 10)`
### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

Notes for this CalculatedAttributeExpression.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### Operator

The exprssion operator. Available operators are limited to a pre-selected list of operators. `Required`

_Type_: **[ExpressionOperator](Systems.Bpm.CalculatedAttributeExpressions.md#operator)**  
Generic enum type for ExpressionOperator properties  
_Allowed Values (Systems.Bpm.ExpressionOperator Enum Members)_  

| Value | Description |
| ---- | --- |
| ADD | ADD value. Stored as 'ADD'. <br /> _Database Value:_ 'ADD' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'ADD' |
| ADDDAYS | ADDDAYS value. Stored as 'ADDDAYS'. <br /> _Database Value:_ 'ADDDAYS' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'ADDDAYS' |
| AND | AND value. Stored as 'AND'. <br /> _Database Value:_ 'AND' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'AND' |
| CAST | CAST value. Stored as 'CAST'. <br /> _Database Value:_ 'CAST' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'CAST' |
| CEILING | CEILING value. Stored as 'CEILING'. <br /> _Database Value:_ 'CEILING' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'CEILING' |
| CONCAT | CONCAT value. Stored as 'CONCAT'. <br /> _Database Value:_ 'CONCAT' <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'CONCAT' |
| CONVERT | CONVERT value. Stored as 'CONVERT'. <br /> _Database Value:_ 'CONVERT' <br /> _Model Value:_ 6 <br /> _Domain API Value:_ 'CONVERT' |
| COUNT | COUNT value. Stored as 'COUNT'. <br /> _Database Value:_ 'COUNT' <br /> _Model Value:_ 7 <br /> _Domain API Value:_ 'COUNT' |
| DIVIDE | DIVIDE value. Stored as 'DIVIDE'. <br /> _Database Value:_ 'DIVIDE' <br /> _Model Value:_ 8 <br /> _Domain API Value:_ 'DIVIDE' |
| IN | IN value. Stored as 'IN'. <br /> _Database Value:_ 'IN' <br /> _Model Value:_ 9 <br /> _Domain API Value:_ 'IN' |
| IIF | IIF value. Stored as 'IIF'. <br /> _Database Value:_ 'IIF' <br /> _Model Value:_ 10 <br /> _Domain API Value:_ 'IIF' |
| INCNUM | INCNUM value. Stored as 'INCNUM'. <br /> _Database Value:_ 'INCNUM' <br /> _Model Value:_ 11 <br /> _Domain API Value:_ 'INCNUM' |
| EQUAL | EQUAL value. Stored as 'EQUAL'. <br /> _Database Value:_ 'EQUAL' <br /> _Model Value:_ 12 <br /> _Domain API Value:_ 'EQUAL' |
| FILTER | FILTER value. Stored as 'FILTER'. <br /> _Database Value:_ 'FILTER' <br /> _Model Value:_ 13 <br /> _Domain API Value:_ 'FILTER' |
| FIRST | FIRST value. Stored as 'FIRST'. <br /> _Database Value:_ 'FIRST' <br /> _Model Value:_ 14 <br /> _Domain API Value:_ 'FIRST' |
| FLOOR | FLOOR value. Stored as 'FLOOR'. <br /> _Database Value:_ 'FLOOR' <br /> _Model Value:_ 15 <br /> _Domain API Value:_ 'FLOOR' |
| FORMATSTRING | FORMATSTRING value. Stored as 'FORMATSTRING'. <br /> _Database Value:_ 'FORMATSTRING' <br /> _Model Value:_ 16 <br /> _Domain API Value:_ 'FORMATSTRING' |
| GETVALUE | GETVALUE value. Stored as 'GETVALUE'. <br /> _Database Value:_ 'GETVALUE' <br /> _Model Value:_ 17 <br /> _Domain API Value:_ 'GETVALUE' |
| GETOBJVALUE | GETOBJVALUE value. Stored as 'GETOBJVALUE'. <br /> _Database Value:_ 'GETOBJVALUE' <br /> _Model Value:_ 18 <br /> _Domain API Value:_ 'GETOBJVALUE' |
| GT | GT value. Stored as 'GT'. <br /> _Database Value:_ 'GT' <br /> _Model Value:_ 19 <br /> _Domain API Value:_ 'GT' |
| GTE | GTE value. Stored as 'GTE'. <br /> _Database Value:_ 'GTE' <br /> _Model Value:_ 20 <br /> _Domain API Value:_ 'GTE' |
| LIKE | Compare by mask. Use * (asterisk) as wildcard char.. Stored as 'LIKE'. <br /> _Database Value:_ 'LIKE' <br /> _Model Value:_ 21 <br /> _Domain API Value:_ 'LIKE' |
| LIST | LIST value. Stored as 'LIST'. <br /> _Database Value:_ 'LIST' <br /> _Model Value:_ 22 <br /> _Domain API Value:_ 'LIST' |
| LEFT | LEFT value. Stored as 'LEFT'. <br /> _Database Value:_ 'LEFT' <br /> _Model Value:_ 23 <br /> _Domain API Value:_ 'LEFT' |
| LEN | LEN value. Stored as 'LEN'. <br /> _Database Value:_ 'LEN' <br /> _Model Value:_ 24 <br /> _Domain API Value:_ 'LEN' |
| LT | LT value. Stored as 'LT'. <br /> _Database Value:_ 'LT' <br /> _Model Value:_ 25 <br /> _Domain API Value:_ 'LT' |
| LTE | LTE value. Stored as 'LTE'. <br /> _Database Value:_ 'LTE' <br /> _Model Value:_ 26 <br /> _Domain API Value:_ 'LTE' |
| MULTIPLY | MULTIPLY value. Stored as 'MULTIPLY'. <br /> _Database Value:_ 'MULTIPLY' <br /> _Model Value:_ 27 <br /> _Domain API Value:_ 'MULTIPLY' |
| NOT | NOT value. Stored as 'NOT'. <br /> _Database Value:_ 'NOT' <br /> _Model Value:_ 28 <br /> _Domain API Value:_ 'NOT' |
| OR | OR value. Stored as 'OR'. <br /> _Database Value:_ 'OR' <br /> _Model Value:_ 29 <br /> _Domain API Value:_ 'OR' |
| ORDERBY | ORDERBY value. Stored as 'ORDERBY'. <br /> _Database Value:_ 'ORDERBY' <br /> _Model Value:_ 30 <br /> _Domain API Value:_ 'ORDERBY' |
| POS | POS value. Stored as 'POS'. <br /> _Database Value:_ 'POS' <br /> _Model Value:_ 31 <br /> _Domain API Value:_ 'POS' |
| REGEX | REGEX value. Stored as 'REGEX'. <br /> _Database Value:_ 'REGEX' <br /> _Model Value:_ 32 <br /> _Domain API Value:_ 'REGEX' |
| REPLACE | REPLACE value. Stored as 'REPLACE'. <br /> _Database Value:_ 'REPLACE' <br /> _Model Value:_ 33 <br /> _Domain API Value:_ 'REPLACE' |
| RIGHT | RIGHT value. Stored as 'RIGHT'. <br /> _Database Value:_ 'RIGHT' <br /> _Model Value:_ 34 <br /> _Domain API Value:_ 'RIGHT' |
| ROUND | ROUND value. Stored as 'ROUND'. <br /> _Database Value:_ 'ROUND' <br /> _Model Value:_ 35 <br /> _Domain API Value:_ 'ROUND' |
| SELECT | SELECT value. Stored as 'SELECT'. <br /> _Database Value:_ 'SELECT' <br /> _Model Value:_ 36 <br /> _Domain API Value:_ 'SELECT' |
| SORT | SORT value. Stored as 'SORT'. <br /> _Database Value:_ 'SORT' <br /> _Model Value:_ 37 <br /> _Domain API Value:_ 'SORT' |
| SUBSTRING | SUBSTRING value. Stored as 'SUBSTRING'. <br /> _Database Value:_ 'SUBSTRING' <br /> _Model Value:_ 38 <br /> _Domain API Value:_ 'SUBSTRING' |
| SUM | SUM value. Stored as 'SUM'. <br /> _Database Value:_ 'SUM' <br /> _Model Value:_ 39 <br /> _Domain API Value:_ 'SUM' |
| TODAY | TODAY value. Stored as 'TODAY'. <br /> _Database Value:_ 'TODAY' <br /> _Model Value:_ 40 <br /> _Domain API Value:_ 'TODAY' |
| TOLOWER | TOLOWER value. Stored as 'TOLOWER'. <br /> _Database Value:_ 'TOLOWER' <br /> _Model Value:_ 41 <br /> _Domain API Value:_ 'TOLOWER' |
| TOP | TOP value. Stored as 'TOP'. <br /> _Database Value:_ 'TOP' <br /> _Model Value:_ 42 <br /> _Domain API Value:_ 'TOP' |
| TOUPPER | TOUPPER value. Stored as 'TOUPPER'. <br /> _Database Value:_ 'TOUPPER' <br /> _Model Value:_ 43 <br /> _Domain API Value:_ 'TOUPPER' |
| WHERE | WHERE value. Stored as 'WHERE'. <br /> _Database Value:_ 'WHERE' <br /> _Model Value:_ 44 <br /> _Domain API Value:_ 'WHERE' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Parameter1Type

The type of the parameter specifies how to obtain the parameter value.

_Type_: **[ExpressionParameterType](Systems.Bpm.CalculatedAttributeExpressions.md#parameter1type) __nullable__**  
Generic enum type for ExpressionParameterType properties  
_Allowed Values (Systems.Bpm.ExpressionParameterType Enum Members)_  

| Value | Description |
| ---- | --- |
| Constant | Constant value. Stored as 'CONST'. <br /> _Database Value:_ 'CONST' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Constant' |
| Attribute | Attribute value. Stored as 'ATTRIB'. <br /> _Database Value:_ 'ATTRIB' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Attribute' |
| Reference | Reference value. Stored as 'REF'. <br /> _Database Value:_ 'REF' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Reference' |
| ChildList | ChildList value. Stored as 'CHILD'. <br /> _Database Value:_ 'CHILD' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'ChildList' |
| Expression | Expression value. Stored as 'EXP'. <br /> _Database Value:_ 'EXP' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'Expression' |
| Input | Input value. Stored as 'INPUT'. <br /> _Database Value:_ 'INPUT' <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'Input' |
| Repository | Repository value. Stored as 'REPO'. <br /> _Database Value:_ 'REPO' <br /> _Model Value:_ 6 <br /> _Domain API Value:_ 'Repository' |
| System | System value. Stored as 'SYS'. <br /> _Database Value:_ 'SYS' <br /> _Model Value:_ 7 <br /> _Domain API Value:_ 'System' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Parameter1Value

The actual value of parameter 1.

_Type_: **string (256) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **256**  

### Parameter2Type

The type of the parameter specifies how to obtain the parameter value.

_Type_: **[ExpressionParameterType](Systems.Bpm.CalculatedAttributeExpressions.md#parameter2type) __nullable__**  
Generic enum type for ExpressionParameterType properties  
_Allowed Values (Systems.Bpm.ExpressionParameterType Enum Members)_  

| Value | Description |
| ---- | --- |
| Constant | Constant value. Stored as 'CONST'. <br /> _Database Value:_ 'CONST' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Constant' |
| Attribute | Attribute value. Stored as 'ATTRIB'. <br /> _Database Value:_ 'ATTRIB' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Attribute' |
| Reference | Reference value. Stored as 'REF'. <br /> _Database Value:_ 'REF' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Reference' |
| ChildList | ChildList value. Stored as 'CHILD'. <br /> _Database Value:_ 'CHILD' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'ChildList' |
| Expression | Expression value. Stored as 'EXP'. <br /> _Database Value:_ 'EXP' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'Expression' |
| Input | Input value. Stored as 'INPUT'. <br /> _Database Value:_ 'INPUT' <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'Input' |
| Repository | Repository value. Stored as 'REPO'. <br /> _Database Value:_ 'REPO' <br /> _Model Value:_ 6 <br /> _Domain API Value:_ 'Repository' |
| System | System value. Stored as 'SYS'. <br /> _Database Value:_ 'SYS' <br /> _Model Value:_ 7 <br /> _Domain API Value:_ 'System' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Parameter2Value

The actual value of the parameter.

_Type_: **string (256) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **256**  

### Parameter3Type

The type of the parameter specifies how to obtain the parameter value.

_Type_: **[ExpressionParameterType](Systems.Bpm.CalculatedAttributeExpressions.md#parameter3type) __nullable__**  
Generic enum type for ExpressionParameterType properties  
_Allowed Values (Systems.Bpm.ExpressionParameterType Enum Members)_  

| Value | Description |
| ---- | --- |
| Constant | Constant value. Stored as 'CONST'. <br /> _Database Value:_ 'CONST' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Constant' |
| Attribute | Attribute value. Stored as 'ATTRIB'. <br /> _Database Value:_ 'ATTRIB' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Attribute' |
| Reference | Reference value. Stored as 'REF'. <br /> _Database Value:_ 'REF' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Reference' |
| ChildList | ChildList value. Stored as 'CHILD'. <br /> _Database Value:_ 'CHILD' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'ChildList' |
| Expression | Expression value. Stored as 'EXP'. <br /> _Database Value:_ 'EXP' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'Expression' |
| Input | Input value. Stored as 'INPUT'. <br /> _Database Value:_ 'INPUT' <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'Input' |
| Repository | Repository value. Stored as 'REPO'. <br /> _Database Value:_ 'REPO' <br /> _Model Value:_ 6 <br /> _Domain API Value:_ 'Repository' |
| System | System value. Stored as 'SYS'. <br /> _Database Value:_ 'SYS' <br /> _Model Value:_ 7 <br /> _Domain API Value:_ 'System' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Parameter3Value

The actual value of the parameter.

_Type_: **string (256) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **256**  


## Reference Details

### CalculatedAttribute

The `CalculatedAttribute`(Systems.Bpm.CalculatedAttributeExpressions.md#calculatedattribute) to which this CalculatedAttributeExpression belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[CalculatedAttributes](Systems.Bpm.CalculatedAttributes.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list erp.entity=Systems.Bpm.CalculatedAttributeExpressions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Bpm.CalculatedAttributeExpressions erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Bpm_CalculatedAttributeExpressions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Bpm_CalculatedAttributeExpressions?$top=10>

