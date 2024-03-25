# Recopilatorio de Comandos Básicos de Kubernetes

## 🌐 Información General
- `kubectl cluster-info` → Información del cluster.
- `kubectl config view` → Configuración utilizada actualmente en el cluster.

## 📊 Recursos y APIs
- `kubectl api-resources` → Listado de api-resources disponibles, útil para saber qué esquemas puedes usar en tus manifiestos de K8S.
- `kubectl api-versions` → Listado de las versiones de APIs disponibles en tu cluster.

## 📡 Nodos y Clusters
- `kubectl get nodes` → Lista de los nodos del cluster.
- `kubeadm token list` → Listar los tokens.
- `kubeadm join` → Agregar nodo al cluster.

## 📁 Objetos y Entidades
- `kubectl get service` → Lista de los servicios.
- `kubectl get pods` → Lista de los pods.
- `kubectl get deployments` → Lista de deployments.
- `kubectl get namespaces` → Lista de namespaces.
- `kubectl get pods -n prueba` → Lista de los pods del namespace 'prueba'.

## 🛠️ Gestión y Modificaciones
- `kubectl create namespace "NOMBRE_NAMESPACE"` → Crear un namespace nuevo.
- `kubectl get namespace "NOMBRE_NAMESPACE"` → Lista los namespaces disponibles o información de un namespace concreto si se indica su nombre.
- `kubectl create deployment "NOMBRE_DEPLOYMENT"` → Crear un nuevo deployment.
- `kubectl delete deployment "NOMBRE_DEPLOYMENT"` → Eliminar un deployment existente.
- `kubectl rollout status deployment "NOMBRE_DEPLOYMENT"` → Estado de rollout para un deployment.
- `kubectl expose deployment first-deployment --port=80 --type=NodePort` → Exponer un deployment.
- `kubectl delete service hello-world` → Eliminar servicio.
- `kubectl scale --replicas=3 deployment prestashop -n prestashop` → Escalar a 3 replicas un deployment.
- `kubectl create secret generic mysql-pass --from-literal=password=mypassword` → Crear un secret.
- `kubectl apply -f deployment.yaml` → Aplicar el contenido del fichero deployment.yaml.

## 📋 Detalles y Monitoreo
- `kubectl describe pod apache1` → Información detallada del pod 'apache1'.
- `kubectl get events` → Lista eventos recientes.
- `kubectl top pod` → PODs que consumen más recursos.
- `kubectl logs --since=1h "NOMBRE_POD"` → Logs producidos en la última hora para el POD especificado.
- `kubectl top node` → Nodos que consumen más recursos.

## 🔒 Gestión de Nodos
- `kubectl cordon node "NOMBRE_NODO"` → Marca el nodo como “no planificable”.
- `kubectl uncordon node "NOMBRE_NODO"` → Devuelve el nodo a su estado normal.
- `kubectl drain node "NOMBRE_NODO"` → Marca el nodo en estado de mantenimiento.
- `kubectl --namespace=enmilocalfunciona exec -it ubuntu-test bash` → Acceder al pod 'ubuntu-test'.
