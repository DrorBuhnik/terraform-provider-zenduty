---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "Zenduty: PostIncidentTasks"
subcategory: ""
description: |- 
     Provides a Zenduty PostIncidentTasks Resource. This allows PostIncidentTasks to be created, updated, and deleted.
  
---

# Resource : zenduty_post_incident_tasks 
Provides a Zenduty PostIncidentTasks Resource. This allows PostIncidentTasks to be created, updated, and deleted.    
## Example Usage
```hcl
resource "zenduty_teams" "exampleteam" {
  name = "exmaple team"
}
```


```hcl
resource "zenduty_post_incident_tasks" "demotask" {
  title       = "demo task template"
  description = "this is a description of demo task"
  team_id     = zenduty_teams.exampleteam.id
  due_in_time = "YYYY-MM-DD HH:MM"
  status      = 0
}
```


## Argument Reference

* `team_id` - (Required) The unique_id of team.
* `title` - (Required) The title of the task.
* `description`  - (Required) The description of the task.
* `status` - (Optional) the status of the task choices are `0` is To-Do,`1` is In-Progress, `2`- Done
* `due_in_time` - (Optional) The due time of the task in format YYYY-MM-DD HH:MM.
* `assigned_to` - (Optional) username of the user to assign the task
## Attributes Reference

The following attributes are exported:

* `id` - The ID of the Zenduty PostIncidentTasks.

## Import

Team PostIncidentTask can be imported using the `team_id`(ie. unique_id of the team) and `task_id`(ie. unique_id of the task template)

```hcl
resource "zenduty_post_incident_tasks" "demotask" {


}
```

`$ terraform import zenduty_post_incident_tasks.demotask team_id/task_id` 

`$ terraform state show zenduty_post_incident_tasks.demotask`

`* copy the output data and paste inside zenduty_post_incident_tasks.demotask resource block and remove the id attribute`

`$ terraform plan` to verify the import




