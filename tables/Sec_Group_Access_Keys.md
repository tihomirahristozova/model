# Table Sec_Group_Access_Keys

Specifies the access keys for which the user groups have permissions. The existance of a record grants read permission. Additional permissions are granted through specialized fields. Entity: Sec_Group_Access_Keys

# Aggregate Hierarchy

* [Sec_Groups](Sec_Groups.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Group_Access_Key_Id|`Guid`|`PK`, Readonly||
|Can_Administer|`Boolean`||When true, the group is granted with administrative permission (allowance to change access key) for the entity, protected by the access key. `Required` `Default(false)` |
|Can_Delete|`Boolean`||When true, the group is granted with delete permission for the entity, protected by the access key. `Required` |
|Can_Update|`Boolean`||When true, the group is granted with update permission for the entity, protected by the access key. `Required` |
|Permission1|`Boolean`||When true, the group is granted with entity-specific permission for the entity, protected by the access key. `Required` `Default(false)` |
|Permission10|`Boolean`||When true, the group is granted with entity-specific permission for the entity, protected by the access key. `Required` `Default(false)` |
|Permission2|`Boolean`||When true, the group is granted with entity-specific permission for the entity, protected by the access key. `Required` `Default(false)` |
|Permission3|`Boolean`||When true, the group is granted with entity-specific permission for the entity, protected by the access key. `Required` `Default(false)` |
|Permission4|`Boolean`||When true, the group is granted with entity-specific permission for the entity, protected by the access key. `Required` `Default(false)` |
|Permission5|`Boolean`||When true, the group is granted with entity-specific permission for the entity, protected by the access key. `Required` `Default(false)` |
|Permission6|`Boolean`||When true, the group is granted with entity-specific permission for the entity, protected by the access key. `Required` `Default(false)` |
|Permission7|`Boolean`||When true, the group is granted with entity-specific permission for the entity, protected by the access key. `Required` `Default(false)` |
|Permission8|`Boolean`||When true, the group is granted with entity-specific permission for the entity, protected by the access key. `Required` `Default(false)` |
|Permission9|`Boolean`||When true, the group is granted with entity-specific permission for the entity, protected by the access key. `Required` `Default(false)` |
