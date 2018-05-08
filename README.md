## Swagger UI Kubernetes

This is an example deployment of swagger-ui using kubernetes.

#### Adding externally hosted documentation

Add a new entry in the json array in `deployment.yml` under the `API_URLS` environment variable.
the `name` key is the display name shown in the dropdown of the ui and `url` is the url used to retrieve the documentation.

#### Adding internally hosed documentation

Create a new config map `.yml` file using `local.example.configmap.yml` as an example with the documentation in.
Then create a new volume mount and volume in `deployment.yml` using the `local-example` as an example.

#### Deployment

Run in the root folder

```bash
kubectl apply -f ./
```