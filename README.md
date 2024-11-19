### cpp-ansible-role-xdr-install

An ansible playbook, built around ansible 2.3, for installing the Cortex XDR agent on RHEL7/CentOS7.

## Variables

Define the following variables in inventory at either the group or host level:

- cortex_env
- xdr_tags

cortex_env is a string which needs set to either 'nonprod' or 'prod'. MoJ SoC provided a separate installation package for nonprod & prod, this defines which installation package is used.

xdr_tags is a comma-separated string of tags to provide to the Cortex Agent.

Example:

```bash
xdr_tags: "hmcts,server,idam"
cortex_env: "nonprod"
```

An MS Team channel exists called "HMCTS - Tagging Catch Up" with the MoJ SoC team as members. Please reach out for help if unsure on tags on VMs.


### Other Role variables

Other variables are defaulted within the Role and do not need setting in automation.ansible repo inventory. 
The only exception to this is: 

- 'sa_key'

This should be set on the 'all' group and so it is usable by all hosts. This has been set in automation.ansible already which is the only place this Role is currently consumed.
