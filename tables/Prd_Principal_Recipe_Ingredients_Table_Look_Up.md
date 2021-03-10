# Query Prd_Principal_Recipe_Ingredients_Table_Look_Up


## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`|The Id of the recipe ingredient. This changes for each different line of each different recipe in contrast to the ingredient id, which might be the same for many principal recipes|
|[Ingredient_Name](#ingredient_name)|`nvarchar` |The principal name of the ingredient.|

## Columns

### Id


Id


The Id of the recipe ingredient. This changes for each different line of each different recipe in contrast to the ingredient id, which might be the same for many principal recipes


The Id of the recipe ingredient. This changes for each different line of each different recipe in contrast to the ingredient id, which might be the same for many principal recipes

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|yes|
|Order in Primary Key|1|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|NewGuid|
|Derived From|[Prd_Principal_Recipe_Ingredients](Prd_Principal_Recipe_Ingredients.md).[Id](Prd_Principal_Recipe_Ingredients.md#id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Ingredient_Name


Ingredient_Name


The principal name of the ingredient.


The principal name of the ingredient.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Principal_Recipe_Ingredients](Prd_Principal_Recipe_Ingredients.md).[Ingredient_Name](Prd_Principal_Recipe_Ingredients.md#ingredient_name)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Like|None|no|no|


