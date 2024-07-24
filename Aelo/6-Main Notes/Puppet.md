
2024-07-23 15:21

Status : #baby 

Tags : [[DevOps Tools]] [[CICD Tools]] 

# Puppet

Puppet is a configuration management tool similar to Ansible.

Master - Slave architecture ( connection is using SSL )

Facts - Node sends normalized data about itself to Master 
Catalog - Puppet uses facts to compile a catalog that specifies how the node should be configured
Report - the node reports back to puppet indicating the configuration is complete, which is visible in the Puppet dashboard


# References