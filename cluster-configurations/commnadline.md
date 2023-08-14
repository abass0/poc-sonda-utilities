## Command Line Resources 

**srcImage:** docker://containerregistrycs.azurecr.io/cs-api-servicos-online:4231

**destImage:** docker://image-registry.openshift-image-registry.svc:5000/<<namespace>>/cs-api-servicos-online:4231

**GitOps application control permission:** `oc adm policy add-role-to-user admin system:serviceaccount:openshift-gitops:openshift-gitops-argocd-application-controller -n sonda`

**Pipeline permission bind:**` oc create -f image-puller-bind.yaml -n cs-homolog` 


