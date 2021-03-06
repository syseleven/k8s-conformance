## To reproduce:

 This Kubernetes conformance report is generated by Kubernetes on DC/OS.

 ### Provision the Kubernetes cluster

 To recreate these results, first you need to provision a DC/OS cluster, install the Mesosphere Kubernetes engine and create a Kubernetes cluster.
To do so, please follow [these instructions](https://github.com/mesosphere/dcos-kubernetes-quickstart/blob/master/docs/cncf_conformance.md#cncf-conformance).

 When the Kubernetes cluster is up and running, proceed to run the conformance tests.

 ### Run conformance tests

 Tests are run according to the [official instructions](https://github.com/cncf/k8s-conformance/blob/master/instructions.md):

 ```shell
$ go get -u -v github.com/heptio/sonobuoy
$ sonobuoy run
$ sonobuoy retrieve .
$ mkdir ./results; tar xzf *.tar.gz -C ./results
$ sonobuoy delete
```

 ### Clean-up

 To delete the entire infrastructure, please follow [these instructions](https://github.com/mesosphere/dcos-kubernetes-quickstart/blob/master/docs/cncf_conformance.md#destroy-the-infrastructure).