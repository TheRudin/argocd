# argocd

The password for the admin user is set to argocd




The mother charts can be excluded by: echo "charts/" > charts/argo-cd/.gitignore

change dependend version ... just change the release numer form the umbrella chart and fire follow thing: helm dep update charts/argo-cd/


install the chart using:

helm install argo-cd charts/argo-cd/



forward the port: kubectl port-forward svc/argo-cd-argocd-server 8080:443


get initial password from argo: kubectl get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d

--->  0Qam2dlynRF5djXY
$



CREATE THE CLUSTER:

k3d cluster create theRudinCluster -p "80:80@loadbalancer" --agents 2


get grafana password: S0daVkFRa0xKa2ZpaWhmQXNQQzU2d3UzQ2FvdjdXNkNKZUg1RUxxaA==

kubectl get secret --namespace default grafana -o yaml   

kubectl get secret grafana -o jsonpath="{.data.admin-password}" | base64 --decode ; echo

