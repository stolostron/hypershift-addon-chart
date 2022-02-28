# hypershift-addon-chart

## Dependency
1. 'hypershiftDeployment' CRD
https://github.com/stolostron/hypershift-deployment-controller/blob/main/config/crd/cluster.open-cluster-management.io_hypershiftdeployments.yaml

2. 'manifestwork' CRD
https://github.com/open-cluster-management-io/api/blob/main/work/v1/0000_00_work.open-cluster-management.io_manifestworks.crd.yaml

3. s3 buckect creds in a secret `hypershift-operator-oidc-provider-s3-credentials`  at `open-cluster-management`