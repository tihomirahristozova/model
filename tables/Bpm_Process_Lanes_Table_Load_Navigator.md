# Query Bpm_Process_Lanes_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Process_Lane_Id](#process_lane_id)|`uniqueidentifier` `PK`||
|[Process_Id](#process_id)|`uniqueidentifier` |The process to which this lane belongs|
|[Process_Lane_Name](#process_lane_name)|`nvarchar` `ML`|Multilanguage lane name|
|[Is_System_Executed](#is_system_executed)|`bit` |When set, specifies that the lane allows only system executed tasks and will never have human user as executor.|
|[Offer_To_Role_Id](#offer_to_role_id)|`uniqueidentifier` |When set, the tasks from the lane are offered for assignment to the users with the specified role and the same locality as the process instance.|
|[Assign_To_User_Id](#assign_to_user_id)|`uniqueidentifier` |When set, specifies that tasks from the lane are always assigned to specific user.|
|[Assign_By_Instance_Property_Id](#assign_by_instance_property_id)|`uniqueidentifier` |When set, the user, specified in the instance property will be assigned the task. Mutually exclusive with Assign To User.|
|[User_Condition_Filter_Xml](#user_condition_filter_xml)|`nvarchar` |User defined filter, used to select possible executors of tasks in the lane.|
|[Assign_By_User_Condition](#assign_by_user_condition)|`nvarchar` Allowed: `N`, `R`, `L`|Specifies direct assign action, based on User Condition. N=No direct assignment, only offer to users; R=Assign to random user; L=User with least tasks assigned.|
|[Locality](#locality)|`nvarchar` Allowed: `P`, `L`, `C`, `I`|Process execution locality. Represents where the execution takes place and influences the selection of possible executors. For example, when L, the execution is private to the location, where the process originated. P=Same as parent; L=Location; C=Company; I=Intra-company.|
|[Restrict_To_Single_User](#restrict_to_single_user)|`bit` |Specifies whether the lane would be restricted to the first user, who is assigned an activity in the lane. Subsequent tasks are directly assigned to that user.|
|[Notes](#notes)|`nvarchar` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Process_Lane_Id


Process_Lane_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|yes|
|Order in Primary Key|1|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|NewGuid|
|Derived From|[Bpm_Process_Lanes](Bpm_Process_Lanes.md).[Process_Lane_Id](Bpm_Process_Lanes.md#process_lane_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|0|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Process_Id


Process_Id


The process to which this lane belongs


The process to which this lane belongs

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Bpm_Processes](Bpm_Processes.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Bpm_Process_Lanes](Bpm_Process_Lanes.md).[Process_Id](Bpm_Process_Lanes.md#process_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|1|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Process_Lane_Name


Process_Lane_Name


Multilanguage lane name


Multilanguage lane name

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|yes|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Bpm_Process_Lanes](Bpm_Process_Lanes.md).[Process_Lane_Name](Bpm_Process_Lanes.md#process_lane_name)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|Like|None|no|no|

### Is_System_Executed


Is_System_Executed


When set, specifies that the lane allows only system executed tasks and will never have human user as executor.


When set, specifies that the lane allows only system executed tasks and will never have human user as executor.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Bpm_Process_Lanes](Bpm_Process_Lanes.md).[Is_System_Executed](Bpm_Process_Lanes.md#is_system_executed)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|3|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Offer_To_Role_Id


Offer_To_Role_Id


When set, the tasks from the lane are offered for assignment to the users with the specified role and the same locality as the process instance.


When set, the tasks from the lane are offered for assignment to the users with the specified role and the same locality as the process instance.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Wf_Roles](Wf_Roles.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Bpm_Process_Lanes](Bpm_Process_Lanes.md).[Offer_To_Role_Id](Bpm_Process_Lanes.md#offer_to_role_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|4|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Assign_To_User_Id


Assign_To_User_Id


When set, specifies that tasks from the lane are always assigned to specific user.


When set, specifies that tasks from the lane are always assigned to specific user.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Sec_Users](Sec_Users.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Bpm_Process_Lanes](Bpm_Process_Lanes.md).[Assign_To_User_Id](Bpm_Process_Lanes.md#assign_to_user_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|5|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Assign_By_Instance_Property_Id


Assign_By_Instance_Property_Id


When set, the user, specified in the instance property will be assigned the task. Mutually exclusive with Assign To User.


When set, the user, specified in the instance property will be assigned the task. Mutually exclusive with Assign To User.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Properties](Gen_Properties.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Bpm_Process_Lanes](Bpm_Process_Lanes.md).[Assign_By_Instance_Property_Id](Bpm_Process_Lanes.md#assign_by_instance_property_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|6|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### User_Condition_Filter_Xml


User_Condition_Filter_Xml


User defined filter, used to select possible executors of tasks in the lane.


User defined filter, used to select possible executors of tasks in the lane.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Bpm_Process_Lanes](Bpm_Process_Lanes.md).[User_Condition_Filter_Xml](Bpm_Process_Lanes.md#user_condition_filter_xml)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|yes|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|7|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|Like|None|no|no|

### Assign_By_User_Condition


Assign_By_User_Condition


Specifies direct assign action, based on User Condition. N=No direct assignment, only offer to users; R=Assign to random user; L=User with least tasks assigned.


Specifies direct assign action, based on User Condition. N=No direct assignment, only offer to users; R=Assign to random user; L=User with least tasks assigned.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`N`, `R`, `L`|
|Default Value|None|
|Derived From|[Bpm_Process_Lanes](Bpm_Process_Lanes.md).[Assign_By_User_Condition](Bpm_Process_Lanes.md#assign_by_user_condition)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|8|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|Like|None|no|no|

### Locality


Locality


Process execution locality. Represents where the execution takes place and influences the selection of possible executors. For example, when L, the execution is private to the location, where the process originated. P=Same as parent; L=Location; C=Company; I=Intra-company.


Process execution locality. Represents where the execution takes place and influences the selection of possible executors. For example, when L, the execution is private to the location, where the process originated. P=Same as parent; L=Location; C=Company; I=Intra-company.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`P`, `L`, `C`, `I`|
|Default Value|None|
|Derived From|[Bpm_Process_Lanes](Bpm_Process_Lanes.md).[Locality](Bpm_Process_Lanes.md#locality)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|9|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|Like|None|no|no|

### Restrict_To_Single_User


Restrict_To_Single_User


Specifies whether the lane would be restricted to the first user, who is assigned an activity in the lane. Subsequent tasks are directly assigned to that user.


Specifies whether the lane would be restricted to the first user, who is assigned an activity in the lane. Subsequent tasks are directly assigned to that user.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Bpm_Process_Lanes](Bpm_Process_Lanes.md).[Restrict_To_Single_User](Bpm_Process_Lanes.md#restrict_to_single_user)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|10|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Notes


Notes

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Bpm_Process_Lanes](Bpm_Process_Lanes.md).[Notes](Bpm_Process_Lanes.md#notes)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|11|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Row_Version


Row_Version

| Property | Value |
| - | - |
|Type|timestamp|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Bpm_Process_Lanes](Bpm_Process_Lanes.md).[Row_Version](Bpm_Process_Lanes.md#row_version)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|12|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|


