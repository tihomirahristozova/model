# Table Bpm_Process_Lanes

The process lanes categorize elements in the process and contain logic for executor selection. Entity: Bpm_Process_Lanes

## Owner Tables Hierarchy

* [Bpm_Processes](Bpm_Processes.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Process_Lane_Id](#process_lane_id)|`uniqueidentifier` `PK`||
|[Process_Id](#process_id)|`uniqueidentifier` |The process to which this lane belongs|
|[Process_Lane_Name](#process_lane_name)|`nvarchar(254)` `ML`|Multilanguage lane name|
|[Is_System_Executed](#is_system_executed)|`bit` |When set, specifies that the lane allows only system executed tasks and will never have human user as executor.|
|[Offer_To_Role_Id](#offer_to_role_id)|`uniqueidentifier` |When set, the tasks from the lane are offered for assignment to the users with the specified role and the same locality as the process instance.|
|[Assign_To_User_Id](#assign_to_user_id)|`uniqueidentifier` |When set, specifies that tasks from the lane are always assigned to specific user.|
|[Assign_By_Instance_Property_Id](#assign_by_instance_property_id)|`uniqueidentifier` |When set, the user, specified in the instance property will be assigned the task. Mutually exclusive with Assign To User.|
|[User_Condition_Filter_Xml](#user_condition_filter_xml)|`nvarchar(2147483647)` |User defined filter, used to select possible executors of tasks in the lane.|
|[Assign_By_User_Condition](#assign_by_user_condition)|`nvarchar(1)` Allowed: `N`, `R`, `L`|Specifies direct assign action, based on User Condition. N=No direct assignment, only offer to users; R=Assign to random user; L=User with least tasks assigned.|
|[Locality](#locality)|`nvarchar(1)` Allowed: `P`, `L`, `C`, `I`|Process execution locality. Represents where the execution takes place and influences the selection of possible executors. For example, when L, the execution is private to the location, where the process originated. P=Same as parent; L=Location; C=Company; I=Intra-company.|
|[Restrict_To_Single_User](#restrict_to_single_user)|`bit` |Specifies whether the lane would be restricted to the first user, who is assigned an activity in the lane. Subsequent tasks are directly assigned to that user.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Process_Lane_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Process_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Process_Lane_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Is_System_Executed

| Property | Value |
| - | - |
|Type|bit|

### Offer_To_Role_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Assign_To_User_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Assign_By_Instance_Property_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### User_Condition_Filter_Xml

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Assign_By_User_Condition

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Locality

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Restrict_To_Single_User

| Property | Value |
| - | - |
|Type|bit|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


