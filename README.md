# hypershift-addon-chart

## Dependency
1. `hypershiftDeployment` CRD

https://github.com/stolostron/hypershift-deployment-controller/blob/main/config/crd/cluster.open-cluster-management.io_hypershiftdeployments.yaml

2. `manifestwork` CRD

https://github.com/open-cluster-management-io/api/blob/main/work/v1/0000_00_work.open-cluster-management.io_manifestworks.crd.yaml

3. s3 buckect creds in a secret `hypershift-operator-oidc-provider-s3-credentials`  at `open-cluster-management`


**Note** this chart is intended to be migrated to the [backplane](https://github.com/stolostron/backplane-operator/tree/main/pkg/templates/charts) as a toggled component for ACM 2.5 release.


## Install

1. clone this repo
2. `cd` to the clone directory
3. run `helm install hypershift-addon ./` to install this chart
4. verify the installation
```
$ helm list
NAME            	NAMESPACE	REVISION	UPDATED                             	STATUS  	CHART                       	APP VERSION
hypershift-addon	default  	1       	2022-02-28 13:48:19.368608 -0500 EST	deployed	hypershift-addon-chart-0.1.0	2.5.0

$ oc get deploy -n open-cluster-management | grep hypershift

hypershift-addon-manager                         1/1     1            1           5m34s
hypershift-deployment-controller                 2/2     2            2           5m34s
```

## Uninstall
1. go to the clone dirctroy
2. run `helm uninstall hypershift-addon` to install this chart
