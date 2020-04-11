# Minikube Installation On Mac

Minikube is an all-in-one kubernetes that you can install at your local machine to play and learn about Kubernetes. 
[Minikube Documentation](https://kubernetes.io/docs/tasks/tools/install-minikube/)
<br />
## kubectl
Before installing minikube itself, you should install kubectl command line interface (CLI), I had installed minikube to macos via Home Brew: steps<br />

`brew install kubectl`
<br />
after successful install you can start check kubectl below command:<br />
`kubectl version`
<br />
<b>Sample output</b>
```
kubectl version
Client Version: version.Info{Major:"1", Minor:"14", GitVersion:"v1.14.7", GitCommit:"8fca2ec50a6133511b771a11559e24191b1aa2b4", GitTreeState:"clean", BuildDate:"2019-09-18T14:47:22Z", GoVersion:"go1.12.9", Compiler:"gc", Platform:"darwin/amd64"}
```
<br />

## minikube

I had installed minikube to macos via Home Brew and used Vmware Fusion. Minikube installation steps: <br />

`brew install minikube`
<br />
after successful install you can start minikube via below command:<br />
`minikube start --vm-driver=vmware`
<br />
you can set vm-driver as vmware as always on config via command below and can start with only minikube start command after that<br />
`minikube config set vm-driver vmware`
<br />

<b>Sample output</b>

```
minikube start
😄  minikube v1.5.2 on Darwin 10.15
💡  Tip: Use 'minikube start -p <name>' to create a new cluster, or 'minikube delete' to delete this one.
🔄  Starting existing vmware VM for "minikube" ...
⌛  Waiting for the host to be provisioned ...
🐳  Preparing Kubernetes v1.16.2 on Docker '18.09.9' ...
🔄  Relaunching Kubernetes using kubeadm ... 
⌛  Waiting for: apiserver
🏄  Done! kubectl is now configured to use "minikube"
⚠️  /usr/local/bin/kubectl is version 1.14.7, and is incompatible with Kubernetes 1.16.2. You will need to update /usr/local/bin/kubectl or use 'minikube kubectl' to connect with this cluster
```
<br />
You can launch the dashboard via below command:

`minikube dashboard`

<br />
<b>Sample output</b>

```
minikube dashboard
🤔  Verifying dashboard health ...
🚀  Launching proxy ...
🤔  Verifying proxy health ...
🎉  Opening http://127.0.0.1:57377/api/v1/namespaces/kubernetes-dashboard/services/http:kubernetes-dashboard:/proxy/ in your default browser...
```
<br />

It opens <br />
> http://127.0.0.1:57377/api/v1/namespaces/kubernetes-dashboard/services/http:kubernetes-dashboard:/proxy/#/overview?namespace=default

<br />
You can check out the IP for your minikube via command: <br />

`minikube ip`

<br />
<b>Sample output</b>

```
minikube ip
192.168.106.133
```
