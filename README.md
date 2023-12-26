# k8s-controller

Creating custom K8s controller, reference: [kubebuilder](https://book.kubebuilder.io/quick-start)

## Steps

Edit the reconciliation business logic at `pdf-controller/internal/controller/pdfdocument_controller.go`

Edit API definition at `pdf-controller/api/v1/pdfdocument_types.go`

Generate Custom Resource and Custom Resource Definitions files

```
make manifests
```

Install CRDs

```
make install
```

Run the controller

```
make run
```

Apply the Custom Resource

```
k apply -f pdf-controller/config/samples/webapp_v1_pdfdocument.yaml
```
