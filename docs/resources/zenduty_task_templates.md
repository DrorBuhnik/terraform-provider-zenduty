---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "Zenduty: TaskTemplates"
subcategory: ""
description: |- 
     Provides a Zenduty TaskTemplates Resource. This allows TaskTemplates to be created, updated, and deleted.
  
---

# Resource : zenduty_task_templates 
Provides a Zenduty TaskTemplates Resource. This allows TaskTemplates to be created, updated, and deleted.    
## Example Usage
```hcl
resource "zenduty_teams" "exampleteam" {
  name = "exmaple team"
}
```

```hcl
resource "zenduty_task_templates" "demotemplate" {
  name    = "example template"
  summary = "this is an example template"
  team_id = zenduty_teams.exampleteam.id
}
```


## Argument Reference

* `team_id` - (Required) The unique_id of team to create the tasktemplate in.
* `name` - (Required) The name of the tasktemplate.
* `summary`  - (Required) The summary of the tasktemplate.

## Attributes Reference

The following attributes are exported:

* `id` - The ID of the Zenduty TaskTemplate.

## Import

Team TaskTemplate can be imported using the `team_id`(ie. unique_id of the team) and `task_template_id`(ie. unique_id of the task template), e.g.

```hcl
resource "zenduty_task_templates" "demotemplate" {


}
```

`$ terraform import zenduty_task_templates.demotemplate team_id/task_template_id` 

`$ terraform state show zenduty_task_templates.demotemplate`

`* copy the output data and paste inside zenduty_task_templates.demotemplate resource block and remove the id attribute`

`$ terraform plan` to verify the import




