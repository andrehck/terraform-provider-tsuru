---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "tsuru_app_env Resource - terraform-provider-tsuru"
subcategory: ""
description: |-
  Tsuru Application Environment
---

# tsuru_app_env (Resource)

Tsuru Application Environment

## Example Usage

```terraform
resource "tsuru_app_env" "env" {
  app               = tsuru_app.my-app.name
  restart_on_update = true

  environment_variables = {
    "ENV1" = "10"
    "ENV2" = "other value"
  }

  private_environment_variables = {
    "SECRET_ENV"  = data.google_secret_manager_secret_version.mysecret.secret_data
    "SECRET_ENV2" = data.myother-secret-manager.mysecret.value
  }
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- **app** (String) Application name

### Optional

- **environment_variables** (Map of String) Environment variables
- **id** (String) The ID of this resource.
- **private_environment_variables** (Map of String) Environment variables
- **restart_on_update** (Boolean) restart app after applying
- **timeouts** (Block, Optional) (see [below for nested schema](#nestedblock--timeouts))

<a id="nestedblock--timeouts"></a>
### Nested Schema for `timeouts`

Optional:

- **create** (String)
- **delete** (String)
- **update** (String)


