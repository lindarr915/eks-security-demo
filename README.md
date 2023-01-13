### EKS Security Demo




## Using Kyverno to block ClusterRoleBinding to `kubernetes-admin` 



```
➜  eks-security-demo git:(main) ✗ kubectl apply -f rbac-anonymous-admin.yaml 
Error from server: error when creating "rbac-anonymous-admin.yaml": admission webhook "validate.kyverno.svc-fail" denied the request: 

policy ClusterRoleBinding//cluster-admin-anonymous for resource violation: 

restrict-binding-clusteradmin:
  clusteradmin-bindings: 'validation error: Binding to cluster-admin is not allowed.
    rule clusteradmin-bindings failed at path /roleRef/name/'
```