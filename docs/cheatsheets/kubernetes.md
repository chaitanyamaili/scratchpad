# ☸️ Kubernetes Cheat Sheet

A quick reference guide for working with Kubernetes (kubectl, manifests, objects, and tips).

---

## 🛠️ Basics

```bash
kubectl version                     # Show client/server version
kubectl cluster-info                # Show cluster info
kubectl config view                 # Show kubeconfig details
kubectl get nodes                   # List cluster nodes



⸻

📦 Pods

kubectl get pods                    # List all pods
kubectl get pods -n <namespace>    # List pods in a namespace
kubectl describe pod <name>        # Show pod details
kubectl delete pod <name>          # Delete a pod
kubectl logs <pod>                 # View pod logs
kubectl exec -it <pod> -- sh       # Exec into a pod shell



⸻

📂 Namespaces

kubectl get namespaces              # List all namespaces
kubectl create namespace <name>    # Create a new namespace
kubectl delete namespace <name>    # Delete a namespace



⸻

📁 Deployments

kubectl create deployment <name> --image=<image>
kubectl get deployments
kubectl describe deployment <name>
kubectl delete deployment <name>
kubectl scale deployment <name> --replicas=3
kubectl rollout status deployment/<name>
kubectl rollout undo deployment/<name>



⸻

🔄 Services

kubectl expose deployment <name> --port=80 --target-port=8080 --type=NodePort
kubectl get svc
kubectl describe svc <name>
kubectl delete svc <name>



⸻

📜 YAML Manifests

kubectl apply -f <file.yaml>       # Apply manifest
kubectl delete -f <file.yaml>      # Delete using manifest
kubectl get all -o yaml            # Get all resources in YAML
kubectl explain <resource>         # Documentation for resource

Sample Deployment YAML:

apiVersion: apps/v1
kind: Deployment
metadata:
  name: my-app
spec:
  replicas: 2
  selector:
    matchLabels:
      app: my-app
  template:
    metadata:
      labels:
        app: my-app
    spec:
      containers:
        - name: app
          image: nginx
          ports:
            - containerPort: 80



⸻

🎯 Labels & Selectors

kubectl get pods --show-labels
kubectl label pod <pod> env=prod
kubectl get pods -l env=prod
kubectl delete pod -l app=frontend



⸻

🔍 Debug & Troubleshoot

kubectl get events
kubectl describe pod <pod>
kubectl logs <pod> --previous
kubectl top pod                    # Requires metrics-server



⸻

⛵ ConfigMaps & Secrets

kubectl create configmap my-config --from-literal=key=value
kubectl get configmap my-config -o yaml

kubectl create secret generic my-secret --from-literal=password=1234
kubectl get secret my-secret -o yaml



⸻

🔐 RBAC

kubectl create serviceaccount <name>
kubectl create rolebinding <binding> --role=<role> --serviceaccount=<ns>:<account> --namespace=<ns>



⸻

📊 Resource Metrics (via metrics-server)

kubectl top node
kubectl top pod



⸻

🧼 Cleanup

kubectl delete all --all           # Delete all resources in current ns
kubectl delete namespace <name>    # Delete a namespace and its resources



⸻

✅ Pro Tips
	•	Use kubens and kubectx for quick switching (install via krew)
	•	Use -o wide for more detailed outputs
	•	Aliases:

alias k=kubectl
alias kgp='kubectl get pods'
alias kaf='kubectl apply -f'
