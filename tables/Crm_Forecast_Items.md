# Table Crm_Forecast_Items

Forecast items form demand in MRP calculations. Entity: Crm_Forecast_Items

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Forecast_Item_Id|`Guid`|`PK`, Readonly||
|Date|`DateTime`||The date for which the sales is forecasted. When forecasting for a period, this contains the first date of the period. `Required` `Filter(ge;le)` |
