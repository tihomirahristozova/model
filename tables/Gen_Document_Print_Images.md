# Table Gen_Document_Print_Images

Contains the data of a printout of a document as it was obtained from the data source in the moment of printing. Entity: Gen_Document_Print_Images

# Aggregate Hierarchy

* [Gen_Printout_Layouts](Gen_Printout_Layouts.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Document_Print_Image_Id|`Guid`|`PK`, Readonly||
|Print_Image|`Byte[]`|`BLOB`|The data of the printout, stored in the format, specified in Print Image Format. `Required` |
|Print_Image_Format|`String`||The format, which is used to represent the print image. Currently, only 'CDS' = Compressed Data Set is supported. `Required` `Default("CDS")` |
