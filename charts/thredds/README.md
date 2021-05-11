thredds
=======
A Helm chart for Kubernetes

Current chart version is `0.21.2`

Source code can be found [here](https://www.unidata.ucar.edu/software/tds/)



## Chart Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| autoscaling.enabled | bool | `false` |  |
| autoscaling.maxReplicas | int | `100` |  |
| autoscaling.minReplicas | int | `1` |  |
| autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| awsAccessKeyId | string | `"test"` |  |
| awsSecretAccessKey | string | `"test"` |  |
| fullnameOverride | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"unidata/thredds-docker"` |  |
| image.tag | string | `""` |  |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations | object | `{}` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0].host | string | `"chart-example.local"` |  |
| ingress.hosts[0].paths | list | `[]` |  |
| ingress.tls | list | `[]` |  |
| initImage.pullPolicy | string | `"IfNotPresent"` |  |
| initImage.repository | string | `"satapps/init-thredds"` |  |
| initImage.tag | string | `"851fae8"` |  |
| livenessProbe.enabled | bool | `false` |  |
| livenessProbe.failureThreshold | int | `6` |  |
| livenessProbe.initialDelaySeconds | int | `15` |  |
| livenessProbe.periodSeconds | int | `10` |  |
| livenessProbe.successThreshold | int | `1` |  |
| livenessProbe.timeoutSeconds | int | `5` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| podAnnotations | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| pvc.cmapData.name | string | `"cmap-data"` |  |
| pvc.cmapData.namespace | string | `"dev-csvs"` |  |
| pvc.cmapData.storageClassName | string | `"fast"` |  |
| pvc.configuration.name | string | `"thredds"` |  |
| pvc.configuration.namespace | string | `"dev-csvs"` |  |
| pvc.configuration.storageClassName | string | `"fast"` |  |
| pvc.cruData.name | string | `"cru-data"` |  |
| pvc.cruData.namespace | string | `"dev-csvs"` |  |
| pvc.cruData.storageClassName | string | `"fast"` |  |
| pvc.era5LandData.name | string | `"era5-land-data"` |  |
| pvc.era5LandData.namespace | string | `"dev-csvs"` |  |
| pvc.era5LandData.storageClassName | string | `"fast"` |  |
| pvc.gpcpData.name | string | `"gpcp-data"` |  |
| pvc.gpcpData.namespace | string | `"dev-csvs"` |  |
| pvc.gpcpData.storageClassName | string | `"fast"` |  |
| pvc.ncepData.name | string | `"ncep-data"` |  |
| pvc.ncepData.namespace | string | `"dev-csvs"` |  |
| pvc.ncepData.storageClassName | string | `"fast"` |  |
| pvc.netcdfDaily1.name | string | `"era5-data-daily-part-1"` |  |
| pvc.netcdfDaily1.namespace | string | `"dev-csvs"` |  |
| pvc.netcdfDaily1.storageClassName | string | `"fast"` |  |
| pvc.netcdfDaily2.name | string | `"era5-data-daily-part-2"` |  |
| pvc.netcdfDaily2.namespace | string | `"dev-csvs"` |  |
| pvc.netcdfDaily2.storageClassName | string | `"fast"` |  |
| pvc.netcdfDaily3.name | string | `"era5-data-daily-part-3"` |  |
| pvc.netcdfDaily3.namespace | string | `"dev-csvs"` |  |
| pvc.netcdfDaily3.storageClassName | string | `"fast"` |  |
| pvc.netcdfMontlyYearly.name | string | `"era5-data-monthly-yearly"` |  |
| pvc.netcdfMontlyYearly.namespace | string | `"dev-csvs"` |  |
| pvc.netcdfMontlyYearly.storageClassName | string | `"fast"` |  |
| pvc.trmmData.name | string | `"trmm-data"` |  |
| pvc.trmmData.namespace | string | `"dev-csvs"` |  |
| pvc.trmmData.storageClassName | string | `"fast"` |  |
| readinessProbe.enabled | bool | `false` |  |
| readinessProbe.failureThreshold | int | `6` |  |
| readinessProbe.initialDelaySeconds | int | `15` |  |
| readinessProbe.periodSeconds | int | `10` |  |
| readinessProbe.successThreshold | int | `1` |  |
| readinessProbe.timeoutSeconds | int | `5` |  |
| replicaCount | int | `1` |  |
| resources | object | `{}` |  |
| securityContext | object | `{}` |  |
| service.port | int | `8080` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `""` |  |
| sidecar.awsConcurrentRequests | int | `1` |  |
| sidecar.image.pullPolicy | string | `"IfNotPresent"` |  |
| sidecar.image.repository | string | `"satapps/csvs-thredds-sidecar"` |  |
| sidecar.image.tag | string | `"0.14"` |  |
| tolerations | list | `[]` |  |
