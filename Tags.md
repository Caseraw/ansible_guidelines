# Tags

Use tags where applicable. This eases the use by dissecting large comprehensive tasks into smaller chunks to execute.  
For more on tags and usage: [Tags](https://docs.ansible.com/ansible/latest/user_guide/playbooks_tags.html)

> Please note that tags are only available when using static includes.  
> Sources with info about this:  
> - <https://docs.ansible.com/ansible/latest/user_guide/playbooks_reuse_includes.html>
> - <https://docs.ansible.com/ansible/latest/user_guide/playbooks_reuse.html>

## Tag naming

Just like with variables, tags can be misused (unintentionally). Make sure to name your tags accordingly. Always check which tags are used before reusing one or introducing a new one.

## Tips Trics

The command `ansible-playbook` contains a parameter called `--list-tags`.  
Use this to list out all the tags that are used withing a playbook.

**Example:**  
*The goal is to list all tags, match for `special_something` and follow up by sorting an de-deuplicating the output.*

```shell
ansible-playbook super_awesome_playbook.yml --list-tags | grep -o "\w*special_something\w*" | sort | uniq

tag_special_something_install_packages
tag_special_something_deploy_config
tag_special_something_start_enable_service
tag_special_something_manage_firewall
```
