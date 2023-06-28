# Quay Operator

This Helm chart creates a subscription to the latest version of [quay-operator](https://github.com/redhat-cop/quay-operator) and deploys an instance of this operator on OpenShift.

To apply the Helm chart run this command as a user with a *cluster-admin* role:

```
$ helm template -n openshift-operators -f operator/values.yaml operator | oc apply -f -
```

# Quay Instance

This Helm chart uses [quay-operator](https://github.com/redhat-cop/quay-operator) to install an instance of Red Hat Quay on OpenShift. Before deploying Quay, checkout out the configuration steps in the next section.

To deploy Red Hat Quay, run this command:

```
$ helm template -n quay-enterprise -f instance/values.yaml instance | oc apply -f -
```
