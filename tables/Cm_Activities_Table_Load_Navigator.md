# Query Cm_Activities_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`||
|[From_Party_Id](#from_party_id)|`uniqueidentifier` ||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` ||
|[Document_No](#document_no)|`nvarchar` ||
|[Document_Date](#document_date)|`date` ||
|[Reference_Date](#reference_date)|`datetime` ||
|[State](#state)|`smallint` Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly||
|[Void](#void)|`bit` Readonly||
|[To_Party_Id](#to_party_id)|`uniqueidentifier` ||
|[Currency_Directory_Id](#currency_directory_id)|`uniqueidentifier` ||
|[Master_Document_Id](#master_document_id)|`uniqueidentifier` ||
|[Parent_Document_Id](#parent_document_id)|`uniqueidentifier` ||
|[Adjusted_Document_Id](#adjusted_document_id)|`uniqueidentifier` ||
|[Adjustment_Number](#adjustment_number)|`int` Readonly||
|[Creation_Time](#creation_time)|`datetime` Readonly||
|[Creation_User](#creation_user)|`nvarchar` Readonly||
|[Void_Time](#void_time)|`datetime` Readonly||
|[Void_User](#void_user)|`nvarchar` Readonly||
|[Adjustment_Time](#adjustment_time)|`datetime` Readonly||
|[Adjustment_User](#adjustment_user)|`nvarchar` Readonly||
|[Read_Only](#read_only)|`bit` Readonly||
|[Document_Notes](#document_notes)|`nvarchar` ||
|[Document_Version](#document_version)|`int` Readonly||
|[Responsible_Person_Id](#responsible_person_id)|`uniqueidentifier` ||
|[Void_Reason](#void_reason)|`nvarchar` Readonly||
|[Reverse_Of_Document_Id](#reverse_of_document_id)|`uniqueidentifier` Readonly||
|[Enterprise_Company_Location_Id](#enterprise_company_location_id)|`uniqueidentifier` ||
|[Planning_Only](#planning_only)|`bit` Readonly||
|[Prime_Cause_Document_Id](#prime_cause_document_id)|`uniqueidentifier` ||
|[Release_Time](#release_time)|`datetime` ||
|[Complete_Time](#complete_time)|`datetime` ||
|[Parent_Document_Relationship_Type](#parent_document_relationship_type)|`nvarchar` Allowed: `S`, `N`||
|[Reference_Document_No](#reference_document_no)|`nvarchar` ||
|[User_Status_Id](#user_status_id)|`uniqueidentifier` Readonly||
|[From_Company_Division_Id](#from_company_division_id)|`uniqueidentifier` ||
|[To_Company_Division_Id](#to_company_division_id)|`uniqueidentifier` ||
|[Entity_Name](#entity_name)|`nvarchar` |The entity name of the document header.|
|[Target_Party_Id_Text](#target_party_id_text)|`nvarchar` ||
|[Party_Code](#party_code)|`nvarchar` ||
|[Responsible_Party_Id_Text](#responsible_party_id_text)|`nvarchar` ||
|[Owner_Party_Id_Text](#owner_party_id_text)|`nvarchar` ||
|[Activity_Id](#activity_id)|`uniqueidentifier` `PK`||
|[System_Type](#system_type)|`nvarchar` Allowed: `C`, `M`, `T`||
|[Subject](#subject)|`nvarchar` ||
|[Notes](#notes)|`nvarchar` ||
|[Target_Party_Id](#target_party_id)|`uniqueidentifier` ||
|[Responsible_Party_Id](#responsible_party_id)|`uniqueidentifier` ||
|[Owner_Party_Id](#owner_party_id)|`uniqueidentifier` ||
|[Priority](#priority)|`tinyint` Allowed: `1`, `2`, `3`, `4`, `5`||
|[Private](#private)|`bit` ||
|[Start_Time](#start_time)|`datetime` ||
|[Deadline_Time](#deadline_time)|`datetime` ||
|[End_Time](#end_time)|`datetime` ||
|[Reminder_Time](#reminder_time)|`datetime` ||
|[Contact_Person_Id](#contact_person_id)|`uniqueidentifier` ||
|[Planned_Duration_Minutes](#planned_duration_minutes)|`int` ||
|[Project_Task_Id](#project_task_id)|`uniqueidentifier` |The project task for which the work is performed. NULL when the activity is not related to a project task.|
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[Target_Party_Name](#target_party_name)|`nvarchar` `ML`||
|[Target_Party_Type](#target_party_type)|`nvarchar` Allowed: `C`, `L`, `P`, `S`, `V`||
|[Target_Party_Code](#target_party_code)|`nvarchar` ||
|[Target_Parent_Party_Id](#target_parent_party_id)|`uniqueidentifier` ||
|[Target_Party_Unique_Number](#target_party_unique_number)|`nvarchar` ||
|[Target_Creation_Time](#target_creation_time)|`datetime` ||
|[Target_Update_Time](#target_update_time)|`datetime` ||
|[Target_Update_User](#target_update_user)|`nvarchar` ||
|[Target_GLN](#target_gln)|`nvarchar` ||
|[Target_Area_Id](#target_area_id)|`uniqueidentifier` ||
|[Target_Default_Product_Coding_System_Id](#target_default_product_coding_system_id)|`uniqueidentifier` ||
|[Target_Administrative_Region_Id](#target_administrative_region_id)|`uniqueidentifier` ||
|[Target_Area_Id_L1_Name](#target_area_id_l1_name)|`nvarchar` `ML`||
|[Target_Area_Id_L2_Name](#target_area_id_l2_name)|`nvarchar` `ML`||
|[Target_Area_Id_L3_Name](#target_area_id_l3_name)|`nvarchar` `ML`||
|[Target_Area_Id_L4_Name](#target_area_id_l4_name)|`nvarchar` `ML`||
|[Target_Area_Id_L5_Name](#target_area_id_l5_name)|`nvarchar` `ML`||
|[Target_Area_Id_L6_Name](#target_area_id_l6_name)|`nvarchar` `ML`||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### From_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_No

| Property | Value |
| - | - |
|Type|nvarchar|

### Document_Date

| Property | Value |
| - | - |
|Type|date|

### Reference_Date

| Property | Value |
| - | - |
|Type|datetime|

### State

| Property | Value |
| - | - |
|Type|smallint|

### Void

| Property | Value |
| - | - |
|Type|bit|

### To_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Currency_Directory_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Master_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Adjusted_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Adjustment_Number

| Property | Value |
| - | - |
|Type|int|

### Creation_Time

| Property | Value |
| - | - |
|Type|datetime|

### Creation_User

| Property | Value |
| - | - |
|Type|nvarchar|

### Void_Time

| Property | Value |
| - | - |
|Type|datetime|

### Void_User

| Property | Value |
| - | - |
|Type|nvarchar|

### Adjustment_Time

| Property | Value |
| - | - |
|Type|datetime|

### Adjustment_User

| Property | Value |
| - | - |
|Type|nvarchar|

### Read_Only

| Property | Value |
| - | - |
|Type|bit|

### Document_Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Document_Version

| Property | Value |
| - | - |
|Type|int|

### Responsible_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Void_Reason

| Property | Value |
| - | - |
|Type|nvarchar|

### Reverse_Of_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Planning_Only

| Property | Value |
| - | - |
|Type|bit|

### Prime_Cause_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Release_Time

| Property | Value |
| - | - |
|Type|datetime|

### Complete_Time

| Property | Value |
| - | - |
|Type|datetime|

### Parent_Document_Relationship_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Reference_Document_No

| Property | Value |
| - | - |
|Type|nvarchar|

### User_Status_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### From_Company_Division_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### To_Company_Division_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Entity_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Target_Party_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Party_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Responsible_Party_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Owner_Party_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Activity_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### System_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Subject

| Property | Value |
| - | - |
|Type|nvarchar|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Target_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Responsible_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Owner_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Priority

| Property | Value |
| - | - |
|Type|tinyint|

### Private

| Property | Value |
| - | - |
|Type|bit|

### Start_Time

| Property | Value |
| - | - |
|Type|datetime|

### Deadline_Time

| Property | Value |
| - | - |
|Type|datetime|

### End_Time

| Property | Value |
| - | - |
|Type|datetime|

### Reminder_Time

| Property | Value |
| - | - |
|Type|datetime|

### Contact_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Planned_Duration_Minutes

| Property | Value |
| - | - |
|Type|int|

### Project_Task_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Is_Single_Execution

| Property | Value |
| - | - |
|Type|bit|

### Is_Released

| Property | Value |
| - | - |
|Type|bit|

### Target_Party_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Target_Party_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Target_Party_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Target_Parent_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Target_Party_Unique_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### Target_Creation_Time

| Property | Value |
| - | - |
|Type|datetime|

### Target_Update_Time

| Property | Value |
| - | - |
|Type|datetime|

### Target_Update_User

| Property | Value |
| - | - |
|Type|nvarchar|

### Target_GLN

| Property | Value |
| - | - |
|Type|nvarchar|

### Target_Area_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Target_Default_Product_Coding_System_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Target_Administrative_Region_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Target_Area_Id_L1_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Target_Area_Id_L2_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Target_Area_Id_L3_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Target_Area_Id_L4_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Target_Area_Id_L5_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Target_Area_Id_L6_Name

| Property | Value |
| - | - |
|Type|nvarchar|

