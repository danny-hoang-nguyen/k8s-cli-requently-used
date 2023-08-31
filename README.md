# k8s-cli-requently-used
Commands that I need

kubectl get pods all running pods on default namespace will be listed
kubectl get pods | grep $name | awk '{print $1}' search pod name.

kubectl exec -it $pod -- /bin/bash jump into $pod to mess with it.
kubectl port-forward $pod port_local:port_remote forward whatever happening on remote on port_remote to your local machine on port port_local

kubectl get pods $pod_name -o jsonpath='{.spec.containers[*].name}' get containers in pod_name

kubectl describe pods <pod_name> | grep "Namespace" to know which namespace that pod_name belongs to
kubectl rollout restart deployment -n <namespace> <pod_name> restart pod_name
