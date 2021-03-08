# Table Prj_Work_Report_Materials

Each record contains a consumed material, reported by the related Work Report. Entity: Prj_Work_Report_Materials

# Aggregate Hierarchy

* [Prj_Work_Reports](Prj_Work_Reports.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Work_Report_Material_Id|`Guid`|`PK`, Readonly||
|Quantity|`Decimal`||The consumed quantity of the material. `Required` `Default(0)` `Filter(eq;like)` |
|Quantity_Base|`Decimal`|Readonly|The equivalence of Quantity in the base measurement unit of the Material. `Required` `Default(0)` `Filter(eq;like)` `ReadOnly` |
