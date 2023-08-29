## Command Line Resources 

**srcImage:** `docker://containerregistrycs.azurecr.io/cs-api-servicos-online:4231`

**destImage:** `docker://image-registry.openshift-image-registry.svc:5000/<<namespace>>/cs-api-servicos-online:4231`

**GitOps application control permission:** `oc adm policy add-role-to-user admin system:serviceaccount:openshift-gitops:openshift-gitops-argocd-application-controller -n sonda`

**Pipeline permission user policies:** 
---
``` oc adm policy add-role-to-group edit system:serviceaccounts -n cs-qa
    oc adm policy add-role-to-group edit system:serviceaccounts -n cs-homolog
    oc adm policy add-role-to-user system:image-puller system:serviceaccounts:cs-homolog -n cs-qa
    oc adm policy add-role-to-user system:deployer system:serviceaccounts:cs-qa -n cs-homolog
```  