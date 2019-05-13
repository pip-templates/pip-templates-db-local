# Overview
Scriptable databases introduce “infrastructure as a code” into devops practices. Use minikube to install kubernetes cluster, couchbase with couchbase sync gateway deployed into kubernetes cluster.

# Syntax
All sripts have one required paramenter - *$ConfigPath*. This is the path to config, path can be absolute or relative. 

**Examples of installing aks**
Relative path example (you should be in *piptemplates-devops-envmgmt* folder):
`
./local/install_couchbase.ps1 ./config/local_config.json
`
Absolute path example:
`
~/pip-templates-db-local/cloud/install_couchbase.ps1 ~/pip-templates-db-local/config/local_config.json
`

**Example delete script**
`
./local/destroy_couchbase.ps1 ./config/local_config.json
`

Also you can install environment using single script:
`
./create_env.ps1 ./config/local_config.json
`

Delete whole environment:
`
./delete_env.ps1 ./config/local_config.json
`

If you have any problem with not installed tools - use `install_prereq_` script for you type of operation system.

# Project structure
| Folder | Description |
|----|----|
| Config | Config files for scripts. Store *example* configs for each environment, recomendation is not change this files with actual values, set actual values in duplicate config files without *example* in name. Also stores *resources* files, created automaticaly. | 
| Lib | Scripts with support functions like working with configs, templates etc. | 
| Local | Scripts related to management local couchbase cluster |  

### Local couchbase

* Local couchbase config parameters

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
