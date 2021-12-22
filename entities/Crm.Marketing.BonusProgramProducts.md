---
uid: Crm.Marketing.BonusProgramProducts
---
# Crm.Marketing.BonusProgramProducts Entity

**Namespace:** [Crm.Marketing](Crm.Marketing.md)  

Provides a way to specify additional (to the one specified in Bonus Program.Conditional Product) products, which will be used to evaluate bonus program conditions. When any of the products exists in the sales document, the conditions are satisfied and the program is applied. When the conditional products list for a bonus program is empty, it is considered that the program is valid for all products. Entity: Crm_Bonus_Program_Products

## Default Visualization
Default Display Text Format:  
_{BonusProgram.Name:T}_  
Default Search Members:  
_BonusProgram.Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Crm.Marketing.BonusPrograms](Crm.Marketing.BonusPrograms.md)  
Aggregate Root:  
[Crm.Marketing.BonusPrograms](Crm.Marketing.BonusPrograms.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.Marketing.BonusProgramProducts.md#id) | guid |  
| [ObjectVersion](Crm.Marketing.BonusProgramProducts.md#objectversion) | int32 |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [BonusProgram](Crm.Marketing.BonusProgramProducts.md#bonusprogram) | [BonusPrograms](Crm.Marketing.BonusPrograms.md) | The <see cref="BonusProgram"/> to which this BonusProgramProduct belongs. `Required` `Filter(multi eq)` `Owner` |
| [Product](Crm.Marketing.BonusProgramProducts.md#product) | [Products](General.Products.Products.md) | The product which is required to exist in the final sales document in order for the bonus program to be applied. `Required` `Filter(multi eq)` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  


## Reference Details

### BonusProgram

The <see cref="BonusProgram"/> to which this BonusProgramProduct belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[BonusPrograms](Crm.Marketing.BonusPrograms.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### Product

The product which is required to exist in the final sales document in order for the bonus program to be applied. `Required` `Filter(multi eq)`

_Type_: **[Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Crm.Marketing.BonusProgramProducts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Crm.Marketing.BonusProgramProducts erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Marketing_BonusProgramProducts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Marketing_BonusProgramProducts?$top=10>

