# Table Ast_Depreciation_Plan_Templates

Specifies the default depreciation methods for the asset categories. Different methods can be specified for each valuation model. Entity: Ast_Depreciation_Plan_Templates

# Aggregate Hierarchy

* [Ast_Asset_Categories](Ast_Asset_Categories.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Depreciation_Plan_Template_Id|`Guid`|`PK`, Readonly||
|Asset_Life|`Int32?`||Asset life in months by default for the depreciation plans created by this template. null means that the asset is booked for this valuation model but is not depreciated in it (i.e. no depreciation plan is created). |
