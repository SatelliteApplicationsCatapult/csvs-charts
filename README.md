helm-geoserver-postgres
=======================

![Version: 0.1.0](https://img.shields.io/badge/Version-0.1.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square)
![](https://github.com/SatelliteApplicationsCatapult/helm-geoserver-postgres/workflows/release/badge.svg)
![Release](https://github.com/SatelliteApplicationsCatapult/helm-geoserver-postgres/workflows/Release/badge.svg)

A Helm chart for Kubernetes

## Usage

1. Install [Helm](https://helm.sh). For more information, see [Helm documentation](https://helm.sh/docs/).

2. Add the helm-geoserver-postgres Helm repository:

```console
$ helm repo add helm-geoserver-postgres https://SatelliteApplicationsCatapult.github.io/helm-geoserver-postgres
$ helm repo update
```

3. View helm-geoserver-postgres Helm charts:

 ```console
 $ helm search helm-geoserver-postgres
 ```



## Chart Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| awsAccessKeyId | string | `"test"` |  |
| awsSecretAccessKey | string | `"test"` |  |
| cronjob.pullPolicy | string | `"IfNotPresent"` |  |
| cronjob.repository | string | `"satapps/geoserver-backup"` |  |
| cronjob.tag | string | `"sha-be266da"` |  |
| fullnameOverride | string | `""` |  |
| geoserverPassword | string | `"geoserver"` |  |
| geoserverUsername | string | `"admin"` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"davidedelerma/geoserver"` |  |
| image.tag | string | `"1.1"` |  |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations | object | `{}` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0].host | string | `"kubernetes.docker.internal"` |  |
| ingress.hosts[0].paths[0].path | string | `"/"` |  |
| ingress.tls | list | `[]` |  |
| livenessProbe.enabled | bool | `true` |  |
| livenessProbe.failureThreshold | int | `6` |  |
| livenessProbe.initialDelaySeconds | int | `60` |  |
| livenessProbe.periodSeconds | int | `10` |  |
| livenessProbe.successThreshold | int | `1` |  |
| livenessProbe.timeoutSeconds | int | `5` |  |
| nameOverride | string | `""` |  |
| namespace | string | `"dev"` |  |
| nodeSelector | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| postgres.awsAccessKeyId | string | `"test"` |  |
| postgres.awsSecretAccessKey | string | `"test"` |  |
| postgres.namespace | string | `"dev"` |  |
| postgres.postgresqlPassword | string | `"supersecret"` |  |
| postgres.postgresqlUsername | string | `"geoserver"` |  |
| postgres.s3bucket | string | `"csvs-backups"` |  |
| postgres.s3url | string | `"http://s3-uk-1.sa-catapult.co.uk"` |  |
| pvc.remote.name | string | `"dev-geoserver-csvs"` |  |
| pvc.remote.namespace | string | `"dev-csvs"` |  |
| pvc.remote.storageClassName | string | `"fast"` |  |
| readinessProbe.enabled | bool | `true` |  |
| replicaCount | int | `1` |  |
| resources | object | `{}` |  |
| s3bucket | string | `"csvs-backups"` |  |
| s3url | string | `"http://s3-uk-1.sa-catapult.co.uk"` |  |
| securityContext | object | `{}` |  |
| service.port | int | `8080` |  |
| service.type | string | `"LoadBalancer"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `nil` |  |
| tolerations | list | `[]` |  |