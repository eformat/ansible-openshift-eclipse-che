Ansible Role: Eclipse Che on OpenShift
[![Build Status](https://travis-ci.org/siamaksade/ansible-openshift-che.svg?branch=master)](https://travis-ci.org/siamaksade/ansible-openshift-che)
=========

Ansible Role for deploying [Eclipse Che](https://www.eclipse.org/che/) web-based IDE in 
single-user mode on OpenShift. 

Role Variables
------------

| Variable                    | Default Value     | Required |  Description   |
|-----------------------------|--------------------|----------|----------------|
|`route_suffix`               | `127.0.0.1.nip.io` | Required | Apps route suffix in the OpenShift cluster |
|`che_version`                | `latest`           | Optional | Eclipse Che image version as available on [Docker Hub](https://hub.docker.com/r/eclipse/che/tags/) |
|`project_name`               | `che`              | Optional | OpenShift project name for the Gogs container  |
|`project_display_name`       | `Eclipse Che IDE`  | Optional | OpenShift project display name for the Gogs container  |
|`project_desc`               | `Eclipse Che IDE`  | Optional | OpenShift project description for the Gogs container |
|`project_annotations`        | -                  | Optional | OpenShift project annotations for the Gogs container |
|`project_admin`              | -                  | Optional | If set, the user to be assigned as project admin |
|`multi_user`                 | `false`            | Optional | Multi-user or single-user mode |
|`multi_user_che_tls`         | `false`            | Optional | For multi-user mode, enable TLS  |
|`multi_user_che_protocol`    | `http`             | Optional | For multi-user mode, `http` or `https` protocol |
|`multi_user_che_ws_protocol` | `ws`               | Optional | For multi-user mode, `ws` or `wss` protocol |
|`keycloak_admin_user`        | `admin`            | Optional | For multi-user mode, Keycloak admin user to be created |
|`keycloak_admin_user`        | `admin`            | Optional | For multi-user mode, Keycloak admin password to be created |
|`install_java_oc_stack`      | `false`            | Optional | Install a Java stack with Maven, OpenShift CLI and Ansible |
|`openshift_cli`              | `oc`               | Optional | OpenShift CLI command and arguments (e.g. auth) | 


Run Me
------

```bash
ansible-playbook -i inventory ocp-nexus-configure.yml
```
