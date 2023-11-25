# Farming Front Door Core
Local development support for orchestrating all Farming Front Door microservices.

## Prerequisites

Ensure you have satisfied the prerequisites of all individual repositories.

## Repositories
- [ffc-ffd-gateway](https://github.com/defra/ffc-ffd-gateway)
- [ffc-ffd-landing-page](https://github.com/defra/ffc-ffd-landing-page)
- [ffc-ffd-auth](https://github.com/defra/ffc-ffd-auth)
- [ffc-ffd-business](https://github.com/defra/ffc-ffd-business)
- [ffc-ffd-proxy](https://github.com/defra/ffc-ffd-proxy)
- [ffc-ffd-ingress](https://github.com/defra/ffc-ffd-ingress)

## Scripts

### Clone

Clone all repositories from GitHub.  Repositories will cloned in the parent directory of this repository.

[`./clone`](clone)

### Update

Switch to `main` branch in every repository and pull latest changes with `git pull`.

[`./update`](update)

### Build

Build/rebuild Docker container for all microservices.

[`./build`](build)

### Start

Run all services.

Runs `Seed` script if `ffc-ffd-scripts` repository is cloned.

[`./start`](start)

#### Optional arguments
- `-f` - include Azure Functions
- `-s` - include Statement services
- `-S` - only statement services

### Stop

Run all services.

[`./stop`](stop)

#### Optional arguments

Any valid `docker-compose down` argument.

### Seed

Seed customer mapping data from private repository to `ffc-ffd-business` if `ffc-ffd-scripts` repository is cloned.

[`./seed`](seed)

### Open

Open all services in Visual Studio Code.

[`./open`](open)

#### Optional arguments
- `-f` - include Azure Functions
- `-s` - include Statement services
- `-S` - only statement services

### Latest versions

List latest GitHub release version for each microservice.

[`./latest-versions`](latest-versions)

### Environment versions

List current environment version for each microservice hosted in Kubernetes.

[`./environment-versions`](environment-versions)

#### Options
- `-c | --cluster` - Kubernetes cluster context name
- `-n | --namespace` - Kubernetes namespace

### Resource quota

Determine the Kubernetes resource usage for a namespace based on all microservices running at maximum capacity and scaling.

[`./resource-quota`](resource-quota)
