# Vagrantfile and Scripts to Automate Kubernetes Setup using Kubeadm [Practice Environment for CKA/CKAD and CKS Exams]

## Documentation

Current k8s version for CKA, CKAD and CKS exam: 1.24

🚀 CKA, CKAD, CKS or KCNA Coupon Codes

If you are preparing for Prometheus Certification, CKA, CKAD, CKS, or KCNA exam, **save 50%** today using code **CYBER22CC** at https://kube.promo/latest. It is a limited-time offer. Or Check out [Linux Foundation coupon](https://scriptcrunch.com/linux-foundation-coupon/) page for the latest voucher codes.

## Prerequisites

1. Working Vagrant setup
2. 16 G + RAM workstation as the VMs use 5 vCPUS and 4+ GB RAM

## Usage/Examples

To provision the cluster, execute the following commands.

```shell
git clone https://github.com/scriptcamp/vagrant-kubeadm-kubernetes.git
cd vagrant-kubeadm-kubernetes9
vagrant up master && vagrant up
```

## Set Kubeconfig file variable

```shell
cd vagrant-kubeadm-kubernetes
cd configs
export KUBECONFIG=$(pwd)/config
```

or you can copy the config file to .kube directory.

```shell
cp config ~/.kube/
```

## Kubernetes Dashboard URL

```shell
http://localhost:8001/api/v1/namespaces/kubernetes-dashboard/services/https:kubernetes-dashboard:/proxy/#/overview?namespace=kubernetes-dashboard
```

## Kubernetes login token

Vagrant up will create the admin user token and saves in the configs directory.

```shell
cd vagrant-kubeadm-kubernetes
cd configs
cat token
```

## To shutdown the cluster,

```shell
vagrant halt
```

## To restart the cluster,

```shell
vagrant up
```

## To destroy the cluster,

```shell
vagrant destroy -f
```
