postgres
========
A Helm chart for Kubernetes

Current chart version is `0.4.3`

Source code can be found [here](https://postgis.net/)



## Chart Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| awsAccessKeyId | string | `"test"` |  |
| awsSecretAccessKey | string | `"test"` |  |
| cronjob.pullPolicy | string | `"IfNotPresent"` |  |
| cronjob.repository | string | `"satapps/postgres-backup"` |  |
| cronjob.tag | string | `"sha-319c345"` |  |
| cronjob.ttlSecondsAfterFinished | int | `3600` |  |
| fullnameOverride | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"mdillon/postgis"` |  |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations | object | `{}` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0].host | string | `"chart-example.local"` |  |
| ingress.hosts[0].paths | list | `[]` |  |
| ingress.tls | list | `[]` |  |
| livenessProbe.enabled | bool | `true` |  |
| livenessProbe.failureThreshold | int | `6` |  |
| livenessProbe.initialDelaySeconds | int | `30` |  |
| livenessProbe.periodSeconds | int | `10` |  |
| livenessProbe.successThreshold | int | `1` |  |
| livenessProbe.timeoutSeconds | int | `5` |  |
| local.enabled | bool | `false` |  |
| nameOverride | string | `""` |  |
| namespace | string | `"dev"` |  |
| nodeSelector | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| postgresqlPassword | string | `"supersecret"` |  |
| postgresqlUsername | string | `"geoserver"` |  |
| pvc.remote.name | string | `"dev-postgres-csvs"` |  |
| replicaCount | int | `1` |  |
| resources | object | `{}` |  |
| s3bucket | string | `"csvs-backups"` |  |
| s3url | string | `"http://s3-uk-1.sa-catapult.co.uk"` |  |
| securityContext | object | `{}` |  |
| service.port | int | `5432` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `nil` |  |
| tolerations | list | `[]` |  |
