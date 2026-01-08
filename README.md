[![CI](https://github.com/de-it-krachten/ansible-role-accounting/workflows/CI/badge.svg?event=push)](https://github.com/de-it-krachten/ansible-role-accounting/actions?query=workflow%3ACI)


# ansible-role-accounting

Setup process accounting



## Dependencies

#### Roles
None

#### Collections
None

## Platforms

Supported platforms

- Red Hat Enterprise Linux 8<sup>1</sup>
- Red Hat Enterprise Linux 9<sup>1</sup>
- Red Hat Enterprise Linux 10<sup>1</sup>
- RockyLinux 8
- RockyLinux 9
- RockyLinux 10
- OracleLinux 8
- OracleLinux 9
- OracleLinux 10
- AlmaLinux 8
- AlmaLinux 9
- AlmaLinux 10
- SUSE Linux Enterprise 15<sup>1</sup>
- openSUSE Leap 15
- Debian 11 (Bullseye)
- Debian 12 (Bookworm)
- Debian 13 (Trixie)
- Ubuntu 22.04 LTS
- Ubuntu 24.04 LTS
- Fedora 42
- Fedora 43

Note:
<sup>1</sup> : no automated testing is performed on these platforms

## Role Variables
### defaults/main.yml
<pre><code>

</pre></code>

### defaults/family-Debian.yml
<pre><code>
# List of packages
accounting_packages:
  - acct

# Service to start
accounting_service: acct

# Accounting file
accounting_file: /var/log/account/pacct
</pre></code>

### defaults/family-RedHat.yml
<pre><code>
# List of packages
accounting_packages:
  - psacct

# Service to start
accounting_service: psacct

# Accounting file
accounting_file: /var/account/pacct
</pre></code>

### defaults/family-Suse.yml
<pre><code>
# List of packages
accounting_packages:
  - acct

# Service to start
accounting_service: acct

# Accounting file
accounting_file: /var/log/account/pacct
</pre></code>




## Example Playbook
### molecule/default/converge.yml
<pre><code>
- name: sample playbook for role 'accounting'
  hosts: all
  become: 'yes'
  tasks:
    - name: Include role 'accounting'
      ansible.builtin.include_role:
        name: accounting
</pre></code>
