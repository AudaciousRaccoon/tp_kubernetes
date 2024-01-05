download the tp-ingress.yaml and tp-deployment.yaml

start a cluster: minikube start --vm-driver=docker -n 2 -p tpcluster
enable ingress: minikube addons enable ingress -p tpcluster
launch the files: kubectl apply -f tp-deployment.yaml 
				  kubectl apply -f tp-ingress.yaml
				  
wait a few moments for the ingress to be ready. 
get the ingress address:  kubectl get ingress

add the following line in the hosts file :  <ingress ip address> tp.nous

try access the tp.nous site on your browser

enjoy