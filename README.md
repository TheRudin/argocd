# argocd

The password for the admin user is set to argocd




The mother charts can be excluded by: echo "charts/" > charts/argo-cd/.gitignore

change dependend version ... just change the release numer form the umbrella chart and fire follow thing: helm dep update charts/argo-cd/


install the chart using:

helm install argo-cd charts/argo-cd/



forward the port: kubectl port-forward svc/argo-cd-argocd-server 8080:443


get initial password from argo: kubectl get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d

--->  baQej15OnJIijnfu