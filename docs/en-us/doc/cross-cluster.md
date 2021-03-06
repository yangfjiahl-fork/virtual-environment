# Cross-cluster isolation

By default, the isolation rules generated by VirtualEnvironment instances are only apply to Pods in the same namespace. But in fact, this isolation capability can also be used across namespaces or even clusters.

When a request is sent to a Pod in another namespace or another Kubernetes cluster, if the target cluster has VirtualEnvironment CRD deployed and the target namespace has a VirtualEnvironment instance with the same configuration, the request will keep the same isolation-based routing rule within that namespace.

![cross-cluster](https://virtual-environment.oss-cn-zhangjiakou.aliyuncs.com/image/cross-cluster.jpg)
