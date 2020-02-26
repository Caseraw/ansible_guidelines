# Playbooks and Plays

Playbooks are scenarios that will be run sequentially. When using the Ansible engine, playbooks are called upon with the `ansible-playbook` command. When using Ansible Tower, playbooks have to be added as jobs. To make sure that paybooks can be run safely with both methods it is good practice to test with both methods.

Basic rules of engagement:

1. Think about what to achieve or what to solve and how to accomplish that.
2. Dissect large section in smaller independent chunks/parts.
3. Ensure each chuck/part works as expected.
4. Build the solution based on one or more stacked playbooks and/or plays and/or other inclusions such as tasks and roles.
5. Create a workflows that combine all the required chunks/parts to a unified solution.

More on this topic is found at: [Working with playbooks](https://docs.ansible.com/ansible/latest/user_guide/playbooks.html)
