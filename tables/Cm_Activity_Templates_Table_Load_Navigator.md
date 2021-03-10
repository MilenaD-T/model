# Query Cm_Activity_Templates_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Activity_Template_Id](#activity_template_id)|`uniqueidentifier` `PK`||
|[Route_Id](#route_id)|`uniqueidentifier` ||
|[Responsible_Party_Id](#responsible_party_id)|`uniqueidentifier` |If Null the user that starts the generation route is responsible party of the activity.|
|[Activity_Subject_Mask](#activity_subject_mask)|`nvarchar` |A mask that uses fields from the header table of the source document in the specified route and is used to fill the Subject of the generated activity.|
|[Source_Date_Field](#source_date_field)|`nvarchar` |A name of a field from the header or the document table of the source document in the specified route, that will be used along with Additional_Days to set the Start_Time of the generated activity.|
|[Additional_Days](#additional_days)|`int` |The number of days that will be added to the date in the Header_Date_Field. The result value is set to Start_Time of the activity.|
|[Start_Time](#start_time)|`time` |The time of the day when the activity starts|
|[Reminder_Time](#reminder_time)|`time` ||

## Columns

### Activity_Template_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Route_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Responsible_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Activity_Subject_Mask

| Property | Value |
| - | - |
|Type|nvarchar|

### Source_Date_Field

| Property | Value |
| - | - |
|Type|nvarchar|

### Additional_Days

| Property | Value |
| - | - |
|Type|int|

### Start_Time

| Property | Value |
| - | - |
|Type|time|

### Reminder_Time

| Property | Value |
| - | - |
|Type|time|

