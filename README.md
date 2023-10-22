# Ansible Role - Netbox Vyatta Facts

Ansible role to gather facts from Netbox for generating network device configurations. The facts are generic, but designed for the Vyatta configuration system (EdgeOS, VyOS).

An example playbook and config template can be found at [./example](./example).

Netbox Vyatta Facts
=========

Ansible role to gather facts from Netbox for generating network device configurations. The facts are generic, but designed for the Vyatta configuration system (EdgeOS, VyOS).

Example Playbook
----------------

```yaml
- name: Configure EdgeRouter
  hosts: edgerouter
  roles:
    - role: netbox-vyatta-facts
  post_tasks:
    - name: Apply config
      community.network.edgeos_config:
        src: example/config.j2
        backup: true
```

Author Information
------------------

[lu1as](https://github.com/lu1as)
