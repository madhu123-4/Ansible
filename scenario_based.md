### 1)You have an ansible playbook that configures a server with a specific package. You want to run the playbook on a group of servers, but you want to skip the task that installs the package on a specific server. How would you do this?

You can achieve this by using Ansible's `when` condition to skip the task based on a condition. Here's an example:

```yaml
- name: Install package
  hosts: your_server_group
  tasks:
    - name: Install package
      package:
        name: your_package
        state: present
      when: inventory_hostname != 'specific_server'
```

In this example, replace `your_server_group` with the group of servers you want to configure and replace `specific_server` with the name of the server where you want to skip the package installation task. This condition (`when: inventory_hostname != 'specific_server'`) will skip the task when the playbook is run on the `specific_server` but will execute it on all other servers in the group.

### 2)You have an ansible playbook that installs and configures a web server. You want to run the playbook, but you want to test the changes before making them. How would you do this?

To test the changes made by an Ansible playbook without actually applying them, you can use the `--check` flag. This flag performs a dry run of the playbook, showing you what changes would be made without actually making them. Here's how you can use it:

```bash
ansible-playbook your_playbook.yml --check
```

Replace `your_playbook.yml` with the name of your playbook file. This command will show you the changes that would be made to the servers without applying them.

### 3. You have an ansible playbook that installs and configures a database server. You want to run the playbook, but you want to make it so that any failures will be ignored, and the playbook will continue to run. How would you do this?


To make an Ansible playbook continue running even if there are failures, you can use the `ignore_errors` attribute for the specific task or use the `ignore_unreachable` option for the entire playbook. Here's how you can do it:

1. **Using `ignore_errors` for a specific task:**

   ```yaml
   - name: Install database server
     hosts: your_server_group
     tasks:
       - name: Install database server
         command: /path/to/install_script.sh
         ignore_errors: yes
   ```

   In this example, the `ignore_errors: yes` attribute will make Ansible ignore any errors that occur during the execution of the `command` task.

2. **Using `ignore_unreachable` for the entire playbook:**

   ```yaml
   - name: Install database server
     hosts: your_server_group
     ignore_unreachable: yes
     tasks:
       - name: Install database server
         command: /path/to/install_script.sh
   ```

   In this example, the `ignore_unreachable: yes` option at the playbook level will make Ansible ignore any unreachable hosts and continue running the playbook on the remaining hosts.

Choose the method that best suits your requirements based on whether you want to ignore errors for specific tasks or for the entire playbook.

### 4. You have an ansible playbook that installs and configures a load balancer. You want to run the playbook, but you want to make it so that any tasks that would change the target hosts will be skipped. How would you do this?

To run an Ansible playbook and skip any tasks that would change the target hosts, you can use the `--check` flag along with the `--diff` flag. The `--check` flag tells Ansible to run in "check mode," where no changes are made to the target hosts, but the playbook shows what changes would have been made. The `--diff` flag shows the differences between the current configuration and the changes that would have been made.

Here's an example command:

```bash
ansible-playbook playbook.yml --check --diff
```

Replace `playbook.yml` with the path to your playbook file. This command will run the playbook in check mode, skipping any tasks that would change the target hosts, and display the differences.

### 5. You have an ansible playbook that installs and configures a monitoring system. You want to run the playbook, but you want to make it so that any tasks that are not idempotent (i.e., tasks that cannot be run multiple times without causing harm) will be skipped. How would you do this?

To run an Ansible playbook and skip any tasks that are not idempotent, you can use the `--check` flag along with the `--diff` flag. This combination will allow you to see which tasks would be executed without actually making any changes to the target hosts.

However, identifying which tasks are not idempotent requires understanding the tasks themselves and their impact on the target hosts. Ansible provides idempotence for many modules, but certain tasks, especially those involving system state changes or complex conditional logic, may not be fully idempotent.

Here's an example command:

```bash
ansible-playbook playbook.yml --check --diff
```

Replace `playbook.yml` with the path to your playbook file. This command will run the playbook in check mode, skipping any tasks that would not be idempotent, and display the differences.


### 6. You have an ansible playbook that installs and configures a file server. You want to run the playbook, but you want to make it so that any tasks that are not relevant to the target hosts will be skipped. How would you do this?

To run an Ansible playbook and skip tasks that are not relevant to the target hosts, you can use the `--limit` flag to specify which hosts to apply the playbook to. By limiting the playbook execution to specific hosts, Ansible will skip tasks that are not relevant to those hosts.

Here's an example command:

```bash
ansible-playbook playbook.yml --limit "your_target_group"
```

Replace `playbook.yml` with the path to your playbook file, and `"your_target_group"` with the name of the group or host you want to apply the playbook to. This command will run the playbook, skipping tasks that are not relevant to the specified target hosts.

### 7. You want to run a shell command on all of the servers in your inventory. How would you do this using ansible?

To run a shell command on all servers in your Ansible inventory, you can use the `ansible` command with the `--module-name` and `--args` options to specify the shell module and the command to run. Here's an example:

```bash
ansible all -m shell -a "your_shell_command_here"
```

Replace `"your_shell_command_here"` with the shell command you want to run. This command will execute the specified shell command on all servers in your inventory.

### 8. You want to copy a file from your local machine to all of the servers in your inventory. How would you do this using ansible?

To copy a file from your local machine to all servers in your Ansible inventory, you can use the `ansible` command with the `--module-name` and `--args` options to specify the copy module and the source and destination files. Here's an example:

```bash
ansible all -m copy -a "src=/path/to/local/file.txt dest=/path/on/server/file.txt"
```

Replace `/path/to/local/file.txt` with the path to the file on your local machine that you want to copy, and `/path/on/server/file.txt` with the path on the servers where you want to copy the file. This command will copy the specified file to all servers in your inventory.


### 9. You want to install a package on all of the servers in your inventory using the package manager for the target operating system. How would you do this using ansible?

To install a package on all servers in your Ansible inventory using the package manager for the target operating system, you can use the `ansible` command with the `--module-name` and `--args` options to specify the appropriate package module and the name of the package to install. Ansible will use the package manager relevant to each target operating system. Here's an example:

```bash
ansible all -m package -a "name=package_name state=present"
```

Replace `package_name` with the name of the package you want to install. This command will install the specified package on all servers in your inventory using the appropriate package manager for each operating system.


### 10. You want to create a user on all of the servers in your inventory. How would you do this using ansible?

To create a user on all servers in your Ansible inventory, you can use the `ansible` command with the `--module-name` and `--args` options to specify the user module and the user details. Here's an example:

```bash
ansible all -m user -a "name=new_user state=present"
```

Replace `new_user` with the username you want to create. This command will create the specified user on all servers in your inventory.
