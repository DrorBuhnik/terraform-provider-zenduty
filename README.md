---
# generated by https://github.com/hashicorp/terraform-plugin-docs\
layout: "zenduty"
page_title: "Zenduty Provider"
subcategory: ""
description: |-
---

# Zenduty Provider

The Zenduty provider is used to interact with the zenduty service. The provider needs to be configured with the proper credentials before it can be used.

## Example Usage

```hcl

# Configure the zenduty provider

terraform {
  required_providers {
    zenduty = {
      source = "zenduty/zenduty"
      version = ">= 0.1.0"
    }
  }
}


provider "zenduty" {
  # Configuration options
}

```

# Configuration options

The zenduty provider offers two means of providing credentials for authentication.

- Static credentials
- Environment variables

### Static credentials

!> **Warning:** Hard-coding credentials into any Terraform configuration is not
recommended, and risks secret leakage should this file ever be committed to a
public version control system.

Static credentials can be provided by adding `token` in-line in
the Zenduty provider block.

```hcl
provider "zenduty" {
  # Configuration options
    token = "your api key"
}

```

### Environment Variables

You can provide your credentials via the `ZENDUTY_API_KEY` environment variables.

Usage:

```sh
$ export ZENDUTY_API_KEY="your-api-key"
$ terraform plan
```

<!-- schema generated by tfplugindocs -->

## Schema

### Required

- **token** (String) Your Zenduty API key

### Optional

- **base_url** (String) The base url of the Zenduty
