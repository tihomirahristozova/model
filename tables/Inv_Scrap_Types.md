# Table Inv_Scrap_Types

Types of scrap. Used in store transactions to categorize scrap, when it occurs. Entity: Inv_Scrap_Types

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Scrap_Type_Id|`Guid`|`PK`, Readonly||
|Description|`String`||The description of this ScrapType. `Filter(like)` |
|Is_Planned|`Boolean`||True=Planned (expected) scrap. Scrap of this type will be used to refine planned scrap for future operations. 2=Unexpected scrap. `Required` `Default(true)` `Filter(eq)` |
