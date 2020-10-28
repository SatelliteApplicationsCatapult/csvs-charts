geoserver
=========
A Helm chart for deploying GeoServer

Current chart version is `0.19.10`

Source code can be found [here](http://geoserver.org/)



## Chart Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| awsAccessKeyId | string | `"test"` |  |
| awsSecretAccessKey | string | `"test"` |  |
| backup.enabled | bool | `false` |  |
| backup.namespace | string | `"dev-csvs"` |  |
| backup.pullPolicy | string | `"IfNotPresent"` |  |
| backup.repository | string | `"satapps/geoserver-backup"` |  |
| backup.s3bucket | string | `"csvs-backups"` |  |
| backup.s3url | string | `"http://s3-uk-1.sa-catapult.co.uk"` |  |
| backup.tag | string | `"sha-be266da"` |  |
| backup.ttlSecondsAfterFinished | int | `3600` |  |
| fullnameOverride | string | `""` |  |
| geoserverPassword | string | `"test_password"` |  |
| geoserverUsername | string | `"test_user"` |  |
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
| local.enabled | bool | `false` |  |
| local.hostPath | string | `"/c/Users/Davide.DeLerma/projects/kube_geoserver_dir/"` |  |
| local.storageClassName | string | `"manual"` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| postgres.awsAccessKeyId | string | `"test"` |  |
| postgres.awsSecretAccessKey | string | `"test"` |  |
| postgres.namespace | string | `"dev-csvs"` |  |
| postgres.postgresqlPassword | string | `"supersecret"` |  |
| postgres.postgresqlUsername | string | `"geoserver"` |  |
| postgres.s3bucket | string | `"csvs-backups"` |  |
| postgres.s3url | string | `"http://s3-uk-1.sa-catapult.co.uk"` |  |
| pvc.rasters.enabled | bool | `false` |  |
| pvc.rasters.name | string | `"geoserver-rasters"` |  |
| pvc.remote.name | string | `"geoserver"` |  |
| pvc.remote.namespace | string | `"dev-csvs"` |  |
| pvc.remote.storageClassName | string | `"fast"` |  |
| rbac.create | bool | `true` |  |
| readinessProbe.enabled | bool | `true` |  |
| replicaCount | int | `1` |  |
| resources | object | `{}` |  |
| securityContext | object | `{}` |  |
| service.port | int | `8080` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `nil` |  |
| sidecar.image.pullPolicy | string | `"IfNotPresent"` |  |
| sidecar.image.repository | string | `"satapps/geoserver-commands"` |  |
| sidecar.image.tag | float | `0.7` |  |
| tolerations | list | `[]` |  |
