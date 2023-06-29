# OpenShift Sandboxed Containers

This Helm chart installs the OpenShift sandboxed containers operator. The official documentation for the operator can be found [here](https://access.redhat.com/documentation/en-us/openshift_sandboxed_containers/1.4/html-single/openshift_sandboxed_containers_user_guide/index).

Note that the operator will install a MachineConfig resource to enable the sandboxed containers extension on the cluster node. This will cause the cluster nodes to restart.

## Usage

Install the OpenShift sandboxed containers operator:

```
$ helm template -n openshift-sandboxed-containers-operator -f operator/values.yaml operator | oc apply -f -
```

Create cluster-wide kataconfig resource:

```
$ helm template -n openshift-sandboxed-containers-operator -f instance/values.yaml instance | oc apply -f -
```

Optionally, deploy a example workload that runs in a sandboxed container:

```
$ helm template -n openshift-sandboxed-containers-operator -f example-workload/values.yaml instance | oc apply -f -
```
