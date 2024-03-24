# custom-facts

Place these in `/etc/ansible/facts.d` so that Ansible will read/execute them.
[More information](https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_vars_facts.html#adding-custom-facts)

## Preview

```shell
~ $ ansible localhost -m setup -a 'filter=ansible_local'
localhost | SUCCESS => {
    "ansible_facts": {
        "ansible_local": {
            "atomicity": {
                "is_atomic": false
            }
        }
    },
    "changed": false
}
```
