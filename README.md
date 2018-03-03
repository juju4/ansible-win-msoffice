[![Build Status - Master](https://travis-ci.org/juju4/ansible-win-msoffice.svg?branch=master)](https://travis-ci.org/juju4/ansible-win-msoffice)
[![Build Status - Devel](https://travis-ci.org/juju4/ansible-win-msoffice.svg?branch=devel)](https://travis-ci.org/juju4/ansible-win-msoffice/branches)(Syntax Only)

[![Appveyor - Master](https://ci.appveyor.com/api/projects/status/m0qj12g9niyr86yo?svg=true)](https://ci.appveyor.com/project/juju4/ansible-win-msoffice)
![Appveyor - Devel](https://ci.appveyor.com/api/projects/status/m0qj12g9niyr86yo/branch/devel?svg=true)

# MsOffice security ansible role

Ansible role to setup MsOffice security on Windows system.

## Requirements & Dependencies

### Ansible
It was tested on the following versions:
 * 2.3
 * 2.4
 * 2.5b2

### Operating systems

Tested in Appveyor

## Example Playbook

Just include this role in your list.
For example

```
- host: all
  roles:
    - juju4.win-msoffice
```

Run
```
$ ansible -i inventory -m win_ping win --ask-pass
$ ansible-playbook -i inventory --limit win site.yml
```

## Variables

See defaults/main.yml for full scope

## Continuous integration

This role has a travis basic test (for github, syntax check only), Appveyor test and a Vagrantfile (test/vagrant).

```
$ cd /path/to/roles/juju4.win-msoffice/test/vagrant
$ vagrant up
$ vagrant provision
$ vagrant destroy
$ ansible -i .vagrant/provisioners/ansible/inventory/vagrant_ansible_inventory -m win_ping -e ansible_winrm_server_cert_validation=ignore -e ansible_ssh_port=55986 all
```

## Troubleshooting & Known issues

## FAQ

## License

BSD 2-clause

