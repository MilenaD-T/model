---
uid: Projects.ProjectTaskResources
---
# Projects.ProjectTaskResources

Contains the resources, required by the project tasks. Entity: Prj_Project_Task_Resources

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [BillingPricePerHour](Projects.ProjectTaskResources.md#billingpriceperhour) | decimal (nullable) | When not null, specifies the price per hour (in the currency of the Project) of resource usage which will be used for billing. null means that the item will be billed in another way. This way of billing is mutually exclusive with Fixed Total Price. [Filter(eq)] 
| [BillingTotalAmount](Projects.ProjectTaskResources.md#billingtotalamount) | decimal (nullable) | When not null, specifies that this item will be billed for the specified fixed total price (in the currency of the Project). null means that this item will be billed in another way. This way of billing is mutually exclusive with Billing Price Per Hour. [Filter(eq)] 
| [CostPerHour](Projects.ProjectTaskResources.md#costperhour) | decimal | Cost per hour for the resource usage for this task (in the currency of the project). [Required] [Default(0)] [Filter(eq)] 
| [Id](Projects.ProjectTaskResources.md#id) | guid |  
| [Notes](Projects.ProjectTaskResources.md#notes) | string (nullable) | Notes for this ProjectTaskResource. 
| [PerUseCost](Projects.ProjectTaskResources.md#perusecost) | [Amount](../data-types.md#amount) (nullable) | One time cost for each resource usage, specified in the projects currency. [Currency: ProjectTask.Project.BudgetingCurrency] 
| [ResourceUsageHours](Projects.ProjectTaskResources.md#resourceusagehours) | decimal | The total number of resource-hours, which are planned for this task. Equals to the length of the task, multiplied by the resource usage. [Required] [Default(0)] [Filter(eq)] 
| [ResourceUsagePercent](Projects.ProjectTaskResources.md#resourceusagepercent) | decimal | The planned resource usage for this activity in percents. Values of more than 100% are allowed when more than 1 resource is required. [Required] [Default(1)] [Filter(eq)] 
| [TaskTotalCost](Projects.ProjectTaskResources.md#tasktotalcost) | decimal | Total cost for this task (in the currency of the project). [Required] [Default(0)] [Filter(eq)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ProjectTask](Projects.ProjectTaskResources.md#projecttask) | [Projects.ProjectTasks](Projects.ProjectTasks.md) | The task for which the resource is planned. [Required] [Filter(multi eq)] [Owner] |
| [Resource](Projects.ProjectTaskResources.md#resource) | [General.Resources.Resources](General.Resources.Resources.md) | The planned resource. [Required] [Filter(multi eq)] |
| [ResourceInstance](Projects.ProjectTaskResources.md#resourceinstance) | [General.Resources.ResourceInstances](General.Resources.ResourceInstances.md) (nullable) | The concrete resource instance, which should be used. null when no specific resource instance is required. [Filter(multi eq)] |


## Attribute Details

### BillingPricePerHour

> When not null, specifies the price per hour (in the currency of the Project) of resource usage which will be used for billing. null means that the item will be billed in another way. This way of billing is mutually exclusive with Fixed Total Price. [Filter(eq)]

_Type_: **decimal (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF(((obj.BillingTotalAmount != null) AndAlso (obj.BillingPricePerHour != null)), null, obj.BillingPricePerHour)`
### BillingTotalAmount

> When not null, specifies that this item will be billed for the specified fixed total price (in the currency of the Project). null means that this item will be billed in another way. This way of billing is mutually exclusive with Billing Price Per Hour. [Filter(eq)]

_Type_: **decimal (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF(((obj.BillingTotalAmount != null) AndAlso (obj.BillingPricePerHour != null)), null, obj.BillingTotalAmount)`
### CostPerHour

> Cost per hour for the resource usage for this task (in the currency of the project). [Required] [Default(0)] [Filter(eq)]

_Type_: **decimal**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **0**  

_Front-End Recalc Expressions:_  
`IIF(((obj.PerUseCost != null) AndAlso (obj.ResourceUsageHours != 0)), ((obj.TaskTotalCost - obj.PerUseCost.Value) / obj.ResourceUsageHours), obj.CostPerHour)`
### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

> Notes for this ProjectTaskResource.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PerUseCost

> One time cost for each resource usage, specified in the projects currency. [Currency: ProjectTask.Project.BudgetingCurrency]

_Type_: **[Amount](../data-types.md#amount) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ResourceUsageHours

> The total number of resource-hours, which are planned for this task. Equals to the length of the task, multiplied by the resource usage. [Required] [Default(0)] [Filter(eq)]

_Type_: **decimal**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **0**  

_Front-End Recalc Expressions:_  
`IIF((obj.ProjectTask != null), (obj.ProjectTask.PlannedDurationHours * obj.ResourceUsagePercent), obj.ResourceUsageHours)`
### ResourceUsagePercent

> The planned resource usage for this activity in percents. Values of more than 100% are allowed when more than 1 resource is required. [Required] [Default(1)] [Filter(eq)]

_Type_: **decimal**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **1**  

_Front-End Recalc Expressions:_  
`IIF((obj.ProjectTask.PlannedDurationHours == 0), 0, (obj.ResourceUsageHours / obj.ProjectTask.PlannedDurationHours))`
### TaskTotalCost

> Total cost for this task (in the currency of the project). [Required] [Default(0)] [Filter(eq)]

_Type_: **decimal**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **0**  

_Back-End Default Expression:_  
`((obj.ResourceUsageHours * obj.CostPerHour) + obj.PerUseCost.Value)`

_Front-End Recalc Expressions:_  
`IIF((obj.PerUseCost != null), ((obj.ResourceUsageHours * obj.CostPerHour) + obj.PerUseCost.Value), obj.TaskTotalCost)`

## Reference Details

### ProjectTask

> The task for which the resource is planned. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Projects.ProjectTasks](Projects.ProjectTasks.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Resource

> The planned resource. [Required] [Filter(multi eq)]

_Type_: **[General.Resources.Resources](General.Resources.Resources.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ResourceInstance

> The concrete resource instance, which should be used. null when no specific resource instance is required. [Filter(multi eq)]

_Type_: **[General.Resources.ResourceInstances](General.Resources.ResourceInstances.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Projects.ProjectTaskResources erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Projects.ProjectTaskResources erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Projects.ProjectTaskResources erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Projects_ProjectTaskResources?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Projects_ProjectTaskResources?$top=10>
