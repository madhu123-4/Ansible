#### 1. _________________ is something that is used for streamlining the development and deployment process.

A. Continuous Delivery
B. Continuous Integration
C. Continuous Test
D. Continuous Intervention
View Answer

#### Ans: B |Explanation: Continuous Integration is something that is used for streamlining the development and deployment process. These lead to the more rapid development of cohesive software.


2. _____________ is a combination of multiple pieces working together to become an automation tool.

A. Bugzilla
B. Chef
C. Ansible
D. Git
View Answer

Ans : C
Explanation: Ansible is a combination of multiple pieces working together to become an automation tool. Mainly these are modules, playbooks, and plugins.


3. What are the features of Ansible?

A. Unlike puppet or chef there is no software or agent managing the nodes
B. Passwordless network authentication which makes it more secure and easy to set up
C. The core concept is to push multiple small codes to the configure and run the action on client nodes
D. All of the above
View Answer

Ans : D
Explanation: All of the above are the features of Ansible.


4. IaC stands for?

A. Integration as Code
B. Infra as Code
C. Infrastructure Ansible Code
D. Infrastructure as Code
View Answer

Ans : D
Explanation: Infrastructure as Code or IaC is a process that DevOps teams should follow to have a more organized way of managing the infra.


5. ___________ is a repository of Ansible roles that can be shared among users and can be directly dropped into playbooks for execution.

A. Modules
B. Functions
C. Galaxy
D. Standalone
View Answer

Ans : C
Explanation: Galaxy is a repository of Ansible roles that can be shared among users and can be directly dropped into playbooks for execution. It is also used for the distribution of packages containing roles, plugins, and modules also known as collection. The ansible-galaxy-collection command implements similar to init, build, install, etc like an ansible-galaxy command.



6. How many types of modules in Ansible?

A. 1
B. 2
C. 3
D. 4
View Answer

Ans : B
Explanation: There are 2 types of modules in Ansible: Core Modules and Extras Modules.


7. YAML or files are like any formatted text file with few sets of rules just like JSON or XML.

A. TRUE
B. FALSE
C. Can be true or false
D. Can not say
View Answer

Ans : A
Explanation: YAML or files are like any formatted text file with few sets of rules just like JSON or XML. Ansible uses this syntax for playbooks as it is more readable than other formats.


8. In Which Language Ansible engine written?

A. C
B. C++
C. Java
D. Python
View Answer

Ans : D
Explanation: In python Language Ansible engine written


9. What language are Ansible playbooks written in by default ?

A. XML
B. HTML
C. JSON
D. YAML
View Answer

Ans : D
Explanation: YAML language is an Ansible playbooks are written in by default.


10. The task is a unit action of Ansible.

A. Yes
B. No
C. Can be yes or no
D. Can not say
View Answer

Ans : A
Explanation: Yes, The task is a unit action of Ansible

1. What is Ansible?

a) A tool for configuration management
b) A tool for containerization
c) A programming language
d) A database management tool

Answer: a) A tool for configuration management

Explanation: Ansible is an open-source tool that provides automation for configuration management, application deployment, and task automation. It simplifies the IT infrastructure management by automating the repetitive tasks.

2. Ansible is written in which language?

a) Ruby
b) Python
c) Perl
d) Java

Answer: b) Python

Explanation: Ansible is written in Python language. Python is a high-level programming language that is easy to read and write, making it a popular choice for automation tools.

3. What is the purpose of the Ansible playbook?

a) To install the Ansible tool
b) To write Python code for automation
c) To define the configuration and deployment steps
d) To manage the Docker containers


Answer: c) To define the configuration and deployment steps



Explanation: Ansible playbook is used to define the configuration and deployment steps required to automate the process. It is a YAML file that contains a list of tasks to be executed on the target host.

4. What is an Ansible module?

a) A collection of tasks
b) A pre-defined set of variables
c) A function that performs a specific task
d) A script that runs on the target host

Answer: c) A function that performs a specific task

Explanation: An Ansible module is a function that performs a specific task, such as copying files, managing packages, or configuring services. Ansible has a large number of built-in modules that can be used in playbooks.

5. How does Ansible communicate with the target hosts?

a) SSH
b) Telnet
c) RDP
d) VNC

Answer: a) SSH

Explanation: Ansible communicates with the target hosts over SSH. SSH is a secure protocol that provides encryption and authentication.

6. What is an Ansible inventory file?

a) A file that contains the list of target hosts
b) A file that defines the playbook steps
c) A file that contains the variables
d) A file that contains the module definitions

Answer: a) A file that contains the list of target hosts



Explanation: An Ansible inventory file is a file that contains the list of target hosts that Ansible will manage. It is a simple text file that can be structured in various ways.

7. What is the default location of the Ansible inventory file?

a) /etc/ansible/hosts
b) /etc/ansible/inventory
c) /etc/ansible/hosts.ini
d) /etc/ansible/inventory.ini

Answer: a) /etc/ansible/hosts

Explanation: The default location of the Ansible inventory file is /etc/ansible/hosts. This can be changed by setting the inventory variable in the ansible.cfg file.

8. What is the difference between Ansible and Puppet?

a) Ansible is written in Python, while Puppet is written in Ruby
b) Ansible uses push-based configuration management, while Puppet uses pull-based configuration management
c) Ansible has a smaller learning curve, while Puppet has a steeper learning curve
d) All of the above

Answer: d) All of the above

Explanation: Ansible and Puppet are both configuration management tools, but there are some differences between them. Ansible is written in Python, uses push-based configuration management, and has a smaller learning curve. Puppet is written in Ruby, uses pull-based configuration management, and has a steeper learning curve.

9. What is the purpose of the Ansible ad-hoc command?

a) To execute a single task on the target hosts
b) To run a playbook on the target hosts
c) To create a new module for Ansible
d) To generate a report of the host inventory

Answer: a) To execute a single task on the target hosts

Explanation: The Ansible ad-hoc command is used to execute a single task on the target hosts without using a playbook. It is useful for quick, one-off tasks.

10. What is the difference between Ansible and Chef?

a) Ansible is written in Python, while Chef is written in Ruby
b) Ansible uses push-based configuration management, while Chef uses pull-based configuration management
c) Ansible has a smaller learning curve, while Chef has a steeper learning curve
d) All of the above

Answer: d) All of the above

Explanation: Ansible and Chef are both configuration management tools, but there are some differences between them. Ansible is written in Python, uses push-based configuration management, and has a smaller learning curve. Chef is written in Ruby, uses pull-based configuration management, and has a steeper learning curve.

11. What is the purpose of the Ansible Vault?

a) To store the playbook files
b) To store the inventory file
c) To store the sensitive data, such as passwords and keys
d) To store the log files

Answer: c) To store the sensitive data, such as passwords and keys

Explanation: Ansible Vault is a feature that allows users to encrypt sensitive data, such as passwords and keys, within Ansible playbooks and inventory files. This ensures that the data is stored securely.

12. How can you encrypt a file using Ansible Vault?

a) ansible-vault encrypt filename
b) ansible encrypt-vault filename
c) ansible-vault encrypt –file filename
d) ansible-encrypt filename

Answer: a) ansible-vault encrypt filename

Explanation: To encrypt a file using Ansible Vault, you can use the ansible-vault encrypt filename command. This will encrypt the file and prompt you for a password.

13. What is the purpose of the Ansible Galaxy?

a) To store the playbook files
b) To store the inventory file
c) To store the roles and collections
d) To store the sensitive data

Answer: c) To store the roles and collections

Explanation: Ansible Galaxy is a hub for sharing Ansible roles and collections. It provides a central location for users to find and share reusable Ansible content.

14. What is an Ansible role?

a) A set of tasks that can be reused across playbooks
b) A collection of modules that perform a specific task
c) A predefined set of variables that can be used in playbooks
d) A script that runs on the target host

Answer: a) A set of tasks that can be reused across playbooks

Explanation: An Ansible role is a set of tasks, files, templates, and variables that can be reused across playbooks. Roles can be shared and reused, making them a powerful tool for managing infrastructure.

15. How can you create an Ansible role?

a) ansible-galaxy init rolename
b) ansible-role init rolename
c) ansible-init role rolename
d) ansible create-role rolename

Answer: a) ansible-galaxy init rolename

Explanation: To create an Ansible role, you can use the ansible-galaxy init rolename command. This will create a new directory structure and files for the role.

16. What is an Ansible collection?

a) A set of roles that can be reused across playbooks
b) A collection of modules that perform a specific task
c) A set of plugins that extend Ansible functionality
d) A predefined set of variables that can be used in playbooks

Answer: c) A set of plugins that extend Ansible functionality

Explanation: An Ansible collection is a curated set of plugins, modules, roles, and other content that extends the functionality of Ansible. Collections can be installed and shared, making them a powerful tool for managing infrastructure.

17. How can you install an Ansible collection?

a) ansible-galaxy install collectionname
b) ansible install-collection collectionname
c) ansible-collection install collectionname
d) ansible install collection collectionname

Answer: a) ansible-galaxy install collectionname

Explanation: To install an Ansible collection, you can use the ansible-galaxy install collectionname command. This will download and install the collection from Ansible Galaxy.

18. What is the purpose of the Ansible Tower?

a) To store the playbook files
b) To store the inventory file
c) To provide a web-based interface for managing Ansible
d) To provide a repository for Ansible roles and collections

Answer: c) To provide a web-based interface for managing Ansible

Explanation: Ansible Tower is a web-based interface for managing Ansible. It provides a central location for managing inventory, creating and scheduling playbooks, and monitoring infrastructure.

19. What is the purpose of the Ansible Config file?

a) To store the playbook files
b) To store the inventory file
c) To configure the behavior of Ansible
d) To store the sensitive data

Answer: c) To configure the behavior of Ansible

Explanation: The Ansible Config file is used to configure the behavior of Ansible. It can be used to specify options such as the location of the inventory file, the default user for SSH connections, and other settings.

20. How can you specify the location of the inventory file in the Ansible Config file?

a) inventory = /path/to/inventory
b) inventory_file = /path/to/inventory
c) inventory_path = /path/to/inventory
d) inventory-location = /path/to/inventory

Answer: b) inventory_file = /path/to/inventory

Explanation: To specify the location of the inventory file in the Ansible Config file, you can use the inventory_file option. The value should be the full path to the inventory file.

21. How can you execute an Ansible playbook?

a) ansible-playbook playbook.yml
b) ansible-play playbook.yml
c) ansible playbook.yml
d) ansible-execute playbook.yml

Answer: a) ansible-playbook playbook.yml

Explanation: To execute an Ansible playbook, you can use the ansible-playbook command followed by the name of the playbook file.

22. What is the purpose of the Ansible Handler?

a) To store the inventory file
b) To store the sensitive data
c) To define a set of tasks that are executed only if a specific condition is met
d) To define a set of tasks that are executed at the end of a playbook run

Answer: d) To define a set of tasks that are executed at the end of a playbook run

Explanation: An Ansible Handler is a special type of task that is defined in a playbook and is executed at the end of a playbook run. Handlers are typically used to restart services or perform other actions that need to be triggered only after a change has been made to the system.

23. What is the purpose of the Ansible Role?

a) To store the playbook files
b) To store the inventory file
c) To define a set of tasks, files, templates, and other content that can be reused across playbooks
d) To store the sensitive data

Answer: c) To define a set of tasks, files, templates, and other content that can be reused across playbooks

Explanation: An Ansible Role is a collection of tasks, files, templates, and other content that can be reused across playbooks. Roles can be shared and installed like collections, making them a powerful tool for managing infrastructure.

24. How can you create a new Ansible role?

a) ansible-galaxy init rolename
b) ansible role init rolename
c) ansible-create role rolename
d) ansible-galaxy create rolename

Answer: a) ansible-galaxy init rolename

Explanation: To create a new Ansible role, you can use the ansible-galaxy init rolename command. This will create a new directory structure for the role and provide some basic content.

25. How can you decrypt a file encrypted with Ansible Vault?

a) ansible-vault decrypt filename
b) ansible decrypt filename
c) ansible-file decrypt filename
d) ansible-galaxy decrypt filename

Answer: a) ansible-vault decrypt filename

Explanation: To decrypt a file encrypted with Ansible Vault, you can use the ansible-vault decrypt filename command. This will prompt you for the password used to encrypt the file.

26. What is the purpose of the Ansible Tower API?

a) To provide a web-based interface for managing Ansible
b) To provide a way to automate and integrate with Ansible Tower
c) To provide a way to install and share Ansible collections
d) To provide a way to encrypt sensitive data using Ansible Vault

Answer: b) To provide a way to automate and integrate with Ansible Tower

Explanation: The Ansible Tower API provides a way to automate and integrate with Ansible Tower. It can be used to perform tasks such as launching jobs, managing inventory, and retrieving job results.

27. How can you authenticate with the Ansible Tower API?

a) By providing a username and password
b) By providing an API token
c) By providing a private SSH key
d) By providing a GPG key

Answer: b) By providing an API token

Explanation: To authenticate with the Ansible Tower API, you need to provide an API token.

28. What is the purpose of the Ansible playbook keyword “become”?

a) To switch to a different inventory group
b) To switch to a different playbook
c) To switch to a different user or privilege level on the target system
d) To switch to a different playbook directory

Answer: c) To switch to a different user or privilege level on the target system

Explanation: The Ansible playbook keyword “become” is used to switch to a different user or privilege level on the target system. This is useful when you need to run tasks as a different user or escalate privileges to perform certain actions.

29. How can you use the “when” keyword in an Ansible playbook?

a) To define the name of the playbook
b) To define the hosts to run the playbook on
c) To conditionally run tasks based on certain criteria
d) To define variables for use in the playbook

Answer: c) To conditionally run tasks based on certain criteria

Explanation: The “when” keyword in an Ansible playbook is used to conditionally run tasks based on certain criteria, such as the value of a variable or the state of a system.

30. What is the purpose of the Ansible module “copy”?

a) To copy files or directories to the target system
b) To create a new file on the target system
c) To delete files or directories from the target system
d) To edit an existing file on the target system

Answer: a) To copy files or directories to the target system

Explanation: The Ansible module “copy” is used to copy files or directories to the target system.

31. How can you use the Ansible module “file” to set permissions on a file?

a) By using the “mode” parameter
b) By using the “owner” parameter
c) By using the “group” parameter
d) By using the “state” parameter

Answer: a) By using the “mode” parameter

Explanation: The Ansible module “file” can be used to set permissions on a file by using the “mode” parameter.

32. What is the purpose of the Ansible module “lineinfile”?

a) To search for a line in a file and replace it with a new line
b) To add a new line to the end of a file
c) To remove a line from a file
d) To create a new file with a single line of text

Answer: a) To search for a line in a file and replace it with a new line

Explanation: The Ansible module “lineinfile” is used to search for a line in a file and replace it with a new line.

33. How can you use the Ansible module “service” to restart a service?

a) By using the “state” parameter with a value of “restarted”
b) By using the “state” parameter with a value of “running”
c) By using the “state” parameter with a value of “stopped”
d) By using the “state” parameter with a value of “reloaded”

Answer: a) By using the “state” parameter with a value of “restarted”

Explanation: The Ansible module “service” can be used to restart a service by using the “state” parameter with a value of “restarted”.

34. What is the purpose of the Ansible module “apt”?

a) To manage packages on a target system using the APT package manager
b) To manage users and groups on a target system
c) To manage files and directories on a target system
d) To manage services on a target system

Answer: a) To manage packages on a target system using the APT package manager

Explanation: The Ansible module “apt” is used to manage packages on a target system using the APT package manager.

35. How can you use the Ansible module “template” to create a new file on a target system?

a) By providing the content of the file as a parameter to the module
b) By providing a Jinja2 template and variables to fill in the template
c) By copying an existing file to the target system and modifying it
d) By creating the file manually on the target system

Answer: b) By providing a Jinja2 template and variables to fill in the template

Explanation: The Ansible module “template” can be used to create a new file on a target system by providing a Jinja2 template and variables to fill in the template.

36. How can you use the Ansible module “debug” to display the value of a variable?

a) By providing the name of the variable as a parameter to the module
b) By providing a message and the name of the variable as parameters to the module
c) By using the “var” parameter with the name of the variable
d) By using the “msg” parameter with the name of the variable

Answer: c) By using the “var” parameter with the name of the variable

Explanation: The Ansible module “debug” can be used to display the value of a variable by using the “var” parameter with the name of the variable.

37. What is the purpose of the Ansible module “fail”?

a) To intentionally fail a task in an Ansible playbook
b) To provide a message to the user and continue with the playbook
c) To skip a task in an Ansible playbook
d) To retry a task in an Ansible playbook

Answer: a) To intentionally fail a task in an Ansible playbook

Explanation: The Ansible module “fail” is used to intentionally fail a task in an Ansible playbook.

38. How can you use the Ansible module “set_fact” to create a new variable?

a) By providing the name and value of the variable as parameters to the module
b) By using a Jinja2 template to calculate the value of the variable
c) By copying an existing variable to create a new one
d) By using the “var” parameter to set the value of the variable

Answer: a) By providing the name and value of the variable as parameters to the module

Explanation: The Ansible module “set_fact” can be used to create a new variable by providing the name and value of the variable as parameters to the module.

39. How can you use the Ansible module “uri” to make an HTTP request?

a) By providing the URL as a parameter to the module
b) By using the “method” parameter to specify the HTTP verb, and the “url” parameter to specify the URL
c) By using the “header” parameter to specify the HTTP headers
d) By using the “data” parameter to specify the request body

Answer: b) By using the “method” parameter to specify the HTTP verb, and the “url” parameter to specify the URL

Explanation: The Ansible module “uri” can be used to make an HTTP request by using the “method” parameter to specify the HTTP verb and the “url” parameter to specify the URL.

40. What is the purpose of the Ansible module “wait_for”?

a) To wait for a specific amount of time before continuing with the playbook
b) To wait for a condition to be true before continuing with the playbook
c) To wait for a user input before continuing with the playbook
d) To wait for a specific event to occur before continuing with the playbook

Answer: b) To wait for a condition to be true before continuing with the playbook

Explanation: The Ansible module “wait_for” is used to wait for a condition to be true before continuing with the playbook.

41. How can you use the Ansible module “lineinfile” to add a new line to a file?

a) By providing the contents of the file as a parameter to the module, along with the new line to add
b) By using a Jinja2 template to generate the contents of the file, including the new line
c) By using the “line” parameter to specify the new line to add, and the “path” parameter to specify the path to the file
d) By using the “regexp” parameter to specify the pattern to match, and the “line” parameter to specify the new line to add

Answer: d) By using the “regexp” parameter to specify the pattern to match, and the “line” parameter to specify the new line to add

Explanation: The Ansible module “lineinfile” can be used to add a new line to a file by using the “regexp” parameter to specify the pattern to match and the “line” parameter to specify the new line to add.

42. How can you use the Ansible module “service” to start a service on a target system?

a) By providing the name of the service as a parameter to the module
b) By using the “state” parameter with the value “started”
c) By using the “action” parameter with the value “start”
d) By using the “service” parameter with the value “start”

Answer: b) By using the “state” parameter with the value “started”

Explanation: The Ansible module “service” can be used to start a service on a target system by using the “state” parameter with the value “started”.

43. What is the purpose of the Ansible module “setup”?

a) To set up a new target system with the necessary software and configurations
b) To gather facts about a target system, such as hardware and software information
c) To automate the deployment of software to a target system
d) To configure network settings on a target system

Answer: b) To gather facts about a target system, such as hardware and software information

Explanation: The Ansible module “setup” is used to gather facts about a target system, such as hardware and software information.

44. How can you use the Ansible module “assert” to test a condition in an Ansible playbook?

a) By providing the condition as a parameter to the module
b) By using a Jinja2 template to generate the condition dynamically
c) By using the “msg” parameter to provide a message to display if the condition fails
d) By using the “success_msg” parameter to provide a message to display if the condition is true

Answer: a) By providing the condition as a parameter to the module

Explanation: The Ansible module “assert” can be used to test a condition in an Ansible playbook by providing the condition as a parameter to the module.

45. How can you use the Ansible module “copy” to copy a file to a target system?

a) By providing the contents of the file as a parameter to the module, along with the path to copy the file to
b) By using a Jinja2 template to generate the contents of the file, including the path to copy the file to
c) By using the “src” parameter to specify the path to the file on the control node, and the “dest” parameter to specify the path to copy the file to on the target system
d) By using the “path” parameter to specify the path to the file on the control node, and the “copy_to” parameter to specify the path to copy the file to on the target system

Answer: c) By using the “src” parameter to specify the path to the file on the control node, and the “dest” parameter to specify the path to copy the file to on the target system

Explanation: The Ansible module “copy” can be used to copy a file to a target system by using the “src” parameter to specify the path to the file on the control node and the “dest” parameter to specify the path to copy the file to on the target system.

46. How can you use the Ansible module “file” to create a directory on a target system?

a) By using the “mode” parameter to specify the permissions for the directory
b) By using the “state” parameter with the value “directory”
c) By using the “directory” parameter with the value “create”
d) By using the “path” parameter to specify the path to the directory

Answer: b) By using the “state” parameter with the value “directory”

Explanation: The Ansible module “file” can be used to create a directory on a target system by using the “state” parameter with the value “directory”.

47. How can you use the Ansible module “lineinfile” to remove a line from a file?

a) By providing the contents of the file as a parameter to the module, with the line to remove omitted
b) By using a Jinja2 template to generate the contents of the file, with the line to remove omitted
c) By using the “line” parameter to specify the line to remove, and the “path” parameter to specify the path to the file
d) By using the “regexp” parameter to specify the pattern to match, and the “state” parameter with the value “absent”

Answer: d) By using the “regexp” parameter to specify the pattern to match, and the “state” parameter with the value “absent”

Explanation: The Ansible module “lineinfile” can be used to remove a line from a file by using the “regexp” parameter to specify the pattern to match and the “state” parameter with the value “absent”.

48. How can you use the Ansible module “yum” to install a package on a target system?

a) By using the “package” parameter to specify the name of the package to install
b) By using the “name” parameter to specify the name of the package to install
c) By using the “action” parameter with the value “install”
d) By using the “state” parameter with the value “installed”

Answer: b) By using the “name” parameter to specify the name of the package to install

Explanation: The Ansible module “yum” can be used to install a package on a target system by using the “name” parameter to specify the name of the package to install.

49. How can you use the Ansible module “apt” to install a package on a target system?

a) By using the “package” parameter to specify the name of the package to install
b) By using the “name” parameter to specify the name of the package to install
c) By using the “action” parameter with the value “install”
d) By using the “state” parameter with the value “installed”

Answer: b) By using the “name” parameter to specify the name of the package to install

Explanation: The Ansible module “apt” can be used to install a package on a target system by using the “name” parameter to specify the name of the package to install.

50. How can you use the Ansible module “cron” to remove a cron job from a target system?

a) By using the “name” parameter to specify the name of the cron job to remove
b) By using the “state” parameter with the value “absent”
c) By using the “job” parameter with the value “remove”
d) By using the “cron” parameter with the value “remove”

Answer: b) By using the “state” parameter with the value “absent”

Explanation: The Ansible module “cron” can be used to remove a cron job from a target system by using the “state” parameter with the value “absent”.

51. How can you use the Ansible module “debug” to display a variable’s value during a playbook run?

a) By using the “msg” parameter to specify the variable’s name
b) By using the “var” parameter to specify the variable’s name
c) By using the “value” parameter to specify the variable’s name
d) By using the “debug” parameter with the value “true” and the variable’s name as the parameter value

Answer: b) By using the “var” parameter to specify the variable’s name

Explanation: The Ansible module “debug” can be used to display a variable’s value during a playbook run by using the “var” parameter to specify the variable’s name.

52. How can you use the Ansible module “uri” to send a POST request to a web service?

a) By using the “method” parameter with the value “POST” and the “url” parameter to specify the URL of the web service
b) By using the “url” parameter to specify the URL of the web service and the “data” parameter to specify the data to be sent in the POST request
c) By using the “body” parameter to specify the data to be sent in the POST request and the “URL” parameter to specify the URL of the web service
d) By using the “request” parameter with the value “POST” and the “url” parameter to specify the URL of the web service

Answer: b) By using the “url” parameter to specify the URL of the web service and the “data” parameter to specify the data to be sent in the POST request

Explanation: The Ansible module “uri” can be used to send a POST request to a web service by using the “url” parameter to specify the URL of the web service and the “data” parameter to specify the data to be sent in the POST request.

53. How can you use the Ansible module “copy” to copy a file from the control machine to a target machine?

a) By using the “src” parameter to specify the source file and the “dest” parameter to specify the destination file
b) By using the “file” parameter to specify the source file and the “to” parameter to specify the destination file
c) By using the “from” parameter to specify the source file and the “to” parameter to specify the destination file
d) By using the “source” parameter to specify the source file and the “destination” parameter to specify the destination file

Answer: a) By using the “src” parameter to specify the source file and the “dest” parameter to specify the destination file

Explanation: The Ansible module “copy” can be used to copy a file from the control machine to a target machine by using the “src” parameter to specify the source file and the “dest” parameter to specify the destination file.

54. How can you use the Ansible module “file” to change the owner and group of a file on a target machine?

a) By using the “owner” and “group” parameters to specify the new owner and group
b) By using the “chown” parameter to specify the new owner and group in the format “user:group”
c) By using the “set_owner” and “set_group” parameters to specify the new owner and group
d) By using the “user” and “group” parameters to specify the new owner and group

Answer: b) By using the “chown” parameter to specify the new owner and group in the format “user:group”

Explanation: The Ansible module “file” can be used to change the owner and group of a file on a target machine by using the “chown” parameter to specify the new owner and group in the format “user:group”.

55. How can you use the Ansible module “lineinfile” to add a line to a file on a target machine?

a) By using the “line” parameter to specify the line to add and the “path” parameter to specify the path to the file
b) By using the “add” parameter to specify the line to add and the “file” parameter to specify the path to the file
c) By using the “insert” parameter to specify the line to add and the “into” parameter to specify the path to the file
d) By using the “append” parameter to specify the line to add and the “to” parameter to specify the path to the file

Answer: a) By using the “line” parameter to specify the line to add and the “path” parameter to specify the path to the file

Explanation: The Ansible module “lineinfile” can be used to add a line to a file on a target machine by using the “line” parameter to specify the line to add and the “path” parameter to specify the path to the file.

56. How can you use the Ansible module “wait_for” to wait for a port to be open on a target machine?

a) By using the “host” and “port” parameters to specify the host and port to wait for
b) By using the “address” and “port” parameters to specify the host and port to wait for
c) By using the “hostname” and “port” parameters to specify the host and port to wait for
d) By using the “ip” and “port” parameters to specify the host and port to wait for

Answer: a) By using the “host” and “port” parameters to specify the host and port to wait for

Explanation: The Ansible module “wait_for” can be used to wait for a port to be open on a target machine by using the “host” and “port” parameters to specify the host and port to wait for.

57. How can you use the Ansible module “file” to create a symbolic link on a target machine?

a) By using the “link” parameter to specify the link name and the “path” parameter to specify the path to the file
b) By using the “symlink” parameter to specify the link name and the “file” parameter to specify the path to the file
c) By using the “name” parameter to specify the link name and the “src” parameter to specify the path to the file
d) By using the “link_name” parameter to specify the link name and the “file_path” parameter to specify the path to the file

Answer: c) By using the “name” parameter to specify the link name and the “src” parameter to specify the path to the file

Explanation: The Ansible module “file” can be used to create a symbolic link on a target machine by using the “name” parameter to specify the link name and the “src” parameter to specify the path to the file.

58. How can you use the Ansible module “lineinfile” to replace a line in a file on a target machine?

a) By using the “line” parameter to specify the line to replace and the “replace” parameter to specify the replacement line
b) By using the “replace” parameter to specify the line to replace and the “line” parameter to specify the replacement line
c) By using the “before” parameter to specify the line to replace and the “after” parameter to specify the replacement line
d) By using the “old” parameter to specify the line to replace and the “new” parameter to specify the replacement line

Answer: b) By using the “replace” parameter to specify the line to replace and the “line” parameter to specify the replacement line

Explanation: The Ansible module “lineinfile” can be used to replace a line in a file on a target machine by using the “replace” parameter to specify the line to replace and the “line” parameter to specify the replacement line.

59. How can you use the Ansible module “user” to create a new user on a target machine?

a) By using the “name” parameter to specify the username and the “state” parameter to specify “present”
b) By using the “user” parameter to specify the username and the “state” parameter to specify “create”
c) By using the “username” parameter to specify the username and the “state” parameter to specify “new”
d) By using the “create_user” parameter to specify the username and the “state” parameter to specify “yes”

Answer: a) By using the “name” parameter to specify the username and the “state” parameter to specify “present”

Explanation: The Ansible module “user” can be used to create a new user on a target machine by using the “name” parameter to specify the username and the “state” parameter to specify “present”.

60. How can you use the Ansible module “apt” to install a package on a Debian-based target machine?

a) By using the “name” parameter to specify the package name and the “state” parameter to specify “installed”
b) By using the “package” parameter to specify the package name and the “state” parameter to specify “present”
c) By using the “pkg_name” parameter to specify the package name and the “pkg_state” parameter to specify “installed”
d) By using the “install” parameter to specify the package name and the “status” parameter to specify “installed”

Answer: b) By using the “package” parameter to specify the package name and the “state” parameter to specify “present”

Explanation: The Ansible module “apt” can be used to install a package on a Debian-based target machine by using the “package” parameter to specify the package name and the “state” parameter to specify “present”.

61. How can you use the Ansible module “yum” to update all packages on a Red Hat-based target machine?

a) By using the “name” parameter to specify “” and the “state” parameter to specify “latest”
b) By using the “package” parameter to specify “” and the “state” parameter to specify “latest”
c) By using the “packages” parameter to specify “” and the “state” parameter to specify “latest”
d) By using the “update” parameter to specify “” and the “status” parameter to specify “latest”

Answer: c) By using the “packages” parameter to specify “” and the “state” parameter to specify “latest”

Explanation: The Ansible module “yum” can be used to update all packages on a Red Hat-based target machine by using the “packages” parameter to specify “” and the “state” parameter to specify “latest”.

62. How can you use the Ansible module “shell” to run a shell command on a target machine?

a) By using the “command” parameter to specify the command to run
b) By using the “exec” parameter to specify the command to run
c) By using the “run” parameter to specify the command to run
d) By using the “shell_command” parameter to specify the command to run

Answer: a) By using the “command” parameter to specify the command to run

Explanation: The Ansible module “shell” can be used to run a shell command on a target machine by using the “command” parameter to specify the command to run.

63. How can you use the Ansible module “cron” to create a new cron job on a target machine?

a) By using the “name” parameter to specify the job name and the “job” parameter to specify the job details
b) By using the “job_name” parameter to specify the job name and the “details” parameter to specify the job details
c) By using the “cron_name” parameter to specify the job name and the “cron_job” parameter to specify the job details
d) By using the “state” parameter to specify “present” and the “job” parameter to specify the job details

Answer: a) By using the “name” parameter to specify the job name and the “job” parameter to specify the job details

Explanation: The Ansible module “cron” can be used to create a new cron job on a target machine by using the “name” parameter to specify the job name and the “job” parameter to specify the job details.

64. How can you use the Ansible module “template” to generate a configuration file on a target machine?

a) By using the “src” parameter to specify the template file and the “dest” parameter to specify the destination file
b) By using the “template_file” parameter to specify the template file and the “destination_file” parameter to specify the destination file
c) By using the “config” parameter to specify the template file and the “output” parameter to specify the destination file
d) By using the “source_file” parameter to specify the template file and the “output_file” parameter to specify the destination file

Answer: a) By using the “src” parameter to specify the template file and the “dest” parameter to specify the destination file

Explanation: The Ansible module “template” can be used to generate a configuration file on a target machine by using the “src” parameter to specify the template file and the “dest” parameter to specify the destination file. The template file can contain placeholders that will be replaced with values from Ansible variables or other sources during the template rendering process.

