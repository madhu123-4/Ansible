# Scenario-based Ansible Interview Questions
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

### Install the Jenkins tool by using Ansible playbook.

Here's a modified and streamlined version of your playbook to install Jenkins using Ansible:

```yaml
---
- name: Install Jenkins using Ansible
  hosts: webservers
  become: true
  tasks:
    - name: Install Java
      yum:
        name: java-11-openjdk-devel
        state: present

    - name: Install wget
      yum:
        name: wget
        state: present

    - name: Download Jenkins Repo
      get_url:
        url: http://pkg.jenkins-ci.org/redhat/jenkins.repo
        dest: /etc/yum.repos.d/jenkins.repo

    - name: Add Jenkins repo key
      rpm_key:
        state: present
        key: http://pkg.jenkins-ci.org/redhat/jenkins-ci.org.key

    - name: Install Jenkins
      yum:
        name: Jenkins
        state: present

    - name: Reload systemd to pick up config changes
      systemd:
        daemon_reload: yes

    - name: Start and enable Jenkins service
      systemd:
        name: Jenkins
        state: started
        enabled: yes
```

This playbook performs the following actions:
1. Install Java and wget if not already installed.
2. Download the Jenkins repository configuration file and save it to `/etc/yum.repos.d/jenkins.repo`.
3. Adds the Jenkins repository key to the RPM database.
4. Install the Jenkins package using `yum`.
5. Reloads systemd to pick up any configuration changes.
6. Starts and enables the Jenkins service to ensure it starts on system boot.

Please note that you might need to adjust the URL for the Jenkins repository configuration file (`Jenkins.repo`) and the Jenkins repository key (`jenkins-ci.org.key`) based on the actual URLs provided by the Jenkins project.

### Write a cronjob to run every two minutes.

Here's an example Ansible playbook to create a cron job on a target server:

```yaml
---
- name: Create a cron job
  hosts: your_target_group
  become: yes
  tasks:
    - name: Add the cron job
      cron:
        name: "My Cron Job"
        minute: "0"
        hour: "*/2"
        job: "/path/to/your/command"
```

Replace `your_target_group` with the name of your host or group of hosts where you want to create the cron job. Modify the `name`, `minute`, `hour`, and `job` parameters according to your requirements. The `minute` and `hour` parameters specify when the cron job should run. In this example, the cron job runs every two hours.
### How to create 100 files at a time by using ansible-playbook with a specific name called madhu.txt

To create 100 files at a time with the specific name "madhu.txt" using Ansible, you can use a loop in your playbook. Here's an example playbook that achieves this:

```yaml
---
- name: Create 100 files with the name madhu.txt
  hosts: localhost
  gather_facts: no
  tasks:
    - name: Create files
      file:
        path: "/path/to/your/directory/madhu_{{ item }}.txt"
        state: touch
      loop: "{{ range(1, 101) | list }}"
```

Replace `/path/to/your/directory/` with the path to the directory where you want to create the files. This playbook uses the `file` module with the `state: touch` option to create 100 files named `madhu_1.txt`, `madhu_2.txt`, and so on, up to `madhu_100.txt` in the specified directory.

### how to create a git repository and clone the repository to git CLI  by using ansible playbook?
To create a Git repository and clone it to the Git CLI using an Ansible playbook, you can use the `git` module. Here's an example playbook that demonstrates this:

```yaml
---
- name: Create a Git repository and clone it
  hosts: localhost
  tasks:
    - name: Create a directory for the Git repository
      file:
        path: "/path/to/your/repository"
        state: directory

    - name: Initialize a Git repository
      git:
        repo: "https://github.com/example/repository.git"
        dest: "/path/to/your/repository"
        clone: yes

    - name: Clone the repository to the Git CLI
      git:
        repo: "/path/to/your/repository"
        dest: "/path/to/clone"
```

Replace `/path/to/your/repository` with the path where you want to create the Git repository and `/path/to/clone` with the path where you want to clone the repository on the local machine. Adjust the `repo` parameter to point to the URL of the Git repository you want to initialize and clone. 

### Question: If you are given a task to manage a new remote machine using Ansible, what is the first thing you would do?

Answer: The first thing to do is to add the new machine’s details in the Ansible inventory file. Then, set up SSH key-based authentication between the Ansible controller node and the new remote machine for secure communication.
### Question: How would you handle sensitive information like passwords in your Ansible Playbook?

Answer: Ansible provides a tool called ansible-vault to encrypt sensitive data. So, you can put all sensitive data inside a vault and reference it in the playbook.
### Question: If an Ansible playbook failed at a particular task, how would you debug it?

Answer: Ansible provides a --step and --start-at-task debugging option. We can use these options to start executing the playbook at the failed task and inspect what’s going wrong.
### Question: You have a common configuration that needs to be shared across multiple playbooks. How would you achieve this?

Answer: In Ansible, we can create a ‘roles’ for such cases. Roles are a way to group multiple tasks together into one container to do the automation in very effective manner.
### Question: How would you run a single task against all the development servers without writing a playbook?

Answer: Ansible provides ad-hoc commands that could be used to do quick tasks. An ad-hoc command looks like ansible <group> -m <module> -a <arguments>
### Question: You have some tasks that should only run on a specific type of OS. How can you manage this in your playbook?

Answer: Ansible gathers facts about the remote hosts and one such fact is the OS type. We can use conditionals (like the when clause) in our playbook to run certain tasks only when the OS type matches our requirements.
### Question: How can you manage different environments like Dev, QA, and Prod in Ansible?

Answer: This can be handled using Ansible inventory files. You can create separate inventory files for each environment, and specify the environment you want to run the playbook against when executing the ansible-playbook command.
### Question: How can you reduce playbook run time which is running against hundreds of machines?

Answer: We can increase the ‘forks’ in the ansible configuration file (ansible.cfg). This controls the number of parallel processes to be used for the playbook execution.
### Question: How can you ensure a task is only run when a file changes?

Answer: Ansible provides a ‘notify’ feature that can be used to trigger a handler only when a change is noticed on a system.
### Question: How can you create a new user across your entire server infrastructure?

Answer: Ansible provides a module called user for creating a user. We can write a simple playbook using the user module and run it against the server group defined in the inventory file.
### Question: How would you copy a file from the Ansible control machine to remote hosts?

Answer: You can use the copy module in Ansible to copy a file from the control machine to the remote hosts. The src parameter is used to specify the source file on the control machine and the dest parameter to specify the destination on the remote host.
### Question: How can you execute a command on a remote machine?

Answer: Ansible has several modules to execute commands on remote machines. For instance, command and shell modules can be used for this purpose. The key difference is that shell module executes the command through a shell /bin/sh on the remote node, allowing you to use shell features like shell pipes, etc.
### Question: How do you manage different software versions to be installed across your infrastructure?

Answer: This can be managed using Ansible variables. The software version can be defined as a variable in an Ansible playbook, and this variable can be altered according to the environment or requirements.
### Question: How would you perform a rolling update on your servers using Ansible?

Answer: Ansible provides a feature called ‘rolling update’ which can be used to update tasks on batch of hosts at a time using serial keyword.
### Question: How can you template a file in Ansible?

Answer: Ansible uses the Jinja2 templating engine to template files. The template module is used to create files on the remote hosts from templates on the control machine. Variables can be used in the templates and they will be replaced with their respective values when the task is executed.
### Question: If you have a task that needs to be run regularly, how would you automate this using Ansible?

Answer: While Ansible itself isn’t a scheduling tool, it integrates well with cron on Unix-like systems and the Scheduled Tasks feature on Windows. You can write a playbook for the task and then add a cron job or Scheduled Task to run the playbook at the desired intervals.
### Question: How can you run a playbook on a specific group of hosts?

Answer: In the Ansible playbook, there is a hosts field at the top where we can specify the group of hosts from our inventory on which we want to run the playbook.
### Question: How can you register the output of a command and use it in another task in Ansible?

Answer: Ansible provides a register keyword which can be used to store the output of a task. The registered value can then be used in subsequent tasks using Jinja2 templating.
### Question: How do you ensure idempotency in your Ansible playbooks?

Answer: Ansible modules are built to be idempotent, ensuring that repeated operations will always result in the same state and not change anything else. As long as you’re using Ansible modules, the idempotency should be handled automatically.
### Question: How can you gather facts about a remote host using Ansible?

Answer: Ansible has a setup module which is used to gather facts about remote hosts. It’s automatically included in plays, but you can also call it manually to get system facts.


### Scenario 1: Infrastructure Provisioning
Scenario: You’re tasked with provisioning a new set of web servers in a cloud environment to accommodate increased user traffic. Describe how you would use Ansible to automate the deployment process.

Answer: Using Ansible, I would create a playbook that defines tasks for provisioning virtual machines, configuring network settings, installing required software packages, and deploying web applications. I would utilize Ansible’s cloud modules to interact with the cloud provider’s API to dynamically create and manage instances. Playbooks would also include tasks for setting up security groups, firewall rules, and load balancers to ensure scalability and security.

### Scenario 2: Rolling Updates
Scenario: Your organization needs to perform rolling updates across multiple servers without causing service downtime. Explain how you would use Ansible to orchestrate the update process.

Answer: To perform rolling updates using Ansible, I would divide the servers into batches and execute playbook tasks sequentially on each batch. The playbook would include tasks for stopping services, applying updates, and restarting services on each server. Ansible’s serial and delegate_to directives can be used to control the order of execution and manage dependencies between tasks. By carefully orchestrating the update process, we can ensure continuous service availability during the rollout.

### Scenario 3: Security Compliance Checks
Scenario: Your organization needs to ensure compliance with security policies by regularly auditing server configurations and remediating any non-compliant settings. Describe how you would automate this process using Ansible.

Answer: I would create Ansible playbooks that include tasks for running security scanning tools, analyzing configuration files, and comparing settings against predefined security benchmarks. Ansible’s built-in modules like command, shell, and script can be used to execute security checks and gather system information. Playbooks would also include remediation tasks, such as updating configurations, applying patches, or installing security updates, to bring systems into compliance with security policies.

### Scenario 4: Application Deployment
Scenario: Your team is responsible for deploying a new version of a web application across multiple servers. Explain how you would use Ansible to automate the deployment process and ensure consistency across environments.

Answer: I would create Ansible playbooks that define tasks for deploying the web application, including copying application files, configuring web servers, updating database schemas, and restarting services. Playbooks would be parameterized to support different environments (e.g., development, staging, production) and include tasks for environment-specific configurations. By using Ansible’s idempotent tasks and role-based organization, we can ensure consistent and reliable deployment across all servers.

### Scenario 5: Disaster Recovery
Scenario: In the event of a disaster, your organization needs to quickly restore services and data on backup servers. Describe how you would use Ansible to automate the disaster recovery process and minimize downtime.

Answer: I would create Ansible playbooks that define tasks for provisioning backup servers, restoring data from backups, configuring network settings, and starting services. Ansible’s cloud modules can be used to dynamically create instances in the backup environment, while tasks for data restoration would leverage backup solutions or file transfer mechanisms. Playbooks would also include tasks for updating DNS records and rerouting traffic to the backup servers to minimize downtime and ensure service continuity.

### Scenario 6: Auto-scaling
Scenario: Your organization’s infrastructure needs to automatically scale up or down based on fluctuating demand to optimize resource utilization and maintain service availability. Explain how you would implement auto-scaling using Ansible.

Answer: I would create Ansible playbooks that define tasks for monitoring resource usage, scaling instances up or down based on predefined thresholds, and updating load balancer configurations dynamically. Ansible’s cloud modules and APIs can be used to interact with the cloud provider’s infrastructure to scale instances in response to demand. Playbooks would include tasks for automated scaling policies, alarm triggers, and instance provisioning to ensure seamless auto-scaling without manual intervention.

### Scenario 7: Configuration Drift Detection
Scenario: Your organization needs to detect and remediate configuration drift across a fleet of servers to ensure consistency and compliance with predefined standards. Describe how you would use Ansible to automate configuration drift detection and remediation.

Answer: I would create Ansible playbooks that define tasks for collecting configuration data from managed servers, comparing it against baseline configurations, and identifying discrepancies or drift. Ansible’s gather_facts module and custom scripts can be used to collect system information and configuration files from servers. Playbooks would include tasks for analyzing configuration differences, generating reports, and applying remediation steps to bring servers back into compliance with standards.

### Scenario 8: Multi-tier Application Deployment
Scenario: Your organization needs to deploy a multi-tier application consisting of web servers, application servers, and database servers across multiple environments. Explain how you would use Ansible to automate the deployment of the entire application stack.

Answer: I would create Ansible playbooks that define tasks for provisioning and configuring each component of the application stack, including web servers, application servers, and database servers. Playbooks would be organized into roles corresponding to each tier of the application and include tasks for dependency management, service orchestration, and environment-specific configurations. By using Ansible’s modular and role-based approach, we can automate the deployment of the entire application stack consistently across different environments.

### Scenario 9: Zero Downtime Deployment
Scenario: Your organization needs to deploy updates to a critical production system with zero downtime to ensure continuous service availability. Describe how you would use Ansible to orchestrate a zero downtime deployment.

Answer: To achieve zero downtime deployment using Ansible, I would implement a blue-green deployment strategy where a new version of the application is deployed alongside the existing version without interrupting service. Ansible playbooks would include tasks for provisioning duplicate infrastructure, deploying the new version of the application, and gradually redirecting traffic to the updated servers. By carefully managing the cutover process and monitoring application health, we can ensure seamless deployment with zero downtime.

### Scenario 10: Compliance Reporting
Scenario: Your organization needs to generate compliance reports detailing the configuration status of servers and adherence to security policies. Explain how you would use Ansible to automate compliance reporting.

Answer: I would create Ansible playbooks that define tasks for collecting configuration data, performing security checks, and generating compliance reports based on predefined standards or benchmarks. Ansible’s built-in modules like gather_facts, command, and template can be used to collect system information, execute security checks, and generate report templates. Playbooks would include tasks for analyzing configuration data, identifying security vulnerabilities, and producing detailed compliance reports for review and audit purposes.
