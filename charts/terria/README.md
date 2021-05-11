terria
======
A Helm chart for terria map

Current chart version is `0.36.1`

Source code can be found [here](https://terria.io/)



## Chart Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| authentication.enabled | bool | `false` |  |
| autoscaling.enabled | bool | `false` |  |
| autoscaling.maxReplicas | int | `100` |  |
| autoscaling.minReplicas | int | `1` |  |
| autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| clientConfig.initializationUrls[0] | string | `"terria"` |  |
| clientConfig.initializationUrls[1] | string | `"metoffice"` |  |
| clientConfig.parameters.appName | string | `"Terria Map"` |  |
| clientConfig.parameters.brandBarElements[0] | string | `""` |  |
| clientConfig.parameters.brandBarElements[1] | string | `"<a target=\"_blank\" href=\"http://terria.io\"><img src=\"images/SI_high.png\" height=\"52\" title=\"Version: {{version}}\" /></a>"` |  |
| clientConfig.parameters.brandBarElements[2] | string | `""` |  |
| clientConfig.parameters.disclaimer.text | string | `"Disclaimer: This map must not be used for navigation or precise spatial analysis"` |  |
| clientConfig.parameters.disclaimer.url | string | `""` |  |
| clientConfig.parameters.experimentalFeatures | bool | `true` |  |
| clientConfig.parameters.googleAnalyticsKey | string | `nil` |  |
| clientConfig.parameters.googleAnalyticsOptions | string | `nil` |  |
| clientConfig.parameters.googleUrlShortenerKey | string | `nil` |  |
| clientConfig.parameters.mobileDefaultViewerMode | string | `"2d"` |  |
| clientConfig.parameters.proj4ServiceBaseUrl | string | `"proj4def/"` |  |
| clientConfig.parameters.supportEmail | string | `"help@example.com"` |  |
| clientConfig.parameters.useCesiumIonBingImagery | bool | `false` |  |
| clientConfig.parameters.useCesiumIonTerrain | bool | `false` |  |
| fullnameOverride | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"satapps/terriamap"` |  |
| image.suffix | string | `"solomon"` |  |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations."kubernetes.io/ingress.class" | string | `"nginx"` |  |
| ingress.annotations."nginx.ingress.kubernetes.io/rewrite-target" | string | `"/$1"` |  |
| ingress.enabled | bool | `true` |  |
| ingress.hosts[0].host | string | `"dev-csvs.sa-catapult.co.uk"` |  |
| ingress.hosts[0].paths[0].path | string | `"/terria-solomon/(.*)"` |  |
| ingress.tls | list | `[]` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| podAnnotations | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| replicaCount | int | `1` |  |
| resources | object | `{}` |  |
| securityContext | object | `{}` |  |
| serverConfig.allowProxyFor[0] | string | `"geoserver:8080"` |  |
| serverConfig.allowProxyFor[1] | string | `"thredds:8080"` |  |
| serverConfig.blacklistedAddresses | list | `[]` |  |
| serverConfig.port | int | `3001` |  |
| serverConfig.proxyAuth.geoserver:8080.authorization | string | `"Basic dGVzdDp0ZXN0"` |  |
| service.port | int | `3001` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `""` |  |
| tolerations | list | `[]` |  |
