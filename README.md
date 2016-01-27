# ansible-lookup-pass

Ansible lookup plugin for pass (password-store).


Using python's `check_output` this plugin will retrieve variable values using
the pass prompt. Useful if you already store your passwords using pass.

__Alternative__: [Ansible Vault][1]

## Usage:

``` yaml
- hosts: all
  vars:
    test_var: "{{lookup('pass', 'path/to/password')}}"
  tasks:
    - debug: msg="{{test_var}}"
```

[1]: http://docs.ansible.com/ansible/playbooks_vault.html
