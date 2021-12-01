---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "zenduty_roles Data Source - terraform-provider-zenduty"
subcategory: ""
description: |-
---

# zenduty_roles (Data Source)

<!-- schema generated by tfplugindocs -->

## Schema

### Required

- **team_id** (String)

### Optional

- **id** (String) The ID of this resource.

### Read-Only

- **items** (List of Object) (see [below for nested schema](#nestedatt--items))

<a id="nestedatt--items"></a>

### Nested Schema for `items`

Read-Only:

- **creation_date** (String)
- **description** (String)
- **rank** (Number)
- **team** (String)
- **title** (String)
- **unique_id** (String)