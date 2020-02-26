# Variable naming

Make sure to have unique variable names in order to not conflict with other existing variable prior or after the play/job sequence. In order to be most unique, start a variable name with the name of the role (in lower case), followed by an underscore symbol, followed by the rest of the name for the variable.

Specific rules:

- Ensure to comply to the naming convention to minimize conflicts.
- Ensure to have long names that say something about the contents of the variable which improves readability.
- Do not use creative (self made) abbreviations as they may not make sense to other users and developers.
- Regular string, integer, float and boolean values don't need *double quotes* or *single quotes* encapsulating them (yaml default).
- When using *quotes* to encapsulate values, use *single quotes* by default.
- Only use *double quotes* to encapsulate values that require *single quotes* as their value.
- Optionally use *single quotes* to encapsulate values that require *double quotes* as their value.

**Example:**
- Role human name: `Super Special Role`
- Role machine name: `super_special_role`

```yaml
---
super_special_role_hello_message: Hello, How are you?
super_special_role_hello_response: I am fine how about you you?

super_special_role_service_name: httpd
super_special_role_service_port: 80
super_special_role_service_permission: '0764'

super_special_role_shell_command_start_weird_service: "/bin/weird_app spawn -t _('-')/` -u hello_user"
super_special_role_shell_command_quit_weird_service: '/bin/weird_app suicide -f /"-"\ -u fubar'

super_special_role_weird_service_user_name: '{{ super_special_role_register_get_user }}'
super_special_role_weird_service_user_path: /path/to/special/place/{{ super_special_role_weird_service_user_name }}
```

More on variable can be found at: [Using variables](https://docs.ansible.com/ansible/latest/user_guide/playbooks_variables.html)
