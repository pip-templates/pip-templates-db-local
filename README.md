# Overview

This is a built-in module to environment [pip-templates-env-master](https://github.com/pip-templates/pip-templates-env-master). 
This module stores scripts for management local couchbase db inside kubernetes cluster.

# Usage

- Download this repository
- Copy *src* folder to master template
- Add content of *.ps1.add* files to correspondent files from master template
- Add content of *config/config.db.json.add* to json config file from master template and set the required values

# Config parameters

Config variables description


| Variable | Default value | Description |
|----|----|---|
| env_type | local | Type of environment |
| minikube_home |  | Path of *.minikube* folder, if it is not located in home directory.  |
| k8s_version | v1.9.4 | Kuberntes cluster version |
| k8s_driver | virtualbox | Driver for minikube kubernetes cluster |
| k8s_memory | 8198 | Memory allocated to minikube vm |
| k8s_cpus | 2 | Minikube cpu |
| couchbase_username | piptemplatesadmin | Couchbase credentials |
| couchbase_password | piptemplatesadmin2019# | Couchbase credentials |
