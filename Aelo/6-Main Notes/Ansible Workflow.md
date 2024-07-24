
2024-07-24 13:41

Status : #adult 

Tags : [[Ansible]]

# Ansible Workflow

1. **Inventory Parsing**: Ansible starts by parsing the inventory to determine which hosts it will manage.
    
2. **SSH Connection**: Ansible connects to managed nodes over SSH (or WinRM for Windows) using credentials provided in the inventory.
    
3. **Module Execution**: Ansible sends modules to managed nodes and executes them remotely. Modules are executed sequentially as defined in the playbook tasks.
    
4. **Gathering Facts**: Before executing tasks, Ansible gathers system information (facts) from managed nodes using the `gather_facts` module. These facts are then available as variables within playbooks.
    
5. **Task Execution**: Tasks defined in the playbook are executed in the order they are listed. Each task uses a specific module to perform actions such as installing packages, copying files, or restarting services.
    
6. **Reporting**: Ansible collects results from each task and reports back to the control node. It displays success or failure messages for each task executed.

# References
