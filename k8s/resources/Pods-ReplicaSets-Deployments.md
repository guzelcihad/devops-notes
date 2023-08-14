- kubectl create -f nginx.yml

- kubectl get events -> shows events in cluster
- kubectl get all -o wide
- kubectl get pods -l run=nginx -> we can find pods created with this labels
- kubectl scale deplıy nginx-deploy --replicas=3
- kubectl -n kube-system get pods -> find clustered pods

# Namespaces and Contexts
> Identify cluster state: kubectl cluster-info
- kubectl get nodes
- kubectl create namespace <>

You can't create duplicate pods in a namespace

- Shows current config -> kubectl config view same as ~/.kube/config, includes cluster configs
- Shows current context -> kubectl config current-context and kubectl config get-contexts

- Creating new context -> kubectl config set-context <context-name> --namespace=kube-system --user=kubernetes-admin --cluster=kubernetes
- Change context -> kubectl config use-context kubesys

- Current context'e bir namespace set etme -> kubectl config set-context --current --namespace=<insert-namespace-name-here>, kubectl config view --minify | grep namespace: