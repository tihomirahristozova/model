# Table Crm_Bonus_Programs

Bonus programs allow automatic adding of new line with bonus product or automatic application of discount in a sales document. Entity: Crm_Bonus_Programs

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Bonus_Program_Id|`Guid`|`PK`, Readonly||
|Active|`Boolean`||General condition if the bonus is active. The other conditions are verified only for active bonus programs. `Default(true)` `Filter(eq)` |
|Bonus_Action|`BonusAction`|Allowed: `P`, `D`|Bonus action: P-Add product to the order, A-Add amount, D-Give discount. `Required` `Default("D")` `Filter(multi eq)` |
|Bonus_Document_Amount_Percent|`Decimal?`||The percent of the document amount that is rewarded. Should be null if and only if the bonus document amount is null. |
|Bonus_Line_Discount_Percent|`Decimal`||The percent discount to be applied to bonus lines. Used only for bonus programs with Action = D (Discount). `Required` `Default(0)` |
|Condition_Customer_Filter_XML|`DataAccessFilter`||When not null, specifies that the bonus should be applied only to customers who meet the specified criteria. The criteria could include custom properties. |
|Condition_Distribution_Channel_Filter_XML|`DataAccessFilter`||When not null, specifies that the bonus should be applied only when the distribution channel of the sales order has the specified characteristics. |
|Condition_From_Date|`DateTime?`||Starting date of the bonus. null means that there is no starting date restriction. `Filter(eq;ge;le)` |
|Condition_Ship_To_Customer_Filter_XML|`DataAccessFilter`||When not null, specifies that the bonus should be applied only when shipping to customer with the specified characteristics. |
|Condition_To_Date|`DateTime?`||Ending date (inclusive) of the bonus. null means that there is no ending date restriction. `Filter(eq;ge;le)` |
|Bonus_Program_Name|`MultilanguageString`||The name of the bonus program. `Required` `Filter(eq;like)` |
|Priority|`Priority`|Allowed: `0`, `1`, `2`, `3`, `4`|Priority (1-5) of the bonus program comparative to the other bonus programs. 1 is the lowest priority. `Required` `Default(2)` `Filter(multi eq)` |
