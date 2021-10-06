# rosa

(⎈ |myapp/aks-cluste-aks-resource-gro-983c6f-15d1018f-hcp-australiasoutheast-azmk8s-io:443/token-VFJmT6HyYr1K:myapp)➜  vodapoc 
$rosa create cluster --interactive
I: Interactive mode enabled.
Any optional fields can be left empty and a default will be selected.
? Cluster name: rosatest
? Deploy cluster using AWS STS: Yes
? OpenShift version: 4.8.13
W: No account roles found. You will need to manually set them in the next steps or run 'rosa create account-roles' to create them first.
? Role ARN: arn:aws:iam::914054700962:role/assumeopenshift
? External ID (optional): 
? Support Role ARN: arn:aws:iam::914054700962:role/assumeopenshift
? Master IAM Role ARN: arn:aws:iam::914054700962:role/assumeopenshift
? Worker IAM Role ARN: arn:aws:iam::914054700962:role/assumeopenshift
? Operator roles prefix: rosatest-x1e9
? Multiple availability zones (optional): Yes
? AWS region: ap-southeast-2
? PrivateLink cluster (optional): No
? Install into an existing VPC (optional): Yes
? Subnet IDs (optional): 
? Enable Customer Managed key (optional): No
? Compute nodes instance type (optional): m5.xlarge
? Enable autoscaling (optional): Yes
X Sorry, your reply was invalid: Multi AZ cluster requires at least 3 compute nodes
? Min replicas: 3
X Sorry, your reply was invalid: Multi AZ clusters require that the number of compute nodes be a multiple of 3
? Max replicas: 3
? Machine CIDR: 10.0.0.0/16
? Service CIDR: 172.30.0.0/16
? Pod CIDR: 10.128.0.0/14
? Host prefix: 23
I: Creating cluster 'rosatest'

To create this cluster again in the future, you can run:
#rosa cli
rosa create cluster --cluster-name rosatest --role-arn arn:aws:iam::914054700962:role/assumeopenshift --support-role-arn arn:aws:iam::914054700962:role/assumeopenshift --master-iam-role arn:aws:iam::914054700962:role/assumeopenshift --worker-iam-role arn:aws:iam::914054700962:role/assumeopenshift --operator-roles-prefix rosatest-x1e9 --multi-az --region ap-southeast-2 --version 4.8.13 --enable-autoscaling --min-replicas 3 --max-replicas 3 --compute-machine-type m5.xlarge --machine-cidr 10.0.0.0/16 --service-cidr 172.30.0.0/16 --pod-cidr 10.128.0.0/14 --host-prefix 23

I: To view a list of clusters and their status, run 'rosa list clusters'
I: Cluster 'rosatest' has been created.
I: Once the cluster is installed you will need to add an Identity Provider before you can login into the cluster. See 'rosa create idp --help' for more information.
I: To determine when your cluster is Ready, run 'rosa describe cluster -c rosatest'.
I: To watch your cluster installation logs, run 'rosa logs install -c rosatest --watch'.
Name:                       rosatest
ID:                         1nlac469tln268r149c87sp9dh6j04gu
External ID:                
OpenShift Version:          
Channel Group:              stable
DNS:                        rosatest.xsl5.p1.openshiftapps.com
AWS Account:                914054700962
API URL:                    
Console URL:                
Region:                     ap-southeast-2
Multi-AZ:                   true
Nodes:
 - Master:                  3
 - Infra:                   3
 - Compute:                 3
Network:
 - Service CIDR:            172.30.0.0/16
 - Machine CIDR:            10.0.0.0/16
 - Pod CIDR:                10.128.0.0/14
 - Host Prefix:             /23
STS Role ARN:               arn:aws:iam::914054700962:role/assumeopenshift
Support Role ARN:           arn:aws:iam::914054700962:role/assumeopenshift
Instance IAM Roles:
 - Master:                  arn:aws:iam::914054700962:role/assumeopenshift
 - Worker:                  arn:aws:iam::914054700962:role/assumeopenshift
Operator IAM Roles:
 - arn:aws:iam::914054700962:role/rosatest-x1e9-openshift-cluster-csi-drivers-ebs-cloud-credential
 - arn:aws:iam::914054700962:role/rosatest-x1e9-openshift-machine-api-aws-cloud-credentials
 - arn:aws:iam::914054700962:role/rosatest-x1e9-openshift-cloud-credential-operator-cloud-credenti
 - arn:aws:iam::914054700962:role/rosatest-x1e9-openshift-image-registry-installer-cloud-credentia
 - arn:aws:iam::914054700962:role/rosatest-x1e9-openshift-ingress-operator-cloud-credentials
State:                      pending (Waiting for OIDC configuration)
Private:                    No
Created:                    Oct  6 2021 00:55:49 UTC
Details Page:               https://console.redhat.com/openshift/details/s/1z6wGMrYpwpkzGEwNwed0Kpwmy0
OIDC Endpoint URL:          https://rh-oidc.s3.us-east-1.amazonaws.com/1nlac469tln268r149c87sp9dh6j04gu
