---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "Zenduty: Teams"
subcategory: ""
description: |-
  Provides a Zenduty Team Resource. This allows Teams to be created, updated, and deleted.
---

# Resource : zenduty_teams

Provides a Zenduty Team Resource. This allows Teams to be created, updated, and deleted.

## Example Usage
```hcl
    resource "zenduty_teams" "team" {
      name = "exmaple team"
    }

```


<!-- schema generated by tfplugindocs -->
## Argument Reference

* `name` (Required) - Name of the Team (unique) to create team


