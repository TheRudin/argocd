# argocd

The password for the admin user is set to argocd




The mother charts can be excluded by: echo "charts/" > charts/argo-cd/.gitignore

change dependend version ... just change the release numer form the umbrella chart and fire follow thing: helm dep update charts/argo-cd/