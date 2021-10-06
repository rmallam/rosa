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
I: To create this cluster again in the future, you can run:
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

(⎈ |myapp/aks-cluste-aks-resource-gro-983c6f-15d1018f-hcp-australiasoutheast-azmk8s-io:443/token-VFJmT6HyYr1K:myapp)➜  vodapoc 
$rosa logs install -c rosatest --watch
I: Cluster 'rosatest' is in pending state waiting for installation to begin. Logs will show up within 5 minutes
- 
/ 
\ 
/ 
\ 
| 
- 
/ ^C
(⎈ |myapp/aks-cluste-aks-resource-gro-983c6f-15d1018f-hcp-australiasoutheast-azmk8s-io:443/token-VFJmT6HyYr1K:myapp)➜  vodapoc 
$rosa list
List all resources of a specific type

Usage:
  rosa list [command]

Available Commands:
  addons         List add-on installations
  clusters       List clusters
  idps           List cluster IDPs
  ingresses      List cluster Ingresses
  instance-types List Instance types
  machinepools   List cluster machine pools
  regions        List available regions
  upgrades       List available cluster upgrades
  users          List cluster users
  versions       List available versions

Flags:
  -h, --help             help for list
      --profile string   Use a specific AWS profile from your credential file.
      --region string    Use a specific AWS region, overriding the AWS_REGION environment variable.

Global Flags:
      --debug   Enable debug mode.

Use "rosa list [command] --help" for more information about a command.
(⎈ |myapp/aks-cluste-aks-resource-gro-983c6f-15d1018f-hcp-australiasoutheast-azmk8s-io:443/token-VFJmT6HyYr1K:myapp)➜  vodapoc 
$rosa list clusters
ID                                NAME      STATE
1nlac469tln268r149c87sp9dh6j04gu  rosatest  pending
(⎈ |myapp/aks-cluste-aks-resource-gro-983c6f-15d1018f-hcp-australiasoutheast-azmk8s-io:443/token-VFJmT6HyYr1K:myapp)➜  vodapoc 
$rosa logs install -c rosatest --watch

I: Cluster 'rosatest' is in pending state waiting for installation to begin. Logs will show up within 5 minutes
\ ^C
(⎈ |myapp/aks-cluste-aks-resource-gro-983c6f-15d1018f-hcp-australiasoutheast-azmk8s-io:443/token-VFJmT6HyYr1K:myapp)➜  vodapoc 
$rosa create operator-roles --cluster rosatest
? Operator policy prefix (optional): 
? Permissions boundary ARN (optional): 
? Role creation mode: auto
I: Creating roles using 'arn:aws:iam::914054700962:role/assumeopenshift'
? Create the 'rosatest-x1e9-openshift-machine-api-aws-cloud-credentials' role? Yes
I: Created role 'rosatest-x1e9-openshift-machine-api-aws-cloud-credentials' with ARN 'arn:aws:iam::914054700962:role/rosatest-x1e9-openshift-machine-api-aws-cloud-credentials'
E: There was an error creating the operator roles: Failed to attach role policy. Check your prefix or run 'rosa create account-roles' to create the necessary policies: NoSuchEntity: Policy arn:aws:iam::914054700962:policy/ManagedOpenShift-openshift-machine-api-aws-cloud-credentials does not exist or is not attachable.
	status code: 404, request id: f67085ca-8e51-4dd6-9991-b1546af24d9c
(⎈ |myapp/aks-cluste-aks-resource-gro-983c6f-15d1018f-hcp-australiasoutheast-azmk8s-io:443/token-VFJmT6HyYr1K:myapp)➜  vodapoc 
$rosa create account-roles
? OpenShift version: 4.8
? Role prefix: ManagedOpenShift
? Permissions boundary ARN (optional): 
? Role creation mode: auto
I: Creating roles using 'arn:aws:iam::914054700962:role/assumeopenshift'
? Create the 'ManagedOpenShift-Installer-Role' role? Yes
I: Created role 'ManagedOpenShift-Installer-Role' with ARN 'arn:aws:iam::914054700962:role/ManagedOpenShift-Installer-Role'
? Create the 'ManagedOpenShift-ControlPlane-Role' role? Yes
I: Created role 'ManagedOpenShift-ControlPlane-Role' with ARN 'arn:aws:iam::914054700962:role/ManagedOpenShift-ControlPlane-Role'
? Create the 'ManagedOpenShift-Worker-Role' role? Yes
I: Created role 'ManagedOpenShift-Worker-Role' with ARN 'arn:aws:iam::914054700962:role/ManagedOpenShift-Worker-Role'
? Create the 'ManagedOpenShift-Support-Role' role? Yes
I: Created role 'ManagedOpenShift-Support-Role' with ARN 'arn:aws:iam::914054700962:role/ManagedOpenShift-Support-Role'
? Create the operator policies for OpenShift 4.8? Yes
I: Created policy with ARN 'arn:aws:iam::914054700962:policy/ManagedOpenShift-openshift-machine-api-aws-cloud-credentials'
I: Created policy with ARN 'arn:aws:iam::914054700962:policy/ManagedOpenShift-openshift-cloud-credential-operator-cloud-crede'
I: Created policy with ARN 'arn:aws:iam::914054700962:policy/ManagedOpenShift-openshift-image-registry-installer-cloud-creden'
I: Created policy with ARN 'arn:aws:iam::914054700962:policy/ManagedOpenShift-openshift-ingress-operator-cloud-credentials'
I: Created policy with ARN 'arn:aws:iam::914054700962:policy/ManagedOpenShift-openshift-cluster-csi-drivers-ebs-cloud-credent'
I: To create a cluster with these roles, run the following command:
rosa create cluster --sts
(⎈ |myapp/aks-cluste-aks-resource-gro-983c6f-15d1018f-hcp-australiasoutheast-azmk8s-io:443/token-VFJmT6HyYr1K:myapp)➜  vodapoc 
$rosa create operator-roles --cluster rosatest
? Operator policy prefix (optional): 
? Permissions boundary ARN (optional): 
? Role creation mode: auto
I: Creating roles using 'arn:aws:iam::914054700962:role/assumeopenshift'
? Create the 'rosatest-x1e9-openshift-machine-api-aws-cloud-credentials' role? Yes
I: Created role 'rosatest-x1e9-openshift-machine-api-aws-cloud-credentials' with ARN 'arn:aws:iam::914054700962:role/rosatest-x1e9-openshift-machine-api-aws-cloud-credentials'
? Create the 'rosatest-x1e9-openshift-cloud-credential-operator-cloud-credenti' role? Yes
I: Created role 'rosatest-x1e9-openshift-cloud-credential-operator-cloud-credenti' with ARN 'arn:aws:iam::914054700962:role/rosatest-x1e9-openshift-cloud-credential-operator-cloud-credenti'
? Create the 'rosatest-x1e9-openshift-image-registry-installer-cloud-credentia' role? Yes
I: Created role 'rosatest-x1e9-openshift-image-registry-installer-cloud-credentia' with ARN 'arn:aws:iam::914054700962:role/rosatest-x1e9-openshift-image-registry-installer-cloud-credentia'

? Create the 'rosatest-x1e9-openshift-ingress-operator-cloud-credentials' role? Yes
I: Created role 'rosatest-x1e9-openshift-ingress-operator-cloud-credentials' with ARN 'arn:aws:iam::914054700962:role/rosatest-x1e9-openshift-ingress-operator-cloud-credentials'
? Create the 'rosatest-x1e9-openshift-cluster-csi-drivers-ebs-cloud-credential' role? Yes
I: Created role 'rosatest-x1e9-openshift-cluster-csi-drivers-ebs-cloud-credential' with ARN 'arn:aws:iam::914054700962:role/rosatest-x1e9-openshift-cluster-csi-drivers-ebs-cloud-credential'
(⎈ |myapp/aks-cluste-aks-resource-gro-983c6f-15d1018f-hcp-australiasoutheast-azmk8s-io:443/token-VFJmT6HyYr1K:myapp)➜  vodapoc 
$rosa create oidc-provider --cluster rosatest
? OIDC provider creation mode: auto
I: Creating OIDC provider using 'arn:aws:iam::914054700962:role/assumeopenshift'
? Create the OIDC provider for cluster 'rosatest'? Yes
I: Created OIDC provider with ARN 'arn:aws:iam::914054700962:oidc-provider/rh-oidc.s3.us-east-1.amazonaws.com/1nlac469tln268r149c87sp9dh6j04gu'
(⎈ |myapp/aks-cluste-aks-resource-gro-983c6f-15d1018f-hcp-australiasoutheast-azmk8s-io:443/token-VFJmT6HyYr1K:myapp)➜  vodapoc 
