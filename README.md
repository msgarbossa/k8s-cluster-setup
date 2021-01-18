# k8s-cluster-setup

Ansible playbooks

- basic-all.yml
- patching.yml (patch and reboot)
- basic-k8snodes.yml
- master.yml (init cluster)
- worker.yml (generate token on master, join workers)
- admin.yml (get admin.conf and setup kubectl)

- calico

```
curl https://docs.projectcalico.org/manifests/calico.yaml -O
update CALICO_IPV4POOL_CIDR w/ pod_network_cidr used to init cluster
kubectl --kubeconfig=admin.conf apply -f ../files/calico.yaml
```

- openebs.yml (cluster storage)
- auto-patch.yml (setup auto-patching using auto_patch role)
- kured.yml (automated rolling cluster node reboots)

