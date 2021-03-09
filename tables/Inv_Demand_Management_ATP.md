# View Inv_Demand_Management_ATP

Quantities available to promise for the different date periods. Also contains the current and projected availability. Entity: Inv_Demand_Management_ATP

## Summary

| Name | Type | Description |
| - | - | --- |
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |Тhe Enterprise Company, for which the quantities are calculated.|
|[Store_Id](#store_id)|`uniqueidentifier` |The Store, for which the quantities are calculated.|
|[Product_Id](#product_id)|`uniqueidentifier` |The Product, for which the quantities are calculated.|
|[From_Date](#from_date)|`datetime` |Тhe date from which the available to promise quantity is valid.|
|[Movements_Base](#movements_base)|`decimal(38, 3)` |The sum of the quantity of all planned stock movements on this date in а base measurement unit. |
|[Movements_To_Date_Base](#movements_to_date_base)|`decimal(38, 3)` |The sum of the quantity of all planned stock movements until this date (inclusive) in а base measurement unit. The value is cumulative.|
|[Current_Availability_Base](#current_availability_base)|`decimal(38, 3)` |The current availability in а base measurement unit.|
|[Projected_Availability_Base](#projected_availability_base)|`decimal(38, 3)` |Projected Availability in а base measurement unit on the particular date. The value is cumulative and includes the sum of all planned stock movements until this date (inclusive) and the current availability.|
|[ATP_Base](#atp_base)|`decimal(38, 3)` |Indicates the quantity available to promise (in a base unit). It is valid from this date on.|

## Columns

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### From_Date

| Property | Value |
| - | - |
|Type|datetime|

### Movements_Base

| Property | Value |
| - | - |
|Type|decimal(38, 3)|

### Movements_To_Date_Base

| Property | Value |
| - | - |
|Type|decimal(38, 3)|

### Current_Availability_Base

| Property | Value |
| - | - |
|Type|decimal(38, 3)|

### Projected_Availability_Base

| Property | Value |
| - | - |
|Type|decimal(38, 3)|

### ATP_Base

| Property | Value |
| - | - |
|Type|decimal(38, 3)|


