# What is an Ansible role?

A role is a collection or grouping of files that are stored in a standardized file structure primarily containing as set of tasks, variables, files, templates and handlers to achieve a certain state.

Roles are perfect for isolating a large set of tasks together with their own configuration and dependencies. Please understand that not everything can be put into roles or are worthy of a role. Generally everything starts with a playbook ranging from a single task to several plays to a set of hierarchical flow of playbooks and includes. Once there is a need for isolation/grouping certain actions together, it will become wise to evolve into an Ansible role. As rule of thumb an Ansible role is similar to program/script function, a confined set of engine parts that require an input and generate a certain output, idempotent.

More on this can be found at: [Roles](https://docs.ansible.com/ansible/latest/user_guide/playbooks_reuse_roles.html)

## Git each Role

Make sure to initialize the role as a git repository in order to make is easy to maintain and to share between teams.

## Files and templates

Do not confuse the files and templates, basically it comes down to:

- A file is a static object file.
- A template is a dynamic object file using Jinja2 templating to generate a static file.

**Templates**  
Use these specifically to deploy dynamic files on remote nodes. Templates have to be placed in the *templates directory* with their file names ending in `.j2`. Use these templates with the **template** module when using them inside tasks.

**Files**  
Use these for any purpose except for dynamically templating. Ensure they exist in the *files directory* in order to perform correct look-up's.

## Variables "defaults" and "vars"

Do not confuse variable precedence. Basically it comes down to:

- Variable `defaults` should be used when users should have the freedom of choice.
- Variable `vars` should be used when users do not have the freedom of choice and the internals require a specific set to work properly which has to be forced upon.

It all boils down to the variable precedence. More on this topic is found at: [Variable precedence](https://docs.ansible.com/ansible/latest/user_guide/playbooks_variables.html#variable-precedence-where-should-i-put-a-variable)
