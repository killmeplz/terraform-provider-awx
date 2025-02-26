---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "awx_project Resource - awx"
subcategory: ""
description: |-
  Manages an Ansible AWX/Tower project. A project is a logical collection of Ansible playbooks, represented in Tower. You can manage playbooks and playbook directories by either placing them manually under the Project Base Path on your Tower server, or by placing your playbooks into a source code management (SCM) system supported by Tower, including Git, Subversion, and Mercurial.
---

# awx_project (Resource)

Manages an Ansible AWX/Tower project. A project is a logical collection of Ansible playbooks, represented in Tower. You can manage playbooks and playbook directories by either placing them manually under the Project Base Path on your Tower server, or by placing your playbooks into a source code management (SCM) system supported by Tower, including Git, Subversion, and Mercurial.



<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `name` (String) Name of this project. Used to identify the project in the AWX/Tower interface.

### Optional

- `allow_override` (Boolean) If enabled, users can override the SCM branch or revision in job templates that use this project.
- `credential_id` (String) The ID of the credential to use for authenticating with the SCM system.
- `description` (String) Optional description of this project. Can be used to provide more context about the project's purpose.
- `local_path` (String) The local path (relative to PROJECTS_ROOT) on the AWX/Tower server where playbooks are stored. Used when scm_type is set to 'manual'.
- `organization` (Number) The organization the project belongs to. Projects must be associated with an organization for role-based access control.
- `scm_branch` (String) The branch, tag, or commit to checkout from the SCM system. Default is the default branch of the SCM repository.
- `scm_clean` (Boolean) If enabled, the project directory will be cleared before each update, removing any untracked files.
- `scm_delete_on_update` (Boolean) If enabled, the project directory will be deleted and recreated with each project update.
- `scm_refspec` (String) For git projects, an additional refspec to fetch. Can be used to retrieve additional branches or pull requests.
- `scm_track_submodules` (Boolean) If enabled, git submodules will be tracked and updated when the project is updated.
- `scm_type` (String) Type of source control management system. Valid options include: 'manual', 'git', 'svn', 'hg', and others as supported by AWX/Tower.
- `scm_update_on_launch` (Boolean) If enabled, the project will update from its SCM source before each job using this project is run.
- `scm_url` (String) The source control URL for the project. Required when scm_type is set to a valid SCM system.

### Read-Only

- `id` (String) The ID of this resource.
