terria
======
A Helm chart for terria map

Current chart version is `0.5.3`

Source code can be found [here](https://terria.io/)



## Chart Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| authentication.authData | string | `"foo: $2y$10$mgU3C0jwc/IY168nIM5i7.Cld/y6NZsi6JLCh84i5RacV7pxwPimK\nbaz: $2y$10$mgU3C0jwc/IY168nIM5i7.Cld/y6NZsi6JLCh84i5RacV7pxwPimK\n"` |  |
| authentication.enabled | bool | `true` |  |
| autoscaling.enabled | bool | `false` |  |
| autoscaling.maxReplicas | int | `100` |  |
| autoscaling.minReplicas | int | `1` |  |
| autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| clientConfig.initializationUrls[0] | string | `"terria"` |  |
| clientConfig.parameters.appName | string | `"Terria Map"` |  |
| clientConfig.parameters.brandBarElements[0] | string | `""` |  |
| clientConfig.parameters.brandBarElements[1] | string | `"<a target=\"_blank\" href=\"http://terria.io\"><img src=\"images/terria_logo.png\" height=\"52\" title=\"Version: {{version}}\" /></a>"` |  |
| clientConfig.parameters.brandBarElements[2] | string | `""` |  |
| clientConfig.parameters.cesiumIonAccessToken | string | `"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJqdGkiOiI3ODY5M2VjZi01MGE5LTQwMGYtYmU0Ni1kOGIzNWUxYzZlNzQiLCJpZCI6Mjc1ODksInNjb3BlcyI6WyJhc3IiLCJnYyJdLCJpYXQiOjE1ODk3OTIyMjl9.P7XCpfHLYOnfxZqq89HQrLEMbFe6XzVKwBAjrH68GLs"` |  |
| clientConfig.parameters.disclaimer.text | string | `"Disclaimer: This map must not be used for navigation or precise spatial analysis"` |  |
| clientConfig.parameters.disclaimer.url | string | `""` |  |
| clientConfig.parameters.experimentalFeatures | bool | `true` |  |
| clientConfig.parameters.feedbackUrl | string | `"feedback"` |  |
| clientConfig.parameters.googleAnalyticsKey | string | `nil` |  |
| clientConfig.parameters.googleAnalyticsOptions | string | `nil` |  |
| clientConfig.parameters.googleUrlShortenerKey | string | `nil` |  |
| clientConfig.parameters.mobileDefaultViewerMode | string | `"2d"` |  |
| clientConfig.parameters.proj4ServiceBaseUrl | string | `"proj4def/"` |  |
| clientConfig.parameters.supportEmail | string | `"help@example.com"` |  |
| fullnameOverride | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"satapps/terriamap"` |  |
| image.tag | string | `""` |  |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations."kubernetes.io/ingress.class" | string | `"nginx"` |  |
| ingress.annotations."nginx.ingress.kubernetes.io/rewrite-target" | string | `"/$1"` |  |
| ingress.enabled | bool | `true` |  |
| ingress.hosts[0].host | string | `"dev-csvs.sa-catapult.co.uk"` |  |
| ingress.hosts[0].paths[0].path | string | `"/terria/(.*)"` |  |
| ingress.tls | list | `[]` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| podAnnotations | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| replicaCount | int | `1` |  |
| resources | object | `{}` |  |
| securityContext | object | `{}` |  |
| service.port | int | `3001` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `""` |  |
| tolerations | list | `[]` |  |
