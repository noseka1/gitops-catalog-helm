# Container Security Operator

This Helm chart creates a subscription to the latest version of [Container Security Operator](https://github.com/quay/container-security-operator) and deploys an instance of this operator on OpenShift.

Helm chart deploys to the target namespace called `openshift-operators`. Pods in all namespaces will be monitored for vulnerabilities.

To apply the Helm chart run this command as a user with a *cluster-admin* role:

```
$ helm template -n openshift-operators -f operator/values.yaml operator | oc apply -f -
```
