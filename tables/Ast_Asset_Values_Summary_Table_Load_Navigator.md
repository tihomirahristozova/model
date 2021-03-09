# Query Ast_Asset_Values_Summary_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Asset_Id](#asset_id)|`uniqueidentifier` ||
|[Asset_Name](#asset_name)|`nvarchar` `ML`||
|[Valuation_Model_Id](#valuation_model_id)|`uniqueidentifier` ||
|[Purchase_Date](#purchase_date)|`datetime` ||
|[Deployment_Date](#deployment_date)|`datetime` ||
|[Acquire_Date](#acquire_date)|`datetime` ||
|[Retire_Date](#retire_date)|`datetime` ||
|[Valuation_Date](#valuation_date)|`datetime` ||
|[Depreciation_End_Date](#depreciation_end_date)|`datetime` ||
|[Depreciation_Method_Id](#depreciation_method_id)|`uniqueidentifier` ||
|[Asset_Life](#asset_life)|`int` ||
|[Purchase_Value_Start](#purchase_value_start)|`decimal(0, 0)` ||
|[Purchase_Value_Base_Start](#purchase_value_base_start)|`decimal(0, 0)` ||
|[Depreciation_Value_Start](#depreciation_value_start)|`decimal(0, 0)` ||
|[Depreciation_Value_Base_Start](#depreciation_value_base_start)|`decimal(0, 0)` ||
|[Salvage_Value_Start](#salvage_value_start)|`decimal(0, 0)` ||
|[Salvage_Value_Base_Start](#salvage_value_base_start)|`decimal(0, 0)` ||
|[Positive_Reserve_Value_Start](#positive_reserve_value_start)|`decimal(0, 0)` ||
|[Positive_Reserve_Value_Base_Start](#positive_reserve_value_base_start)|`decimal(0, 0)` ||
|[Negative_Reserve_Value_Start](#negative_reserve_value_start)|`decimal(0, 0)` ||
|[Negative_Reserve_Value_Base_Start](#negative_reserve_value_base_start)|`decimal(0, 0)` ||
|[Purchase_Value_PUR_Change](#purchase_value_pur_change)|`decimal(0, 0)` ||
|[Purchase_Value_SLS_Change](#purchase_value_sls_change)|`decimal(0, 0)` ||
|[Purchase_Value_DEP_Change](#purchase_value_dep_change)|`decimal(0, 0)` ||
|[Purchase_Value_ADJ_Change](#purchase_value_adj_change)|`decimal(0, 0)` ||
|[Purchase_Value_Base_PUR_Change](#purchase_value_base_pur_change)|`decimal(0, 0)` ||
|[Purchase_Value_Base_SLS_Change](#purchase_value_base_sls_change)|`decimal(0, 0)` ||
|[Purchase_Value_Base_DEP_Change](#purchase_value_base_dep_change)|`decimal(0, 0)` ||
|[Purchase_Value_Base_ADJ_Change](#purchase_value_base_adj_change)|`decimal(0, 0)` ||
|[Depreciation_Value_PUR_Change](#depreciation_value_pur_change)|`decimal(0, 0)` ||
|[Depreciation_Value_SLS_Change](#depreciation_value_sls_change)|`decimal(0, 0)` ||
|[Depreciation_Value_DEP_Change](#depreciation_value_dep_change)|`decimal(0, 0)` ||
|[Depreciation_Value_ADJ_Change](#depreciation_value_adj_change)|`decimal(0, 0)` ||
|[Depreciation_Value_Base_PUR_Change](#depreciation_value_base_pur_change)|`decimal(0, 0)` ||
|[Depreciation_Value_Base_SLS_Change](#depreciation_value_base_sls_change)|`decimal(0, 0)` ||
|[Depreciation_Value_Base_DEP_Change](#depreciation_value_base_dep_change)|`decimal(0, 0)` ||
|[Depreciation_Value_Base_ADJ_Change](#depreciation_value_base_adj_change)|`decimal(0, 0)` ||
|[Salvage_Value_PUR_Change](#salvage_value_pur_change)|`decimal(0, 0)` ||
|[Salvage_Value_SLS_Change](#salvage_value_sls_change)|`decimal(0, 0)` ||
|[Salvage_Value_DEP_Change](#salvage_value_dep_change)|`decimal(0, 0)` ||
|[Salvage_Value_ADJ_Change](#salvage_value_adj_change)|`decimal(0, 0)` ||
|[Salvage_Value_Base_PUR_Change](#salvage_value_base_pur_change)|`decimal(0, 0)` ||
|[Salvage_Value_Base_SLS_Change](#salvage_value_base_sls_change)|`decimal(0, 0)` ||
|[Salvage_Value_Base_DEP_Change](#salvage_value_base_dep_change)|`decimal(0, 0)` ||
|[Salvage_Value_Base_ADJ_Change](#salvage_value_base_adj_change)|`decimal(0, 0)` ||
|[Positive_Reserve_Value_PUR_Change](#positive_reserve_value_pur_change)|`decimal(0, 0)` ||
|[Positive_Reserve_Value_SLS_Change](#positive_reserve_value_sls_change)|`decimal(0, 0)` ||
|[Positive_Reserve_Value_DEP_Change](#positive_reserve_value_dep_change)|`decimal(0, 0)` ||
|[Positive_Reserve_Value_ADJ_Change](#positive_reserve_value_adj_change)|`decimal(0, 0)` ||
|[Positive_Reserve_Value_Base_PUR_Change](#positive_reserve_value_base_pur_change)|`decimal(0, 0)` ||
|[Positive_Reserve_Value_Base_SLS_Change](#positive_reserve_value_base_sls_change)|`decimal(0, 0)` ||
|[Positive_Reserve_Value_Base_DEP_Change](#positive_reserve_value_base_dep_change)|`decimal(0, 0)` ||
|[Positive_Reserve_Value_Base_ADJ_Change](#positive_reserve_value_base_adj_change)|`decimal(0, 0)` ||
|[Negative_Reserve_Value_PUR_Change](#negative_reserve_value_pur_change)|`decimal(0, 0)` ||
|[Negative_Reserve_Value_SLS_Change](#negative_reserve_value_sls_change)|`decimal(0, 0)` ||
|[Negative_Reserve_Value_DEP_Change](#negative_reserve_value_dep_change)|`decimal(0, 0)` ||
|[Negative_Reserve_Value_ADJ_Change](#negative_reserve_value_adj_change)|`decimal(0, 0)` ||
|[Negative_Reserve_Value_Base_PUR_Change](#negative_reserve_value_base_pur_change)|`decimal(0, 0)` ||
|[Negative_Reserve_Value_Base_SLS_Change](#negative_reserve_value_base_sls_change)|`decimal(0, 0)` ||
|[Negative_Reserve_Value_Base_DEP_Change](#negative_reserve_value_base_dep_change)|`decimal(0, 0)` ||
|[Negative_Reserve_Value_Base_ADJ_Change](#negative_reserve_value_base_adj_change)|`decimal(0, 0)` ||
|[Purchase_Value_End](#purchase_value_end)|`decimal(0, 0)` ||
|[Purchase_Value_Base_End](#purchase_value_base_end)|`decimal(0, 0)` ||
|[Depreciation_Value_End](#depreciation_value_end)|`decimal(0, 0)` ||
|[Depreciation_Value_Base_End](#depreciation_value_base_end)|`decimal(0, 0)` ||
|[Salvage_Value_End](#salvage_value_end)|`decimal(0, 0)` ||
|[Salvage_Value_Base_End](#salvage_value_base_end)|`decimal(0, 0)` ||
|[Positive_Reserve_Value_End](#positive_reserve_value_end)|`decimal(0, 0)` ||
|[Positive_Reserve_Value_Base_End](#positive_reserve_value_base_end)|`decimal(0, 0)` ||
|[Negative_Reserve_Value_End](#negative_reserve_value_end)|`decimal(0, 0)` ||
|[Negative_Reserve_Value_Base_End](#negative_reserve_value_base_end)|`decimal(0, 0)` ||
|[Reevaluation_Positive_Reserve_BC_Change](#reevaluation_positive_reserve_bc_change)|`decimal(0, 0)` ||
|[Reevaluation_Positive_Reserve_Change](#reevaluation_positive_reserve_change)|`decimal(0, 0)` ||
|[Reevaluation_Salvage_BC_Change](#reevaluation_salvage_bc_change)|`decimal(0, 0)` ||
|[Reevaluation_Salvage_Change](#reevaluation_salvage_change)|`decimal(0, 0)` ||
|[Reevaluation_Negative_Reserve_Change](#reevaluation_negative_reserve_change)|`decimal(0, 0)` ||
|[Reevaluation_Depreciation_Change](#reevaluation_depreciation_change)|`decimal(0, 0)` ||
|[Reevaluation_Purchase_BC_Change](#reevaluation_purchase_bc_change)|`decimal(0, 0)` ||
|[Reevaluation_Purchase_Change](#reevaluation_purchase_change)|`decimal(0, 0)` ||
|[Asset_Category_Id](#asset_category_id)|`uniqueidentifier` |The category of this asset. The category may determine default values for the depreciation plans for the different valuation models for this asset.|
|[Reevaluation_Depreciation_BC_Change](#reevaluation_depreciation_bc_change)|`decimal(0, 0)` ||
|[Reevaluation_Negative_Reserve_BC_Change](#reevaluation_negative_reserve_bc_change)|`decimal(0, 0)` ||

## Columns

### Asset_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Asset_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Valuation_Model_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Purchase_Date

| Property | Value |
| - | - |
|Type|datetime|

### Deployment_Date

| Property | Value |
| - | - |
|Type|datetime|

### Acquire_Date

| Property | Value |
| - | - |
|Type|datetime|

### Retire_Date

| Property | Value |
| - | - |
|Type|datetime|

### Valuation_Date

| Property | Value |
| - | - |
|Type|datetime|

### Depreciation_End_Date

| Property | Value |
| - | - |
|Type|datetime|

### Depreciation_Method_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Asset_Life

| Property | Value |
| - | - |
|Type|int|

### Purchase_Value_Start

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Purchase_Value_Base_Start

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Depreciation_Value_Start

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Depreciation_Value_Base_Start

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Salvage_Value_Start

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Salvage_Value_Base_Start

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Positive_Reserve_Value_Start

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Positive_Reserve_Value_Base_Start

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Negative_Reserve_Value_Start

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Negative_Reserve_Value_Base_Start

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Purchase_Value_PUR_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Purchase_Value_SLS_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Purchase_Value_DEP_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Purchase_Value_ADJ_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Purchase_Value_Base_PUR_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Purchase_Value_Base_SLS_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Purchase_Value_Base_DEP_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Purchase_Value_Base_ADJ_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Depreciation_Value_PUR_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Depreciation_Value_SLS_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Depreciation_Value_DEP_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Depreciation_Value_ADJ_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Depreciation_Value_Base_PUR_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Depreciation_Value_Base_SLS_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Depreciation_Value_Base_DEP_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Depreciation_Value_Base_ADJ_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Salvage_Value_PUR_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Salvage_Value_SLS_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Salvage_Value_DEP_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Salvage_Value_ADJ_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Salvage_Value_Base_PUR_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Salvage_Value_Base_SLS_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Salvage_Value_Base_DEP_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Salvage_Value_Base_ADJ_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Positive_Reserve_Value_PUR_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Positive_Reserve_Value_SLS_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Positive_Reserve_Value_DEP_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Positive_Reserve_Value_ADJ_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Positive_Reserve_Value_Base_PUR_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Positive_Reserve_Value_Base_SLS_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Positive_Reserve_Value_Base_DEP_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Positive_Reserve_Value_Base_ADJ_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Negative_Reserve_Value_PUR_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Negative_Reserve_Value_SLS_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Negative_Reserve_Value_DEP_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Negative_Reserve_Value_ADJ_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Negative_Reserve_Value_Base_PUR_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Negative_Reserve_Value_Base_SLS_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Negative_Reserve_Value_Base_DEP_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Negative_Reserve_Value_Base_ADJ_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Purchase_Value_End

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Purchase_Value_Base_End

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Depreciation_Value_End

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Depreciation_Value_Base_End

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Salvage_Value_End

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Salvage_Value_Base_End

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Positive_Reserve_Value_End

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Positive_Reserve_Value_Base_End

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Negative_Reserve_Value_End

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Negative_Reserve_Value_Base_End

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Reevaluation_Positive_Reserve_BC_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Reevaluation_Positive_Reserve_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Reevaluation_Salvage_BC_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Reevaluation_Salvage_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Reevaluation_Negative_Reserve_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Reevaluation_Depreciation_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Reevaluation_Purchase_BC_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Reevaluation_Purchase_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Asset_Category_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Reevaluation_Depreciation_BC_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Reevaluation_Negative_Reserve_BC_Change

| Property | Value |
| - | - |
|Type|decimal(0, 0)|


