# Table Prd_Recipe_Operations

Contains the routing (operation list) of the recipes. Entity: Prd_Recipe_Operations

# Aggregate Hierarchy

* [Prd_Recipes](Prd_Recipes.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Id|`Guid`|`PK`, Readonly||
|Line_Ord|`Int32`||Order of the operation within the recipe. `Required` |
|Minimum_Concurrent_Start_Time_Minutes|`Int32?`||How many minutes after the start of this operation can the next operation start. null means that the next operation should wait this operation to finish before starting. |
|Move_Time_Minutes|`Int32`||Time to move the lot to the next operation in minutes. `Required` `Default(0)` |
|Notes|`String`||Notes for this RecipeOperation. |
|Operation_Description|`String`||The description of the operation. |
|Run_Time_Minutes|`Int32`||Duration of the operation for standard lot of the product. `Required` `Default(0)` |
|Scrap_Rate|`Decimal`||Standard rate of scrap during the operation. `Required` `Default(0)` |
|Setup_Time_Minutes|`Int32`||Time needed to setup the equipment. `Required` `Default(0)` |
|Tooling|`String`||The tools needed for the routing step. |
|Wait_Time_Minutes|`Int32`||Wait time (drying, cooling, etc.) after the operation in minutes. `Required` `Default(0)` |
