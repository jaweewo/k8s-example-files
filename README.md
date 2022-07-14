## Comandos de utilidad

### Ejecutar un pod

kubectl run nginx --image=nginx 

# Shell dentro de un pod

kubectl exec --stdin --tty my-pod -- /bin/bash


### Eliminar elementos

kubectl delete pod my-pod

kubectl delete svc my-service

kubectl delete pvc my-pvc

### Comandos de salida simple

kubectl get services                          # Lista todos los servicios del Namespace actual

kubectl get pods --all-namespaces             # Lista todos los pods de todos los namespaces

kubectl get pods -o wide                      # Lista todos los pods del Namespace actual con más detalle

kubectl get deployment my-dep                 # Lista un deployment especifico

kubectl get pods                              # Lista todos los pods del namespace actual

kubectl get pod my-pod -o yaml                # Obtener el YML de un pod

### Comandos para describir elementos 

kubectl describe nodes my-node                # Describe el nodo que indiquemos

kubectl describe pods my-pod                  # Describe el pod que indiquemos

### Listar servicios ordenados por nombre

kubectl get services --sort-by=.metadata.name
