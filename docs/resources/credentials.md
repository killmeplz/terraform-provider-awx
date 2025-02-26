---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "awx_credentials Resource - awx"
subcategory: ""
description: |-
  Manages credentials in Ansible AWX/Tower. Credentials are utilized by Tower for authentication when launching jobs against machines, synchronizing with inventory sources, and importing project content from version control systems. Different credential types support different authentication methods (SSH keys, username/password, API tokens, etc.) depending on the service they connect to.
---

# awx_credentials (Resource)

Manages credentials in Ansible AWX/Tower. Credentials are utilized by Tower for authentication when launching jobs against machines, synchronizing with inventory sources, and importing project content from version control systems. Different credential types support different authentication methods (SSH keys, username/password, API tokens, etc.) depending on the service they connect to.



<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `credential_type` (String) The type of credential being created (e.g., SSH, AWS, GitHub, etc.). This determines what authentication fields are required in the inputs parameter.
- `inputs` (Map of String, Sensitive) A map of inputs required by the credential type. The specific inputs required depend on the credential_type. For example, an SSH credential might need 'username' and 'password' or 'ssh_key_data'.
- `name` (String) Name of this credential. Used to identify the credential in the AWX/Tower interface.

### Optional

- `description` (String) Optional description of this credential. Can be used to provide more context about the credential's purpose or usage.
- `organization` (String) The organization the credential belongs to. If provided, the credential will inherit permissions from organization roles. Cannot be specified together with user or team.

### Read-Only

- `id` (String) The ID of this resource.
