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

Reference links
* https://www.asd.gov.au/publications/protect/hardening-ms-office-2016.htm
* https://www.asd.gov.au/publications/protect/ms-office-macro-security.htm
* http://www.asd.gov.au/publications/protect/Microsoft_Office_Macro_Security.pdf
* https://blogs.technet.microsoft.com/mmpc/2016/03/22/new-feature-in-office-2016-can-block-macros-and-help-prevent-infection/
* https://technet.microsoft.com/en-us/library/cc179076.aspx    ActiveX in Office
* https://technet.microsoft.com/en-us/library/cc179039.aspx
* https://doublepulsar.com/oleoutlook-bypass-almost-every-corporate-security-control-with-a-point-n-click-gui-37f4cbc107d0
* https://blogs.technet.microsoft.com/mmpc/2016/06/14/wheres-the-macro-malware-author-are-now-using-ole-embedding-to-deliver-malicious-files/
* https://www.endgame.com/blog/technical-blog/bug-feature-debate-back-yet-again-ddeauto-root-cause-analysis
* https://blog.barkly.com/microsoft-office-malware-attack-no-macros
* https://gist.github.com/wdormann/732bb88d9b5dd5a66c9f1e1498f31a1b
* https://technet.microsoft.com/en-us/library/security/4053440
* https://blogs.technet.microsoft.com/diana_tudor/2014/12/02/microsoft-project-how-to-control-macro-settings-using-registry-keys/

## License

BSD 2-clause

