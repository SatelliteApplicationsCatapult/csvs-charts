geoserver
=========
A Helm chart for deploying GeoServer

Current chart version is `0.3.0`

Source code can be found [here](http://geoserver.org/)



## Chart Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| awsAccessKeyId | string | `"test"` |  |
| awsSecretAccessKey | string | `"test"` |  |
| cronjob.pullPolicy | string | `"IfNotPresent"` |  |
| cronjob.repository | string | `"satapps/geoserver-backup"` |  |
| cronjob.tag | string | `"sha-be266da"` |  |
| cronjob.ttlSecondsAfterFinished | int | `3600` |  |
| fullnameOverride | string | `""` |  |
| geoserverPassword | string | `"geoserver"` |  |
| geoserverUsername | string | `"admin"` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"davidedelerma/geoserver"` |  |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations."kubernetes.io/ingress.class" | string | `"nginx"` |  |
| ingress.enabled | bool | `true` |  |
| ingress.hosts[0].host | string | `"dev-csvs.sa-catapult.co.uk"` |  |
| ingress.hosts[0].paths[0].path | string | `"/geoserver"` |  |
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
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `nil` |  |
| tolerations | list | `[]` |  |
