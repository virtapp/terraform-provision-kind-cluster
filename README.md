# Install Kind and ArgoCD with Terraform
![image](https://user-images.githubusercontent.com/23049337/221380821-54af138c-72aa-4124-bb7a-b01a17c47c1f.png)
# Install prerequisites
 * docker
 * terraform 
 * kubectl 
 


# Connect to ArgoCD

## Get ArgoCD admin password
```bash
$ \
bin/kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d
```
## Connect to ArgoCD
Port forward ArgoCD to http://localhost:8080
```bash
$ \
bin/kubectl port-forward -n argocd service/argocd-server --address 0.0.0.0 8080:80
```

