# Table Bpm_Process_Connections

Contains the connections between process elements. Part of the process model. Entity: Bpm_Process_Connections

## Owner Tables Hierarchy

* [Bpm_Processes](Bpm_Processes.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Process_Connection_Id](#process_connection_id)|`uniqueidentifier` `PK`||
|[Process_Id](#process_id)|`uniqueidentifier` |The process version to which this connection belongs.|
|[Process_Connection_Code](#process_connection_code)|`nvarchar(64)` |Connection code, unique within the process. Used as ID for XML serialization purposes.|
|[Process_Connection_Name](#process_connection_name)|`nvarchar(512)` `ML`|Multilanguage connection name.|
|[Source_Process_Node_Id](#source_process_node_id)|`uniqueidentifier` |The element, from which the connection starts. The element should be in the same process as the connection.|
|[Target_Process_Node_Id](#target_process_node_id)|`uniqueidentifier` |The element, at which the connection ends. The element should be in the same process as the connection.|
|[Condition_Filter_Xml](#condition_filter_xml)|`nvarchar(2147483647)` |When not NULL, specifies that the flow will be followed only if the condition is matched by the current values in the process instance.|
|[Is_Default](#is_default)|`bit` |Denotes this flow as the default sequence flow. It is taken only when all other flows are not valid. For example, gateways usually are followed by several conditional flows and one default flow.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Process_Connection_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Process_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Process_Connection_Code

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Process_Connection_Name

| Property | Value |
| - | - |
|Type|nvarchar(512)|

### Source_Process_Node_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Target_Process_Node_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Condition_Filter_Xml

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Is_Default

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

