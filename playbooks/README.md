# STIG on Ceph nodes
We are using the RHEL 7 STIG to harden the Ceph Debian Buster nodes. This
is the approach that the OpenStack people are taking.

1. Clone the git repository for ansible-hardening.
   https://github.com/whaddock/ansible-hardening.git
   Use the "main" branch.

2. This ansible code provides the roles for the STIG hardening.
   Create a directory, ceph-stig, and drop the ansible-hardening
   tree inside of it. Then, copy the files in the playbooks directory
   to the ceph-stig directory. You can then run the code:
   ansible-playbook --check -i localhost.yml ansible-hardening.yml

3. Explanation of the options are found at:
   https://docs.openstack.org/ansible-hardening/latest/domains.html


# Usage

```bash
ansible-playbook -i hosts.yml ansible-hardening.yml
```
