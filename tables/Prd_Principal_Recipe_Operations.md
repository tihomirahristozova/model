# Table Prd_Principal_Recipe_Operations

Contains the operations within a principal recipe. Entity: Prd_Principal_Recipe_Operations

# Aggregate Hierarchy

* [Prd_Principal_Recipes](Prd_Principal_Recipes.md)
* [Gen_Product_Groups](Gen_Product_Groups.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Id|`Guid`|`PK`, Readonly||
|Conditional_Property_Description|`MultilanguageString`||The desired description of the Conditional Property. . |
|Conditional_Property_Value|`String`||The desired value of the Conditional Property. . |
|Line_Ord|`Int32`||Consecutive line number within the principal recipe. `Required` |
|Minimum_Concurrent_Start_Time_Minutes|`Int32?`||How many minutes after the start of the previous operation can this operation start. null means that this operation should wait the previous operation to finish before starting. |
|Move_Time_Minutes|`Int32`||Time to move the lot to the next operation in minutes. `Required` `Default(0)` `Filter(ge;le)` |
|Notes|`String`||Notes for this PrincipalRecipeOperation. |
|Operation_Description|`String`||The description of the operation. Initially copied from the generic operation definition. |
|Run_Time_Minutes|`Int32`||Duration of the operation for one piece in the standard measurement unit of the product. `Required` `Default(0)` `Filter(ge;le)` |
|Scrap_Rate|`Decimal`||Standard rate of scrap during the operation. `Required` `Default(0)` |
|Setup_Time_Minutes|`Int32`||Time needed to setup the equipment. `Required` `Default(0)` `Filter(ge;le)` |
|Tooling|`String`||The tools needed for the routing step. |
|Wait_Time_Minutes|`Int32`||Wait time (drying, cooling, etc.) after the operation in minutes. `Required` `Default(0)` `Filter(ge;le)` |
