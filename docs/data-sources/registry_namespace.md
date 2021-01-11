---
page_title: "Scaleway: scaleway_registry_namespace"
description: |-
  Gets information about a registry namespace.
---

# scaleway_registry_namespace

Gets information about a registry namespace.

## Example Usage

```hcl
// Get info by namespace name
data "scaleway_registry_namespace" "my_namespace" {
  name = "my-namespace-name"
}

// Get info by namespace ID
data "scaleway_registry_namespace" "my_namespace" {
  namespace_id = "11111111-1111-1111-1111-111111111111"
}
```

## Argument Reference

- `name` - (Optional) The namespace name.
  Only one of `name` and `namespace_id` should be specified.

- `namespace_id` - (Optional) The namespace id.
  Only one of `name` and `namespace_id` should be specified.

- `region` - (Defaults to [provider](../index.md#region) `region`) The [region](../guides/regions_and_zones.md#regions) in which the namespace exists.

- `organization_id` - (Defaults to [provider](../index.md#organization_id) `organization_id`) The ID of the organization the namespace is associated with.

- `project_id` - (Defaults to [provider](../index.md#project_id) `project_id`) The ID of the project the namespace is associated with.

## Attributes Reference

In addition to all above arguments, the following attributes are exported:

- `id` - The ID of the Registry Namespace.
- `is_public` - The Namespace Privacy Policy: whether or not the images are public.
- `endpoint` - The endpoint of the Registry Namespace.
