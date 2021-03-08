# Table Gen_Product_Catalogs

Product catalogs serve to organize the products for display primarily in web pages. Entity: Gen_Product_Catalogs

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Product_Catalog_Id|`Guid`|`PK`, Readonly||
|Background_Color|`Int32?`||When not null, specifies the background color to use for visualization of the catalog. The color is in RGBA color format. |
|Background_Image|`Byte[]`|`BLOB`|The background image to be used for web visualization of the catalog. null means that background image won't be displayed. |
|Background_Position_Horizontal|`BackgroundPositionHorizontal`|Allowed: `L`, `C`, `R`|Horizontal position of the Background Image. L=Left, C=Center, R=Right. `Required` `Default("L")` |
|Background_Position_Vertical|`BackgroundPositionVertical`|Allowed: `T`, `C`, `B`|Vertical position of the Background Image. T=Top, C=Center, B=Bottom. `Required` `Default("T")` |
|Background_Repeat|`BackgroundRepeat`|Allowed: `R`, `X`, `Y`, `N`|Specifies if and how the background image will be repeated. R=Repeat both vertically and horizontally; X=Repeat only horizontally; Y=Repeat only vertically; N=No repeat. `Required` `Default("R")` |
|Product_Catalog_Code|`String`||Unique catalog code. `Required` |
|Footer_Html|`String`||The footer of the catalog in HTML format. Primarily used for web visualizations of the catalog. null means that there shouldn't be any user-defined footer. |
|Header_Html|`String`||The header of the catalog in HTML format. Primarily used for web visualizations of the catalog. null specifies that there shouldn't be any user-defined header. |
|Logo|`Byte[]`|`BLOB`|The logo of the product catalog. Used for web and other visualization of the catalog. |
|Product_Catalog_Name|`MultilanguageString`||Product catalog name (multilanguage). `Required` |
|Notes|`String`||Notes for this ProductCatalog. |
