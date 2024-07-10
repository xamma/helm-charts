# Helm Chart Repo
In this Repo my Helm Charts for various Apps can be found.  
Using GitHub Pages for hosting them.  

## Charts
1. [KubeS3](https://github.com/xamma/KubeS3)
2. nextcloud-k8s (v1 with MySQL, v2 with MySQL+Redis)
3. knative operator
4. webserver-controller (custom controller)
5. presetter (controller for resourcepresets)
6. OSTicket PHP app rewritten for K8s setups (SaaS)

## Usage
```
helm repo add xammahelm https://xamma.github.io/helm-charts
helm repo update
helm search repo xammahelm
helm install kubes3-release xammahelm/kubes3 -n NAMESPACE --create-namespace
helm install kubes3-release xammahelm/kubes3 --set key=value --namespace my-namespace --version=x.x.x
helm uninstall my-webapp -n my-namespace
helm repo remove REPONAME
```

If a new Chart is added to this Repo: ```helm repo index docs```.  

Other important flags:
```
--versions --devel
```