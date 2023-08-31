# k8s-cli-requently-used
Commands that I need

1. kubectl get pods all running pods on default namespace will be listed
2. kubectl get pods | grep $name | awk '{print $1}' search pod name.

3. kubectl exec -it $pod -- /bin/bash jump into $pod to mess with it.
4. kubectl port-forward $pod port_local:port_remote forwarding
5. kubectl get pods $pod_name -o jsonpath='{.spec.containers[*].name}' get containers in pod_name

6. kubectl describe pods <pod_name> | grep "Namespace" to know which namespace that pod_name belongs to
7. kubectl rollout restart deployment -n <namespace> <pod_name> restart pod_name
