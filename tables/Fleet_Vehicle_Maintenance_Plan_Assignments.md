# Table Fleet_Vehicle_Maintenance_Plan_Assignments

Represents assignment of a maintenance plan to a vehicle. Entity: Fleet_Vehicle_Maintenance_Plan_Assignments

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Vehicle_Maintenance_Plan_Assignment_Id|`Guid`|`PK`, Readonly||
|Is_Active|`Boolean`||Specifies whether the plan is active. `Required` `Default(true)` |
|Last_Maintenance_Mileage_Km|`Int32?`||The mileage of the vehicle (in Kilometers), when the last maintenance of this type occurred. Should be specified for plans, which require mileage check. |
|Last_Maintenance_Trip_Count|`Int32?`||The trip count of the vehicle, when the last maintenance of this type occurred. Should be specified for plans, which trip count check. |
|Notes|`String`||Notes for this VehicleMaintenancePlanAssignment. |
|Starting_Date|`DateTime`||The date on which the periodic maintenance should start. `Required` |
