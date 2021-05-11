ensoserver
==========
A Helm chart for Kubernetes

Current chart version is `0.1.3`

Source code can be found [here](https://github.com/SatelliteApplicationsCatapult/csvs-enso-server)



## Chart Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| autoscaling.enabled | bool | `false` |  |
| autoscaling.maxReplicas | int | `100` |  |
| autoscaling.minReplicas | int | `1` |  |
| autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| ensoUpdateUrl | string | `"https://psl.noaa.gov/enso/mei/data/meiv2.data"` |  |
| fullnameOverride | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"satapps/csvs-enso-server"` |  |
| image.tag | string | `"latest"` |  |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations | object | `{}` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0].host | string | `"chart-example.local"` |  |
| ingress.hosts[0].paths | list | `[]` |  |
| ingress.tls | list | `[]` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| podAnnotations | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| postgresql.postgresqlDatabase | string | `"ensoserver"` |  |
| postgresql.postgresqlPassword | string | `"supersecret"` |  |
| postgresql.postgresqlUsername | string | `"ensoserver"` |  |
| postgresql.servicePort | int | `5432` |  |
| replicaCount | int | `1` |  |
| resources | object | `{}` |  |
| securityContext | object | `{}` |  |
| service.port | int | `80` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `""` |  |
| tolerations | list | `[]` |  |
| update.apiEntrypoint | string | `"/enso"` |  |
| update.apiMethod | string | `"PUT"` |  |
| update.ttlSecondsAfterFinished | int | `3600` |  |
