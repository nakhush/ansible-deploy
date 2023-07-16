![jenkins](./pictures/jenkins-logo-2.png) ![apache](./pictures/Apache_HTTP_server_logo_(2019-present).svg.png) ![ansible](./pictures/ansible-ar21.png)

# CI/CD Pipeline with Jenkins and Ansible

## Description

This repository demonstrates a method to automatically deploy a web page to an Apache web server using Ansible script and Jenkins Pipeline

## Features

Two virtual machines raised in [Yandex Compute Cloud](https://cloud.yandex.ru/docs/compute/) are a master node and a managed node. ![screen](./pictures/2023-07-16_12-43.png)
The master has [Ansible](https://docs.ansible.com/) and [Jenkins](https://www.jenkins.io/doc/) installed.
Jenkins job is configured to interact automatically with the github repository after a push action. Any push to this repository on the Jenkins server starts a Job containing a Jenkinsfile that runs an Ansible script that deploys a web page to an [Apache](https://httpd.apache.org/docs/2.4/) server on a managed node. This process is repeated whenever this repository changes.

