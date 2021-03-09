# Table Pos_Operators

Represents one operator (person) in one POS location. Entity: Pos_Operators (Introduced in version 19.1)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Pos_Operator_Id](#pos_operator_id)|`uniqueidentifier` `PK`||
|[Pos_Location_Id](#pos_location_id)|`uniqueidentifier` |The POS location where this operator works.|
|[Pos_Operator_Code](#pos_operator_code)|`nvarchar(16)` |Operator code. Unique within the Pos Location.|
|[User_Id](#user_id)|`uniqueidentifier` |The login user for this POS operator.|
|[Pos_Role_Id](#pos_role_id)|`uniqueidentifier` |The role, assigned to the operator. The role indicates the permissions of the operator for this POS location.|
|[Default_Pos_Terminal_Id](#default_pos_terminal_id)|`uniqueidentifier` |The default POS terminal for this opertor. NULL when there is no default.|
|[Starting_Date](#starting_date)|`date` |The first date, when the operator has started working for this POS location.|
|[Termination_Date](#termination_date)|`date` |The date, when the operator has ceased working in this POS location. NULL means, that the operator is still working or the termination date is still unknown.|
|[Is_Active](#is_active)|`bit` |Indicates whether this operator is active and can be chosen for new records.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Pos_Operator_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Pos_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Pos_Operator_Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### User_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Pos_Role_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Default_Pos_Terminal_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Starting_Date

| Property | Value |
| - | - |
|Type|date|

### Termination_Date

| Property | Value |
| - | - |
|Type|date|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


