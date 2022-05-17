# metricbeat-kubernetes
It includes kube-state-metrics and metricbeat  K8s manifests.

# step1
First, we need to install kube-state-metrics, a component that is a service that listens to the Kubernetes API and exposes metrics data about the state of each resource object.

kubectl apply -f ./kube-state-metrics/ -n kube-system

# step2
create a new nammspace, name it as "monitoring".

# step3 
pass the elasticsearch credentials to ENV variables in metricbeat.yaml file.

# step4
kubectl apply -f metricbeat.yaml
