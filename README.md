# Jenkins-installation-automation
An Ansible playbook installing Jenkins includes Java JDK install and service start
## Prerequisites

- Ansible installed on master server
- Ansible superuser privileges on target server

## Execution example

```
ansible-playbook jenkins_install.yaml 
```

## Output example

A short example of an output
- in this case installing Jenkins from master server "yamp1" on target server "yamp2"

```
[ansible@yamp1 playbooks]$ ansible-playbook jenkins_install.yaml 
[DEPRECATION WARNING]: DEFAULT_SUDO_USER option, In favor of Ansible Become, which is a generic 
framework. See become_user. , use become instead. This feature will be removed in version 2.8. 
Deprecation warnings can be disabled by setting deprecation_warnings=False in ansible.cfg.

PLAY [centos] ***************************************************************************************

TASK [Gathering Facts] ******************************************************************************
ok: [yamp2.mylabserver.com]

TASK [Installing Java version 1.8-openjdk] **********************************************************
changed: [yamp2.mylabserver.com]

TASK [Download Jenkins repo] ************************************************************************
changed: [yamp2.mylabserver.com]

TASK [Import a key from URL] ************************************************************************
changed: [yamp2.mylabserver.com]

TASK [Install Jenkins] ******************************************************************************
changed: [yamp2.mylabserver.com]

RUNNING HANDLER [enable and start jenkins service] **************************************************
changed: [yamp2.mylabserver.com]

PLAY RECAP ******************************************************************************************
yamp2.mylabserver.com   : ok=6    changed=5    unreachable=0    failed=0   



```

## Built With

* [Bash](https://www.gnu.org/software/bash/) - The GNU Project's shell
* [Ansible](https://www.ansible.com/) - Simple, agentless IT automation
* [Jenkins](https://jenkins.io/) -  open source automation server provides support for building, deploying and automating any project.

## Versioning

Untill this point there is only ver 1.0

## Authors

* [Yam Peled](https://github.com/yampeled1)
