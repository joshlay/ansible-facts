# custom-facts

Place these in `/etc/ansible/facts.d` so that Ansible will read/execute them.
[More information](https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_vars_facts.html#adding-custom-facts)

## Preview

```shell
~ $ ansible localhost -m setup -a 'filter=ansible_local'
localhost | SUCCESS => {
    "ansible_facts": {
        "ansible_local": {
            "amdgpu": {
                "cards": {
                    "card1": {
                        "device": "../../../0000:03:00.0",
                        "hwmon_dir": "/sys/class/drm/card1/device/hwmon/hwmon2"
                    }
                },
                "stats": {
                    "card1": {
                        "power": {
                            "power1_average": 36000000,
                            "power1_cap": 281000000,
                            "power1_cap_default": 281000000,
                            "power1_cap_max": 323000000,
                            "power1_cap_min": 252000000,
                            "power1_label": "PPT",
                            "power1_use_pct": 12.8
                        }
                    }
                }
            },
            "atomicity": {
                "is_atomic": false
            },
            "cloudcfg": {
                "is_cloudy": false
            },
            "os": {
                "is_atomic": false,
                "is_cloudy": false,
                "is_efi": true
            },
            "tuned": {
                "active": true,
                "selected_profile": "latency-performance-amdgpu-default"
            }
        }
    },
    "changed": false
}
```
