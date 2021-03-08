# Table Crm_Sales_Person_Target_Lines

Detail records (lines) of targets for sales persons. Entity: Crm_Sales_Person_Target_Lines

# Aggregate Hierarchy

* [Crm_Sales_Person_Targets](Crm_Sales_Person_Targets.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Sales_Person_Target_Line_Id|`Guid`|`PK`, Readonly||
|Period_Date|`DateTime`|Readonly|Calculated date representation of the target period (used for grouping, filtering and other auxiliary purposes). `Required` `ReadOnly` |
|Period_Month|`Byte`||Month of the period in which the target must be fulfilled (the period is determined by specifying a month and an year). `Required` `Filter(ge;le)` |
|Period_Year|`Int16`||Year of the period in which the target must be fulfilled (the period is determined by specifying a month and an year). `Required` `Filter(ge;le)` |
|Target_Type|`TargetType`|Allowed: `SALES`, `BONUS`, `PROMO`, `LOCNT`|Type of target. Defines the meaning of Target_Value. SALES-sales amount, BONUS-count of bonus progs, PACK-count of promo packs. `Required` `Default("SALES")` `Filter(multi eq)` |
|Target_Value|`Decimal`||Value of target. Meaning depends on target type. `Required` `Default(0)` |
|Target_Weight|`Decimal`||Relative weight of target, comparatively to other targets. `Required` `Default(1)` |
