# kubernetes-monitor
monitor kubernetes cluster solution with prometheus

使用prometheus监控k8s资源部署方案
* kubernetes components (etcd coredns proxy apiserver schedule controller-manager)
* kubernetes resource object
* kubelet & cadvisor
* node_exporter
* alertmanager
* grafana
* prometheus
#### step1
```shell
kubectl create secret generic etcd-certs --from-file=/etc/kubernetes/pki/etcd/healthcheck-client.crt \
--from-file=/etc/kubernetes/pki/etcd/healthcheck-client.key \ 
--from-file=/etc/kubernetes/pki/etcd/ca.crt -n kube-system 
#这里需要替换为prometheus部署所在的namespace
```
#### standalone
#### cluster