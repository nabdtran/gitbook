# Cloud IAM

### Cloud IAM objects

* Organization
* Folders
* Projects
* Resources
* Roles
* Members

Policies are additive only. No deny rules.

![](../.gitbook/assets/image%20%282%29.png)

### Folders

Additional and optional grouping mechanism and isolation boundaries between projects.

### IAM role types

Primitive

Predefined

Custom

### Roles

Roles for service accounts can be assigned to groups or users

### Best Practices

* Use projects to group resources that share the same trust boundary
* Check the policy granted on each resource and understand inheritance
* Use principle of least privilege
* Audit policies in cloud audit logs
* Audit membership of groups used in policies
* Be careful with serviceAccountUser role
* Audit with serviceAccount.keys.list\(\)
* 
