# kube-sample-code
sample-code-kube-depleyemnt-ref


https://drive.google.com/drive/folders/1DSx1NwkRhD_ycRT58S3opwbXBHNWJaSF?usp=sharing

kubectl Get All Manifests
# Export all resources from all namespaces
kubectl get all --all-namespaces -o yaml > all-resources.yaml

# More comprehensive export including RBAC, storage, networking, etc.
kubectl get $(kubectl api-resources --verbs=list -o name | paste -sd, -) --all-namespaces -o yaml > full-cluster-export.yaml

Important Resource Categories to Include
For a complete collection, ensure you have examples of:

###################Workloads#########

Pods

Deployments

StatefulSets

DaemonSets

Jobs/CronJobs

ReplicaSets

###################Networking################

Services

Ingress

NetworkPolicies

Endpoints

########################Storage#####################

PersistentVolumes

PersistentVolumeClaims

StorageClasses

VolumeAttachments

######################Configuration##################

ConfigMaps

Secrets

ResourceQuotas

LimitRanges

RBAC

Roles

RoleBindings

ClusterRoles

ClusterRoleBindings

ServiceAccounts

####################Cluster Management##################

Nodes

Namespaces

RuntimeClasses

PriorityClasses

#################Custom Resources####################

CRDs (Custom Resource Definitions)

Any CRs (Custom Resources) specific to your environment
