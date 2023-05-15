# Ansible <!-- omit in toc -->

I already did the [Ansible Up & Running](https://github.com/dallas-hall/learning-ansible) 2nd & 3rd edition textbooks. So the only thing documented here is new or something I didn't know.

https://www.osboxes.org/ contains some prebuilt and preconfigured VMs for Virtual Box or VMWare.

## Notes

* Ansible uses Powershell Remoting `winrm` to establish connections with Windows servers.
* `free_form` can be used to supply commands with the `command` module and other modules without using parameters as key/value pairs

```bash
# Free form example
- name: Run a script with arguments (free form)
  ansible.builtin.script: /some/local/script.sh --some-argument 1234
```

Everything after `with_*` is a lookup plugin. They are custom scripts that can do specific tasks.

```bash
# Search for roles
ansible-galaxy search $STRING

# View Ansible config
ansible-config dump | grep -i role
```
