# TrueNas Scale Configuration 
## Introduction
### Aliases
First, I start with creating the following aliases.
- [kubectl](#kubectl)


#### kubectl
Settings an alias for kubectl on TrueNas. This will allow you to use `> kubectl` instead of typing `> k3s kubectl` every time.
> alias kubectl="k3s kubectl"

### Exporting
I export the k3s.yml config file to the KUBECONFIG variable. This is how the k3s file is commonly available on k8s systems.
> export KUBECONFIG=/etc/rancher/k3s/k3s.yaml

### Getting the kubectl config file
If you have exported the KUBECONFIG, you can get your k3s config by running the following command.
> cat $KUBECONFIG

An alternative way to get the config is by running the following.

> cat /etc/rancher/k3s/k3s.yaml

### Allowing kubectl trough the firewall

### kubectl proxy
> kubectl proxy --address='0.0.0.0' --port=8002 --accept-hosts='.*'


