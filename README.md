# nfs-provisioner
yaml files to install nfs provisioner on OpenShift

Install steps
1. Ensure that the current project is "default"
2. oc project default
3. oc apply -f rbac.yaml
4. oc adm policy add-scc-to-user hostmount-anyuid system:serviceaccount:default:nfs-client-provisioner
5. Modify IP address and export path of NFS server in nfs-provisioner.yaml
6. oc apply -f nfs-provisioner.yaml
7. Modify the storage class name in storageclass.yaml
8. oc apply -f storageclass.yaml

