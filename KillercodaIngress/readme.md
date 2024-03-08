kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/main/deploy/static/provider/baremetal/deploy.yaml 
kubectl create namespace etkb
kubectl apply -f deployment-apple.yaml
kubectl apply -f deployment-banana.yaml
kubectl apply -f sample-ingress.yaml
kubectl get svc --all-namespaces 
// ingress-nginx   ingress-nginx-controller             NodePort    10.109.237.67   <none>        80:31599/TCP,443:32435/TCP   8m9s
// Sayfada -> Traffic ports = 31599 erişim
// https://1a671e8e-80b9-4ca0-89f2-e13fa32c7764-10-244-0-62-31599.spch.r.killercoda.com/apple prints apple
// https://1a671e8e-80b9-4ca0-89f2-e13fa32c7764-10-244-0-62-31599.spch.r.killercoda.com/banana prints banana
