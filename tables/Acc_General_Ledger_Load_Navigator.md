# Query Acc_General_Ledger_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Enterprise_Company_Location_Id](#enterprise_company_location_id)|`uniqueidentifier` ||
|[Account_Id](#account_id)|`uniqueidentifier` ||
|[Item_Key](#item_key)|`nvarchar` ||
|[Currency_Id](#currency_id)|`uniqueidentifier` ||
|[Account_Name](#account_name)|`nvarchar` `ML`||
|[Account_Group_Id](#account_group_id)|`uniqueidentifier` ||
|[Start_Balance](#start_balance)|`decimal(0, 0)` ||
|[Debit](#debit)|`decimal(0, 0)` ||
|[Credit](#credit)|`decimal(0, 0)` ||
|[End_Balance](#end_balance)|`decimal(0, 0)` ||
|[Type](#type)|`nvarchar` Allowed: `MV`, `SB`||
|[Start_Balance_Base](#start_balance_base)|`decimal(0, 0)` ||
|[Debit_Base](#debit_base)|`decimal(0, 0)` ||
|[Credit_Base](#credit_base)|`decimal(0, 0)` ||
|[End_Balance_Base](#end_balance_base)|`decimal(0, 0)` ||
|[Correspondant_Account_Id](#correspondant_account_id)|`uniqueidentifier` ||
|[Correspondant_Item_Key](#correspondant_item_key)|`nvarchar` ||
|[Correspondant_Currency_Id](#correspondant_currency_id)|`uniqueidentifier` ||
|[Correspondant_Account_Name](#correspondant_account_name)|`nvarchar` `ML`||
|[Correspondant_Account_Group_Id](#correspondant_account_group_id)|`uniqueidentifier` ||
|[Example_Voucher_Line_Id](#example_voucher_line_id)|`uniqueidentifier` `PK`||
|[Correspondant_Example_Voucher_Line_Id](#correspondant_example_voucher_line_id)|`uniqueidentifier` `PK`||
|[Account_Group_Id_L1_Name](#account_group_id_l1_name)|`nvarchar` `ML`||
|[Account_Group_Id_L2_Name](#account_group_id_l2_name)|`nvarchar` `ML`||
|[Account_Group_Id_L3_Name](#account_group_id_l3_name)|`nvarchar` `ML`||
|[Account_Group_Id_L4_Name](#account_group_id_l4_name)|`nvarchar` `ML`||
|[Account_Group_Id_L5_Name](#account_group_id_l5_name)|`nvarchar` `ML`||
|[Account_Group_Id_L6_Name](#account_group_id_l6_name)|`nvarchar` `ML`||
|[Account_Group_Id_L1_NameOnly](#account_group_id_l1_nameonly)|`nvarchar` `ML`||
|[Account_Group_Id_L1_CodeOnly](#account_group_id_l1_codeonly)|`nvarchar` `ML`||
|[Account_Group_Id_L2_NameOnly](#account_group_id_l2_nameonly)|`nvarchar` `ML`||
|[Account_Group_Id_L2_CodeOnly](#account_group_id_l2_codeonly)|`nvarchar` `ML`||
|[Account_Group_Id_L3_NameOnly](#account_group_id_l3_nameonly)|`nvarchar` `ML`||
|[Account_Group_Id_L3_CodeOnly](#account_group_id_l3_codeonly)|`nvarchar` `ML`||
|[Account_Group_Id_L4_NameOnly](#account_group_id_l4_nameonly)|`nvarchar` `ML`||
|[Account_Group_Id_L4_CodeOnly](#account_group_id_l4_codeonly)|`nvarchar` `ML`||
|[Account_Group_Id_L5_NameOnly](#account_group_id_l5_nameonly)|`nvarchar` `ML`||
|[Account_Group_Id_L5_CodeOnly](#account_group_id_l5_codeonly)|`nvarchar` `ML`||
|[Account_Group_Id_L6_NameOnly](#account_group_id_l6_nameonly)|`nvarchar` `ML`||
|[Account_Group_Id_L6_CodeOnly](#account_group_id_l6_codeonly)|`nvarchar` `ML`||
|[Correspondant_Account_Group_Id_L1_Name](#correspondant_account_group_id_l1_name)|`nvarchar` `ML`||
|[Correspondant_Account_Group_Id_L2_Name](#correspondant_account_group_id_l2_name)|`nvarchar` `ML`||
|[Correspondant_Account_Group_Id_L3_Name](#correspondant_account_group_id_l3_name)|`nvarchar` `ML`||
|[Correspondant_Account_Group_Id_L4_Name](#correspondant_account_group_id_l4_name)|`nvarchar` `ML`||
|[Correspondant_Account_Group_Id_L5_Name](#correspondant_account_group_id_l5_name)|`nvarchar` `ML`||
|[Correspondant_Account_Group_Id_L6_Name](#correspondant_account_group_id_l6_name)|`nvarchar` `ML`||
|[Correspondant_Account_Group_Id_L1_NameOnly](#correspondant_account_group_id_l1_nameonly)|`nvarchar` `ML`||
|[Correspondant_Account_Group_Id_L1_CodeOnly](#correspondant_account_group_id_l1_codeonly)|`nvarchar` `ML`||
|[Correspondant_Account_Group_Id_L2_NameOnly](#correspondant_account_group_id_l2_nameonly)|`nvarchar` `ML`||
|[Correspondant_Account_Group_Id_L2_CodeOnly](#correspondant_account_group_id_l2_codeonly)|`nvarchar` `ML`||
|[Correspondant_Account_Group_Id_L3_NameOnly](#correspondant_account_group_id_l3_nameonly)|`nvarchar` `ML`||
|[Correspondant_Account_Group_Id_L3_CodeOnly](#correspondant_account_group_id_l3_codeonly)|`nvarchar` `ML`||
|[Correspondant_Account_Group_Id_L4_NameOnly](#correspondant_account_group_id_l4_nameonly)|`nvarchar` `ML`||
|[Correspondant_Account_Group_Id_L4_CodeOnly](#correspondant_account_group_id_l4_codeonly)|`nvarchar` `ML`||
|[Correspondant_Account_Group_Id_L5_NameOnly](#correspondant_account_group_id_l5_nameonly)|`nvarchar` `ML`||
|[Correspondant_Account_Group_Id_L5_CodeOnly](#correspondant_account_group_id_l5_codeonly)|`nvarchar` `ML`||
|[Correspondant_Account_Group_Id_L6_NameOnly](#correspondant_account_group_id_l6_nameonly)|`nvarchar` `ML`||
|[Correspondant_Account_Group_Id_L6_CodeOnly](#correspondant_account_group_id_l6_codeonly)|`nvarchar` `ML`||
|[Required_Property_1_Id](#required_property_1_id)|`uniqueidentifier` ||
|[Required_Property_1_Value](#required_property_1_value)|`nvarchar` ||
|[Required_Property_1_Value_Id](#required_property_1_value_id)|`uniqueidentifier` ||
|[Required_Property_1_Description](#required_property_1_description)|`nvarchar` `ML`||
|[Correspondant_Required_Property_1_Id](#correspondant_required_property_1_id)|`uniqueidentifier` ||
|[Correspondant_Required_Property_1_Value](#correspondant_required_property_1_value)|`nvarchar` ||
|[Correspondant_Required_Property_1_Value_Id](#correspondant_required_property_1_value_id)|`uniqueidentifier` ||
|[Correspondant_Required_Property_1_Description](#correspondant_required_property_1_description)|`nvarchar` `ML`||
|[Required_Property_2_Id](#required_property_2_id)|`uniqueidentifier` ||
|[Required_Property_2_Value](#required_property_2_value)|`nvarchar` ||
|[Required_Property_2_Value_Id](#required_property_2_value_id)|`uniqueidentifier` ||
|[Required_Property_2_Description](#required_property_2_description)|`nvarchar` `ML`||
|[Correspondant_Required_Property_2_Id](#correspondant_required_property_2_id)|`uniqueidentifier` ||
|[Correspondant_Required_Property_2_Value](#correspondant_required_property_2_value)|`nvarchar` ||
|[Correspondant_Required_Property_2_Value_Id](#correspondant_required_property_2_value_id)|`uniqueidentifier` ||
|[Correspondant_Required_Property_2_Description](#correspondant_required_property_2_description)|`nvarchar` `ML`||
|[Required_Property_3_Id](#required_property_3_id)|`uniqueidentifier` ||
|[Required_Property_3_Value](#required_property_3_value)|`nvarchar` ||
|[Required_Property_3_Value_Id](#required_property_3_value_id)|`uniqueidentifier` ||
|[Required_Property_3_Description](#required_property_3_description)|`nvarchar` `ML`||
|[Correspondant_Required_Property_3_Id](#correspondant_required_property_3_id)|`uniqueidentifier` ||
|[Correspondant_Required_Property_3_Value](#correspondant_required_property_3_value)|`nvarchar` ||
|[Correspondant_Required_Property_3_Value_Id](#correspondant_required_property_3_value_id)|`uniqueidentifier` ||
|[Correspondant_Required_Property_3_Description](#correspondant_required_property_3_description)|`nvarchar` `ML`||
|[Required_Property_4_Id](#required_property_4_id)|`uniqueidentifier` ||
|[Required_Property_4_Value](#required_property_4_value)|`nvarchar` ||
|[Required_Property_4_Value_Id](#required_property_4_value_id)|`uniqueidentifier` ||
|[Required_Property_4_Description](#required_property_4_description)|`nvarchar` `ML`||
|[Correspondant_Required_Property_4_Id](#correspondant_required_property_4_id)|`uniqueidentifier` ||
|[Correspondant_Required_Property_4_Value](#correspondant_required_property_4_value)|`nvarchar` ||
|[Correspondant_Required_Property_4_Value_Id](#correspondant_required_property_4_value_id)|`uniqueidentifier` ||
|[Correspondant_Required_Property_4_Description](#correspondant_required_property_4_description)|`nvarchar` `ML`||
|[Required_Property_5_Id](#required_property_5_id)|`uniqueidentifier` ||
|[Required_Property_5_Value](#required_property_5_value)|`nvarchar` ||
|[Required_Property_5_Value_Id](#required_property_5_value_id)|`uniqueidentifier` ||
|[Required_Property_5_Description](#required_property_5_description)|`nvarchar` `ML`||
|[Correspondant_Required_Property_5_Id](#correspondant_required_property_5_id)|`uniqueidentifier` ||
|[Correspondant_Required_Property_5_Value](#correspondant_required_property_5_value)|`nvarchar` ||
|[Correspondant_Required_Property_5_Value_Id](#correspondant_required_property_5_value_id)|`uniqueidentifier` ||
|[Correspondant_Required_Property_5_Description](#correspondant_required_property_5_description)|`nvarchar` `ML`||

## Columns

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Item_Key

| Property | Value |
| - | - |
|Type|nvarchar|

### Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Account_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Account_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Start_Balance

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Debit

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Credit

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### End_Balance

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Start_Balance_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Debit_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Credit_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### End_Balance_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Correspondant_Account_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Correspondant_Item_Key

| Property | Value |
| - | - |
|Type|nvarchar|

### Correspondant_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Correspondant_Account_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Correspondant_Account_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Example_Voucher_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Correspondant_Example_Voucher_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Account_Group_Id_L1_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Account_Group_Id_L2_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Account_Group_Id_L3_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Account_Group_Id_L4_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Account_Group_Id_L5_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Account_Group_Id_L6_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Account_Group_Id_L1_NameOnly

| Property | Value |
| - | - |
|Type|nvarchar|

### Account_Group_Id_L1_CodeOnly

| Property | Value |
| - | - |
|Type|nvarchar|

### Account_Group_Id_L2_NameOnly

| Property | Value |
| - | - |
|Type|nvarchar|

### Account_Group_Id_L2_CodeOnly

| Property | Value |
| - | - |
|Type|nvarchar|

### Account_Group_Id_L3_NameOnly

| Property | Value |
| - | - |
|Type|nvarchar|

### Account_Group_Id_L3_CodeOnly

| Property | Value |
| - | - |
|Type|nvarchar|

### Account_Group_Id_L4_NameOnly

| Property | Value |
| - | - |
|Type|nvarchar|

### Account_Group_Id_L4_CodeOnly

| Property | Value |
| - | - |
|Type|nvarchar|

### Account_Group_Id_L5_NameOnly

| Property | Value |
| - | - |
|Type|nvarchar|

### Account_Group_Id_L5_CodeOnly

| Property | Value |
| - | - |
|Type|nvarchar|

### Account_Group_Id_L6_NameOnly

| Property | Value |
| - | - |
|Type|nvarchar|

### Account_Group_Id_L6_CodeOnly

| Property | Value |
| - | - |
|Type|nvarchar|

### Correspondant_Account_Group_Id_L1_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Correspondant_Account_Group_Id_L2_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Correspondant_Account_Group_Id_L3_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Correspondant_Account_Group_Id_L4_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Correspondant_Account_Group_Id_L5_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Correspondant_Account_Group_Id_L6_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Correspondant_Account_Group_Id_L1_NameOnly

| Property | Value |
| - | - |
|Type|nvarchar|

### Correspondant_Account_Group_Id_L1_CodeOnly

| Property | Value |
| - | - |
|Type|nvarchar|

### Correspondant_Account_Group_Id_L2_NameOnly

| Property | Value |
| - | - |
|Type|nvarchar|

### Correspondant_Account_Group_Id_L2_CodeOnly

| Property | Value |
| - | - |
|Type|nvarchar|

### Correspondant_Account_Group_Id_L3_NameOnly

| Property | Value |
| - | - |
|Type|nvarchar|

### Correspondant_Account_Group_Id_L3_CodeOnly

| Property | Value |
| - | - |
|Type|nvarchar|

### Correspondant_Account_Group_Id_L4_NameOnly

| Property | Value |
| - | - |
|Type|nvarchar|

### Correspondant_Account_Group_Id_L4_CodeOnly

| Property | Value |
| - | - |
|Type|nvarchar|

### Correspondant_Account_Group_Id_L5_NameOnly

| Property | Value |
| - | - |
|Type|nvarchar|

### Correspondant_Account_Group_Id_L5_CodeOnly

| Property | Value |
| - | - |
|Type|nvarchar|

### Correspondant_Account_Group_Id_L6_NameOnly

| Property | Value |
| - | - |
|Type|nvarchar|

### Correspondant_Account_Group_Id_L6_CodeOnly

| Property | Value |
| - | - |
|Type|nvarchar|

### Required_Property_1_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Required_Property_1_Value

| Property | Value |
| - | - |
|Type|nvarchar|

### Required_Property_1_Value_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Required_Property_1_Description

| Property | Value |
| - | - |
|Type|nvarchar|

### Correspondant_Required_Property_1_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Correspondant_Required_Property_1_Value

| Property | Value |
| - | - |
|Type|nvarchar|

### Correspondant_Required_Property_1_Value_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Correspondant_Required_Property_1_Description

| Property | Value |
| - | - |
|Type|nvarchar|

### Required_Property_2_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Required_Property_2_Value

| Property | Value |
| - | - |
|Type|nvarchar|

### Required_Property_2_Value_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Required_Property_2_Description

| Property | Value |
| - | - |
|Type|nvarchar|

### Correspondant_Required_Property_2_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Correspondant_Required_Property_2_Value

| Property | Value |
| - | - |
|Type|nvarchar|

### Correspondant_Required_Property_2_Value_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Correspondant_Required_Property_2_Description

| Property | Value |
| - | - |
|Type|nvarchar|

### Required_Property_3_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Required_Property_3_Value

| Property | Value |
| - | - |
|Type|nvarchar|

### Required_Property_3_Value_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Required_Property_3_Description

| Property | Value |
| - | - |
|Type|nvarchar|

### Correspondant_Required_Property_3_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Correspondant_Required_Property_3_Value

| Property | Value |
| - | - |
|Type|nvarchar|

### Correspondant_Required_Property_3_Value_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Correspondant_Required_Property_3_Description

| Property | Value |
| - | - |
|Type|nvarchar|

### Required_Property_4_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Required_Property_4_Value

| Property | Value |
| - | - |
|Type|nvarchar|

### Required_Property_4_Value_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Required_Property_4_Description

| Property | Value |
| - | - |
|Type|nvarchar|

### Correspondant_Required_Property_4_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Correspondant_Required_Property_4_Value

| Property | Value |
| - | - |
|Type|nvarchar|

### Correspondant_Required_Property_4_Value_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Correspondant_Required_Property_4_Description

| Property | Value |
| - | - |
|Type|nvarchar|

### Required_Property_5_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Required_Property_5_Value

| Property | Value |
| - | - |
|Type|nvarchar|

### Required_Property_5_Value_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Required_Property_5_Description

| Property | Value |
| - | - |
|Type|nvarchar|

### Correspondant_Required_Property_5_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Correspondant_Required_Property_5_Value

| Property | Value |
| - | - |
|Type|nvarchar|

### Correspondant_Required_Property_5_Value_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Correspondant_Required_Property_5_Description

| Property | Value |
| - | - |
|Type|nvarchar|


