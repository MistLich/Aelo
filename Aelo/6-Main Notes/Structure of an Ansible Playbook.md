
2024-07-24 13:57

Status : #adult 

Tags : [[Ansible Playbooks]]

# Structure of an Ansible Playbook

A playbook consists of one or more **plays**. Each play defines a set of tasks to be performed on a specific group of hosts. Here’s the basic structure:

```yaml
---
- name: Playbook Name
  hosts: group_name   # or specific_host or all (default is all)
  become: yes          # optional, enables privilege escalation (sudo)

  tasks:
    - name: Task 1
      <module_name>:
        <module_parameters>

    - name: Task 2
      <module_name>:
        <module_parameters>
        register: result_variable  # optional, stores result for later use

    - name: Task 3
      <module_name>:
        <module_parameters>
      when: condition           # optional, task conditionally executed

    - name: Task 4
      <module_name>:
        <module_parameters>
      notify: restart service   # optional, triggers handlers

  handlers:
    - name: restart service
      service:
        name: myservice
        state: restarted

  vars:
    var_name: value             # optional, defines variables

  environment:
    ENV_VAR: value              # optional, sets environment variables
```

### Explanation of Key Sections

1. **Header Section**:
   - `name`: A descriptive name for the playbook.
   - `hosts`: Specifies the group of hosts or specific hosts to execute tasks on.
   - `become`: (Optional) Enables privilege escalation (like `sudo`) if tasks require elevated permissions.

2. **Tasks Section**:
   - Contains a list of tasks to be executed sequentially.
   - Each task uses a module (`<module_name>`) to perform a specific action on the remote host.
   - Tasks can include parameters (`<module_parameters>`) specific to the module being used.
   - Tasks can register variables (`register: result_variable`) to store the result of the task for later use.
   - Tasks can be conditionally executed (`when: condition`) based on certain conditions.

3. **Handlers Section**:
   - Contains a list of tasks (handlers) that are triggered by specific events.
   - Handlers are typically used to restart services or perform other actions only when notified by tasks.
   - Handlers are defined separately from tasks and are executed at the end of a playbook run if triggered.

4. **Variables Section** (`vars`):
   - Defines variables (`var_name: value`) that can be used throughout the playbook.
   - Variables can be specific to the playbook or loaded from external files.

5. **Environment Section** (`environment`):
   - Sets environment variables (`ENV_VAR: value`) that are applied during playbook execution.
   - Useful for tasks requiring specific environment configurations.

# References