# nfs-provisioner
yaml files to install nfs provisioner on OpenShift

Install steps
1. Ensure that the current project is "default"
2. oc project default
3. oc apply -f rbac.yml
4. oc adm policy add-scc-to-user hostmount-anyuid system:serviceaccount:default:nfs-client-provisioner
5. Modify IP address and export path of NFS server in nfs-provisioner.yml
6. oc apply -f nfs-provisioner.yml
7. Modify the storage class name in storageclass.yml
8. oc apply -f storageclass.yml

