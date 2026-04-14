# Ansible Roles

Roles are useful to write complex playbooks. Suppose like in a playbook, we have like 20 variables, and 50 tasks, and we have handlers, and we have metadata of the ansible. So instead of writing everything in a single playbook, we can segregate into these into different  folders, and the handlers into one folder, and the tasks into one folder, and these variables into one folder, and everything will put it one umbrella called roles. So, whenever we want to write a complex playbooks, roles are very helpful, and example take Kubernetes, installing the Kubernetes, setting up control nodes and data nodes configuring everything, it will be like very complex to put everything in a single playbook. Then that is the reason Ansible playbook comes into picture. 

An Ansible role is a reusable, self-contained unit of automation that is used to 
organize and manage tasks, variables, files, templates, and handlers in a structured way. 

Roles help to encapsulate and modularize the logic and configuration needed to manage 
a particular system or application component. 

This modular approach promotes reusability, maintainability, and consistency across different 
playbooks and environments.

## Key Components of an Ansible Role

### Tasks
The main list of actions that the role performs.

### Handlers
Tasks that are triggered by changes in other tasks, typically used for actions like restarting services.

### Files
Static files that need to be transferred to managed hosts.

### Templates
Jinja2 templates that can be rendered and transferred to managed hosts.

### Vars
Variables that are used within the role.

### Defaults
Default variables for the role, which can be overridden.

### Meta
Metadata about the role, including dependencies on other roles.

### Library
Custom modules or plugins used within the role.

### Module_defaults
Default module parameters for the role.

### Lookup_plugins
Custom lookup plugins for the role.

## Directory Structure of an Ansible Role

An Ansible role follows a specific directory structure:

```
<role_name>/
  ├── defaults/
  │   └── main.yml
  ├── files/
  ├── handlers/
  │   └── main.yml
  ├── meta/
  │   └── main.yml
  ├── tasks/
  │   └── main.yml
  ├── templates/
  ├── vars/
      └── main.yml
```

## Why Use Ansible Roles?

### Modularity
Roles allow you to break down complex playbooks into smaller, reusable components. 
Each role handles a specific part of the configuration or setup.

### Reusability
Once created, roles can be reused across different playbooks and projects. This saves time 
and effort in writing redundant code.

### Maintainability
By organizing related tasks into roles, it becomes easier to manage and maintain the code. 
Changes can be made in one place and applied consistently wherever the role is used.

### Readability
Roles make playbooks cleaner and easier to read by abstracting away the details into logically
named roles.

### Collaboration
Roles facilitate collaboration among team members by allowing them to work on different parts
of the infrastructure independently.

### Consistency
Using roles ensures that the same setup and configuration procedures are applied uniformly across
multiple environments, reducing the risk of configuration drift.
