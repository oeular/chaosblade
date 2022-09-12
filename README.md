# chaosblad-operator

### Using Helm

Alternatively, you may use [Helm](https://helm.sh/docs/intro/quickstart/); which is a package manager for Kubernetes.

Install the Helm repository:

```sh
$> helm repo add chaosblade-operator https://oeular.github.io/chaosblade-operator/
$> helm repo update
```

Then deploy the operator:

```sh
$> helm install chaosblade-operator  chaosblade-operator/chaosblade-operator
```

Verify the operator is running by checking the deployment inside the `default` namespace:
```sh
$> kubectl get po -n default | grep chaosblade
chaosblade-operator-847fdd7596-h9xtg   1/1     Running            0             4m49s
chaosblade-tool-gkrg5                  1/1     Running            0             4m49s
chaosblade-tool-nv96h                  1/1     Running            0             4m49s
chaosblade-tool-pjrzw                  1/1     Running            0             4m49s
chaosblade-tool-z2j9f                  1/1     Running            0             4m49s
```

