# Quay Bridge Operator

This Helm chart creates a subscription to the latest version of [Quay Bridge Operator](https://github.com/quay/quay-bridge-operator) and deploys an instance of this operator on OpenShift.

The Helm chart deploys to the target namespace called `openshift-operators`. Operator responsible for facilitating the utilization of Red Hat Quay as the default image registry for an OpenShift Container Platform environment.

To apply the Helm chart run this command as a user with a *cluster-admin* role:

```
$ helm template -n openshift-operators -f operator/values.yaml operator | oc apply -f -
```
