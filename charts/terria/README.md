terria
======
A Helm chart for terria map

Current chart version is `0.30.2`

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
| initConfig.baseMapName | string | `"Positron (Light)"` |  |
| initConfig.catalog[0].description | string | `"This group contains DRR vector data for Solomon Island"` |  |
| initConfig.catalog[0].name | string | `"DRR"` |  |
| initConfig.catalog[0].type | string | `"wfs-getCapabilities"` |  |
| initConfig.catalog[0].url | string | `"http://geoserver:8080/geoserver/solomon/ows?service=wfs&version=2.0.0&request=GetCapabilities"` |  |
| initConfig.catalog[1].description | string | `"This group contains maps of Hazard for Solomon Island"` |  |
| initConfig.catalog[1].geoserverWorkspace | string | `"solomon_rasters"` |  |
| initConfig.catalog[1].name | string | `"Hazard data"` |  |
| initConfig.catalog[1].type | string | `"wms-getCapabilities"` |  |
| initConfig.catalog[1].url | string | `"http://geoserver:8080/geoserver/solomon_rasters/wms?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[2].description | string | `"This group contains DEMs for Solomon Island provided by University of Portsmouth"` |  |
| initConfig.catalog[2].name | string | `"DEMs"` |  |
| initConfig.catalog[2].type | string | `"wms-getCapabilities"` |  |
| initConfig.catalog[2].url | string | `"http://geoserver:8080/geoserver/solomon_dems/wms?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].isOpen | bool | `false` |  |
| initConfig.catalog[3].items[0].isOpen | bool | `false` |  |
| initConfig.catalog[3].items[0].items[0].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[0].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[0].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1979.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1979-01-01T11:00:00Z&time_end=1979-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[0].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[0].name | string | `"ERA5 daily mean 2mTemp 1979"` |  |
| initConfig.catalog[3].items[0].items[0].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[0].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[0].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1979.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].items[10].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[10].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[10].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1989.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1989-01-01T11:00:00Z&time_end=1989-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[10].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[10].name | string | `"ERA5 daily mean 2mTemp 1989"` |  |
| initConfig.catalog[3].items[0].items[10].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[10].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[10].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1989.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].items[11].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[11].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[11].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1990.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1990-01-01T11:00:00Z&time_end=1990-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[11].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[11].name | string | `"ERA5 daily mean 2mTemp 1990"` |  |
| initConfig.catalog[3].items[0].items[11].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[11].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[11].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1990.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].items[12].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[12].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[12].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1991.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1991-01-01T11:00:00Z&time_end=1991-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[12].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[12].name | string | `"ERA5 daily mean 2mTemp 1991"` |  |
| initConfig.catalog[3].items[0].items[12].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[12].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[12].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1991.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].items[13].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[13].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[13].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1992.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1992-01-01T11:00:00Z&time_end=1992-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[13].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[13].name | string | `"ERA5 daily mean 2mTemp 1992"` |  |
| initConfig.catalog[3].items[0].items[13].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[13].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[13].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1992.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].items[14].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[14].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[14].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1993.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1993-01-01T11:00:00Z&time_end=1993-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[14].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[14].name | string | `"ERA5 daily mean 2mTemp 1993"` |  |
| initConfig.catalog[3].items[0].items[14].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[14].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[14].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1993.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].items[15].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[15].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[15].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1994.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1994-01-01T11:00:00Z&time_end=1994-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[15].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[15].name | string | `"ERA5 daily mean 2mTemp 1994"` |  |
| initConfig.catalog[3].items[0].items[15].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[15].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[15].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1994.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].items[16].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[16].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[16].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1995.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1995-01-01T11:00:00Z&time_end=1995-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[16].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[16].name | string | `"ERA5 daily mean 2mTemp 1995"` |  |
| initConfig.catalog[3].items[0].items[16].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[16].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[16].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1995.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].items[17].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[17].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[17].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1996.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1996-01-01T11:00:00Z&time_end=1996-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[17].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[17].name | string | `"ERA5 daily mean 2mTemp 1996"` |  |
| initConfig.catalog[3].items[0].items[17].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[17].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[17].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1996.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].items[18].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[18].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[18].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1997.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1997-01-01T11:00:00Z&time_end=1997-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[18].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[18].name | string | `"ERA5 daily mean 2mTemp 1997"` |  |
| initConfig.catalog[3].items[0].items[18].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[18].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[18].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1997.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].items[19].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[19].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[19].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1998.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1998-01-01T11:00:00Z&time_end=1998-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[19].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[19].name | string | `"ERA5 daily mean 2mTemp 1998"` |  |
| initConfig.catalog[3].items[0].items[19].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[19].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[19].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1998.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].items[1].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[1].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[1].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1980.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1980-01-01T11:00:00Z&time_end=1980-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[1].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[1].name | string | `"ERA5 daily mean 2mTemp 1980"` |  |
| initConfig.catalog[3].items[0].items[1].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[1].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[1].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1980.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].items[20].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[20].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[20].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1999.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1999-01-01T11:00:00Z&time_end=1999-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[20].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[20].name | string | `"ERA5 daily mean 2mTemp 1999"` |  |
| initConfig.catalog[3].items[0].items[20].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[20].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[20].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1999.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].items[21].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[21].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[21].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_2000.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2000-01-01T11:00:00Z&time_end=2000-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[21].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[21].name | string | `"ERA5 daily mean 2mTemp 2000"` |  |
| initConfig.catalog[3].items[0].items[21].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[21].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[21].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_2000.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].items[22].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[22].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[22].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_2001.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2001-01-01T11:00:00Z&time_end=2001-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[22].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[22].name | string | `"ERA5 daily mean 2mTemp 2001"` |  |
| initConfig.catalog[3].items[0].items[22].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[22].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[22].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_2001.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].items[23].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[23].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[23].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_2002.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2002-01-01T11:00:00Z&time_end=2002-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[23].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[23].name | string | `"ERA5 daily mean 2mTemp 2002"` |  |
| initConfig.catalog[3].items[0].items[23].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[23].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[23].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_2002.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].items[24].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[24].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[24].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_2003.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2003-01-01T11:00:00Z&time_end=2003-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[24].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[24].name | string | `"ERA5 daily mean 2mTemp 2003"` |  |
| initConfig.catalog[3].items[0].items[24].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[24].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[24].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_2003.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].items[25].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[25].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[25].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_2004.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2004-01-01T11:00:00Z&time_end=2004-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[25].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[25].name | string | `"ERA5 daily mean 2mTemp 2004"` |  |
| initConfig.catalog[3].items[0].items[25].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[25].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[25].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_2004.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].items[26].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[26].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[26].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_2005.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2005-01-01T11:00:00Z&time_end=2005-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[26].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[26].name | string | `"ERA5 daily mean 2mTemp 2005"` |  |
| initConfig.catalog[3].items[0].items[26].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[26].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[26].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_2005.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].items[27].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[27].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[27].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_2006.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2006-01-01T11:00:00Z&time_end=2006-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[27].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[27].name | string | `"ERA5 daily mean 2mTemp 2006"` |  |
| initConfig.catalog[3].items[0].items[27].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[27].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[27].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_2006.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].items[28].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[28].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[28].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_2007.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2007-01-01T11:00:00Z&time_end=2007-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[28].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[28].name | string | `"ERA5 daily mean 2mTemp 2007"` |  |
| initConfig.catalog[3].items[0].items[28].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[28].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[28].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_2007.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].items[29].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[29].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[29].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_2008.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2008-01-01T11:00:00Z&time_end=2008-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[29].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[29].name | string | `"ERA5 daily mean 2mTemp 2008"` |  |
| initConfig.catalog[3].items[0].items[29].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[29].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[29].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_2008.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].items[2].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[2].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[2].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1981.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1981-01-01T11:00:00Z&time_end=1981-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[2].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[2].name | string | `"ERA5 daily mean 2mTemp 1981"` |  |
| initConfig.catalog[3].items[0].items[2].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[2].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[2].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1981.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].items[30].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[30].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[30].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_2009.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2009-01-01T11:00:00Z&time_end=2009-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[30].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[30].name | string | `"ERA5 daily mean 2mTemp 2009"` |  |
| initConfig.catalog[3].items[0].items[30].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[30].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[30].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_2009.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].items[31].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[31].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[31].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_2010.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2010-01-01T11:00:00Z&time_end=2010-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[31].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[31].name | string | `"ERA5 daily mean 2mTemp 2010"` |  |
| initConfig.catalog[3].items[0].items[31].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[31].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[31].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_2010.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].items[32].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[32].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[32].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_2011.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2011-01-01T11:00:00Z&time_end=2011-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[32].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[32].name | string | `"ERA5 daily mean 2mTemp 2011"` |  |
| initConfig.catalog[3].items[0].items[32].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[32].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[32].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_2011.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].items[33].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[33].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[33].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_2012.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2012-01-01T11:00:00Z&time_end=2012-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[33].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[33].name | string | `"ERA5 daily mean 2mTemp 2012"` |  |
| initConfig.catalog[3].items[0].items[33].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[33].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[33].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_2012.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].items[34].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[34].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[34].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_2013.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2013-01-01T11:00:00Z&time_end=2013-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[34].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[34].name | string | `"ERA5 daily mean 2mTemp 2013"` |  |
| initConfig.catalog[3].items[0].items[34].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[34].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[34].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_2013.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].items[35].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[35].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[35].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_2014.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2014-01-01T11:00:00Z&time_end=2014-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[35].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[35].name | string | `"ERA5 daily mean 2mTemp 2014"` |  |
| initConfig.catalog[3].items[0].items[35].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[35].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[35].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_2014.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].items[36].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[36].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[36].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_2015.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2015-01-01T11:00:00Z&time_end=2015-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[36].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[36].name | string | `"ERA5 daily mean 2mTemp 2015"` |  |
| initConfig.catalog[3].items[0].items[36].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[36].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[36].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_2015.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].items[37].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[37].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[37].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_2016.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2016-01-01T11:00:00Z&time_end=2016-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[37].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[37].name | string | `"ERA5 daily mean 2mTemp 2016"` |  |
| initConfig.catalog[3].items[0].items[37].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[37].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[37].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_2016.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].items[38].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[38].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[38].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_2017.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2017-01-01T11:00:00Z&time_end=2017-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[38].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[38].name | string | `"ERA5 daily mean 2mTemp 2017"` |  |
| initConfig.catalog[3].items[0].items[38].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[38].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[38].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_2017.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].items[39].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[39].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[39].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_2018.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2018-01-01T11:00:00Z&time_end=2018-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[39].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[39].name | string | `"ERA5 daily mean 2mTemp 2018"` |  |
| initConfig.catalog[3].items[0].items[39].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[39].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[39].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_2018.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].items[3].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[3].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[3].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1982.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1982-01-01T11:00:00Z&time_end=1982-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[3].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[3].name | string | `"ERA5 daily mean 2mTemp 1982"` |  |
| initConfig.catalog[3].items[0].items[3].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[3].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[3].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1982.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].items[40].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[40].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[40].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_2019.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2019-01-01T11:00:00Z&time_end=2019-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[40].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[40].name | string | `"ERA5 daily mean 2mTemp 2019"` |  |
| initConfig.catalog[3].items[0].items[40].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[40].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[40].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_2019.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].items[4].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[4].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[4].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1983.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1983-01-01T11:00:00Z&time_end=1983-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[4].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[4].name | string | `"ERA5 daily mean 2mTemp 1983"` |  |
| initConfig.catalog[3].items[0].items[4].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[4].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[4].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1983.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].items[5].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[5].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[5].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1984.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1984-01-01T11:00:00Z&time_end=1984-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[5].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[5].name | string | `"ERA5 daily mean 2mTemp 1984"` |  |
| initConfig.catalog[3].items[0].items[5].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[5].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[5].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1984.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].items[6].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[6].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[6].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1985.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1985-01-01T11:00:00Z&time_end=1985-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[6].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[6].name | string | `"ERA5 daily mean 2mTemp 1985"` |  |
| initConfig.catalog[3].items[0].items[6].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[6].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[6].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1985.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].items[7].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[7].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[7].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1986.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1986-01-01T11:00:00Z&time_end=1986-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[7].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[7].name | string | `"ERA5 daily mean 2mTemp 1986"` |  |
| initConfig.catalog[3].items[0].items[7].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[7].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[7].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1986.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].items[8].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[8].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[8].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1987.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1987-01-01T11:00:00Z&time_end=1987-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[8].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[8].name | string | `"ERA5 daily mean 2mTemp 1987"` |  |
| initConfig.catalog[3].items[0].items[8].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[8].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[8].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1987.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].items[9].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[0].items[9].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[0].items[9].featureInfoTemplate | string | `"<p>ERA5 daily mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1988.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1988-01-01T11:00:00Z&time_end=1988-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[0].items[9].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[0].items[9].name | string | `"ERA5 daily mean 2mTemp 1988"` |  |
| initConfig.catalog[3].items[0].items[9].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[0].items[9].type | string | `"wms"` |  |
| initConfig.catalog[3].items[0].items[9].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_2mTemp/ERA5_daily_mean_2mTemp_1988.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[0].name | string | `"ERA5 daily mean 2mTemp"` |  |
| initConfig.catalog[3].items[0].preserveOrder | bool | `true` |  |
| initConfig.catalog[3].items[0].type | string | `"group"` |  |
| initConfig.catalog[3].items[1].isOpen | bool | `false` |  |
| initConfig.catalog[3].items[1].items[0].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[0].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[0].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1979.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1979-01-01T11:00:00Z&time_end=1979-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[0].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[0].name | string | `"ERA5 daily mean RH 1979"` |  |
| initConfig.catalog[3].items[1].items[0].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[0].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[0].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1979.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].items[10].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[10].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[10].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1989.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1989-01-01T11:00:00Z&time_end=1989-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[10].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[10].name | string | `"ERA5 daily mean RH 1989"` |  |
| initConfig.catalog[3].items[1].items[10].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[10].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[10].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1989.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].items[11].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[11].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[11].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1990.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1990-01-01T11:00:00Z&time_end=1990-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[11].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[11].name | string | `"ERA5 daily mean RH 1990"` |  |
| initConfig.catalog[3].items[1].items[11].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[11].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[11].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1990.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].items[12].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[12].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[12].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1991.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1991-01-01T11:00:00Z&time_end=1991-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[12].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[12].name | string | `"ERA5 daily mean RH 1991"` |  |
| initConfig.catalog[3].items[1].items[12].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[12].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[12].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1991.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].items[13].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[13].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[13].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1992.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1992-01-01T11:00:00Z&time_end=1992-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[13].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[13].name | string | `"ERA5 daily mean RH 1992"` |  |
| initConfig.catalog[3].items[1].items[13].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[13].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[13].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1992.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].items[14].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[14].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[14].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1993.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1993-01-01T11:00:00Z&time_end=1993-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[14].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[14].name | string | `"ERA5 daily mean RH 1993"` |  |
| initConfig.catalog[3].items[1].items[14].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[14].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[14].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1993.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].items[15].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[15].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[15].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1994.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1994-01-01T11:00:00Z&time_end=1994-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[15].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[15].name | string | `"ERA5 daily mean RH 1994"` |  |
| initConfig.catalog[3].items[1].items[15].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[15].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[15].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1994.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].items[16].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[16].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[16].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1995.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1995-01-01T11:00:00Z&time_end=1995-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[16].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[16].name | string | `"ERA5 daily mean RH 1995"` |  |
| initConfig.catalog[3].items[1].items[16].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[16].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[16].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1995.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].items[17].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[17].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[17].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1996.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1996-01-01T11:00:00Z&time_end=1996-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[17].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[17].name | string | `"ERA5 daily mean RH 1996"` |  |
| initConfig.catalog[3].items[1].items[17].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[17].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[17].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1996.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].items[18].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[18].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[18].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1997.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1997-01-01T11:00:00Z&time_end=1997-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[18].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[18].name | string | `"ERA5 daily mean RH 1997"` |  |
| initConfig.catalog[3].items[1].items[18].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[18].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[18].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1997.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].items[19].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[19].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[19].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1998.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1998-01-01T11:00:00Z&time_end=1998-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[19].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[19].name | string | `"ERA5 daily mean RH 1998"` |  |
| initConfig.catalog[3].items[1].items[19].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[19].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[19].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1998.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].items[1].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[1].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[1].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1980.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1980-01-01T11:00:00Z&time_end=1980-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[1].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[1].name | string | `"ERA5 daily mean RH 1980"` |  |
| initConfig.catalog[3].items[1].items[1].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[1].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[1].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1980.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].items[20].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[20].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[20].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1999.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1999-01-01T11:00:00Z&time_end=1999-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[20].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[20].name | string | `"ERA5 daily mean RH 1999"` |  |
| initConfig.catalog[3].items[1].items[20].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[20].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[20].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1999.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].items[21].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[21].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[21].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_2000.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2000-01-01T11:00:00Z&time_end=2000-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[21].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[21].name | string | `"ERA5 daily mean RH 2000"` |  |
| initConfig.catalog[3].items[1].items[21].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[21].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[21].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_2000.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].items[22].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[22].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[22].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_2001.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2001-01-01T11:00:00Z&time_end=2001-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[22].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[22].name | string | `"ERA5 daily mean RH 2001"` |  |
| initConfig.catalog[3].items[1].items[22].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[22].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[22].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_2001.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].items[23].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[23].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[23].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_2002.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2002-01-01T11:00:00Z&time_end=2002-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[23].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[23].name | string | `"ERA5 daily mean RH 2002"` |  |
| initConfig.catalog[3].items[1].items[23].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[23].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[23].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_2002.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].items[24].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[24].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[24].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_2003.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2003-01-01T11:00:00Z&time_end=2003-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[24].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[24].name | string | `"ERA5 daily mean RH 2003"` |  |
| initConfig.catalog[3].items[1].items[24].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[24].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[24].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_2003.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].items[25].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[25].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[25].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_2004.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2004-01-01T11:00:00Z&time_end=2004-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[25].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[25].name | string | `"ERA5 daily mean RH 2004"` |  |
| initConfig.catalog[3].items[1].items[25].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[25].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[25].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_2004.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].items[26].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[26].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[26].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_2005.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2005-01-01T11:00:00Z&time_end=2005-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[26].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[26].name | string | `"ERA5 daily mean RH 2005"` |  |
| initConfig.catalog[3].items[1].items[26].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[26].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[26].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_2005.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].items[27].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[27].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[27].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_2006.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2006-01-01T11:00:00Z&time_end=2006-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[27].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[27].name | string | `"ERA5 daily mean RH 2006"` |  |
| initConfig.catalog[3].items[1].items[27].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[27].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[27].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_2006.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].items[28].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[28].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[28].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_2007.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2007-01-01T11:00:00Z&time_end=2007-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[28].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[28].name | string | `"ERA5 daily mean RH 2007"` |  |
| initConfig.catalog[3].items[1].items[28].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[28].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[28].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_2007.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].items[29].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[29].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[29].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_2008.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2008-01-01T11:00:00Z&time_end=2008-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[29].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[29].name | string | `"ERA5 daily mean RH 2008"` |  |
| initConfig.catalog[3].items[1].items[29].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[29].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[29].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_2008.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].items[2].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[2].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[2].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1981.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1981-01-01T11:00:00Z&time_end=1981-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[2].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[2].name | string | `"ERA5 daily mean RH 1981"` |  |
| initConfig.catalog[3].items[1].items[2].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[2].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[2].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1981.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].items[30].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[30].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[30].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_2009.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2009-01-01T11:00:00Z&time_end=2009-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[30].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[30].name | string | `"ERA5 daily mean RH 2009"` |  |
| initConfig.catalog[3].items[1].items[30].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[30].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[30].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_2009.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].items[31].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[31].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[31].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_2010.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2010-01-01T11:00:00Z&time_end=2010-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[31].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[31].name | string | `"ERA5 daily mean RH 2010"` |  |
| initConfig.catalog[3].items[1].items[31].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[31].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[31].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_2010.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].items[32].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[32].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[32].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_2011.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2011-01-01T11:00:00Z&time_end=2011-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[32].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[32].name | string | `"ERA5 daily mean RH 2011"` |  |
| initConfig.catalog[3].items[1].items[32].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[32].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[32].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_2011.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].items[33].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[33].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[33].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_2012.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2012-01-01T11:00:00Z&time_end=2012-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[33].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[33].name | string | `"ERA5 daily mean RH 2012"` |  |
| initConfig.catalog[3].items[1].items[33].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[33].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[33].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_2012.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].items[34].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[34].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[34].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_2013.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2013-01-01T11:00:00Z&time_end=2013-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[34].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[34].name | string | `"ERA5 daily mean RH 2013"` |  |
| initConfig.catalog[3].items[1].items[34].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[34].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[34].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_2013.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].items[35].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[35].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[35].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_2014.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2014-01-01T11:00:00Z&time_end=2014-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[35].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[35].name | string | `"ERA5 daily mean RH 2014"` |  |
| initConfig.catalog[3].items[1].items[35].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[35].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[35].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_2014.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].items[36].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[36].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[36].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_2015.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2015-01-01T11:00:00Z&time_end=2015-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[36].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[36].name | string | `"ERA5 daily mean RH 2015"` |  |
| initConfig.catalog[3].items[1].items[36].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[36].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[36].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_2015.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].items[37].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[37].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[37].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_2016.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2016-01-01T11:00:00Z&time_end=2016-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[37].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[37].name | string | `"ERA5 daily mean RH 2016"` |  |
| initConfig.catalog[3].items[1].items[37].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[37].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[37].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_2016.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].items[38].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[38].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[38].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_2017.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2017-01-01T11:00:00Z&time_end=2017-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[38].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[38].name | string | `"ERA5 daily mean RH 2017"` |  |
| initConfig.catalog[3].items[1].items[38].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[38].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[38].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_2017.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].items[39].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[39].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[39].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_2018.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2018-01-01T11:00:00Z&time_end=2018-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[39].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[39].name | string | `"ERA5 daily mean RH 2018"` |  |
| initConfig.catalog[3].items[1].items[39].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[39].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[39].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_2018.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].items[3].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[3].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[3].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1982.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1982-01-01T11:00:00Z&time_end=1982-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[3].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[3].name | string | `"ERA5 daily mean RH 1982"` |  |
| initConfig.catalog[3].items[1].items[3].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[3].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[3].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1982.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].items[40].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[40].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[40].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_2019.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2019-01-01T11:00:00Z&time_end=2019-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[40].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[40].name | string | `"ERA5 daily mean RH 2019"` |  |
| initConfig.catalog[3].items[1].items[40].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[40].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[40].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_2019.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].items[4].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[4].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[4].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1983.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1983-01-01T11:00:00Z&time_end=1983-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[4].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[4].name | string | `"ERA5 daily mean RH 1983"` |  |
| initConfig.catalog[3].items[1].items[4].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[4].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[4].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1983.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].items[5].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[5].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[5].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1984.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1984-01-01T11:00:00Z&time_end=1984-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[5].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[5].name | string | `"ERA5 daily mean RH 1984"` |  |
| initConfig.catalog[3].items[1].items[5].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[5].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[5].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1984.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].items[6].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[6].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[6].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1985.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1985-01-01T11:00:00Z&time_end=1985-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[6].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[6].name | string | `"ERA5 daily mean RH 1985"` |  |
| initConfig.catalog[3].items[1].items[6].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[6].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[6].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1985.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].items[7].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[7].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[7].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1986.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1986-01-01T11:00:00Z&time_end=1986-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[7].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[7].name | string | `"ERA5 daily mean RH 1986"` |  |
| initConfig.catalog[3].items[1].items[7].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[7].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[7].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1986.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].items[8].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[8].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[8].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1987.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1987-01-01T11:00:00Z&time_end=1987-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[8].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[8].name | string | `"ERA5 daily mean RH 1987"` |  |
| initConfig.catalog[3].items[1].items[8].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[8].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[8].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1987.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].items[9].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[3].items[1].items[9].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[1].items[9].featureInfoTemplate | string | `"<p>ERA5 daily mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1988.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1988-01-01T11:00:00Z&time_end=1988-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[1].items[9].layers | string | `"t2m"` |  |
| initConfig.catalog[3].items[1].items[9].name | string | `"ERA5 daily mean RH 1988"` |  |
| initConfig.catalog[3].items[1].items[9].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[1].items[9].type | string | `"wms"` |  |
| initConfig.catalog[3].items[1].items[9].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_RH/ERA5_daily_mean_RH_1988.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[1].name | string | `"ERA5 daily mean RH"` |  |
| initConfig.catalog[3].items[1].preserveOrder | bool | `true` |  |
| initConfig.catalog[3].items[1].type | string | `"group"` |  |
| initConfig.catalog[3].items[2].isOpen | bool | `false` |  |
| initConfig.catalog[3].items[2].items[0].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[0].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[0].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1979.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1979-01-01T11:00:00Z&time_end=1979-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[0].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[0].name | string | `"ERA5 daily mean TotalWind 1979"` |  |
| initConfig.catalog[3].items[2].items[0].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[0].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[0].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1979.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].items[10].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[10].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[10].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1989.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1989-01-01T11:00:00Z&time_end=1989-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[10].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[10].name | string | `"ERA5 daily mean TotalWind 1989"` |  |
| initConfig.catalog[3].items[2].items[10].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[10].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[10].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1989.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].items[11].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[11].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[11].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1990.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1990-01-01T11:00:00Z&time_end=1990-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[11].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[11].name | string | `"ERA5 daily mean TotalWind 1990"` |  |
| initConfig.catalog[3].items[2].items[11].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[11].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[11].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1990.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].items[12].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[12].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[12].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1991.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1991-01-01T11:00:00Z&time_end=1991-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[12].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[12].name | string | `"ERA5 daily mean TotalWind 1991"` |  |
| initConfig.catalog[3].items[2].items[12].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[12].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[12].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1991.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].items[13].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[13].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[13].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1992.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1992-01-01T11:00:00Z&time_end=1992-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[13].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[13].name | string | `"ERA5 daily mean TotalWind 1992"` |  |
| initConfig.catalog[3].items[2].items[13].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[13].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[13].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1992.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].items[14].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[14].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[14].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1993.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1993-01-01T11:00:00Z&time_end=1993-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[14].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[14].name | string | `"ERA5 daily mean TotalWind 1993"` |  |
| initConfig.catalog[3].items[2].items[14].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[14].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[14].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1993.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].items[15].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[15].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[15].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1994.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1994-01-01T11:00:00Z&time_end=1994-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[15].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[15].name | string | `"ERA5 daily mean TotalWind 1994"` |  |
| initConfig.catalog[3].items[2].items[15].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[15].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[15].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1994.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].items[16].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[16].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[16].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1995.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1995-01-01T11:00:00Z&time_end=1995-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[16].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[16].name | string | `"ERA5 daily mean TotalWind 1995"` |  |
| initConfig.catalog[3].items[2].items[16].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[16].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[16].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1995.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].items[17].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[17].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[17].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1996.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1996-01-01T11:00:00Z&time_end=1996-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[17].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[17].name | string | `"ERA5 daily mean TotalWind 1996"` |  |
| initConfig.catalog[3].items[2].items[17].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[17].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[17].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1996.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].items[18].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[18].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[18].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1997.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1997-01-01T11:00:00Z&time_end=1997-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[18].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[18].name | string | `"ERA5 daily mean TotalWind 1997"` |  |
| initConfig.catalog[3].items[2].items[18].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[18].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[18].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1997.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].items[19].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[19].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[19].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1998.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1998-01-01T11:00:00Z&time_end=1998-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[19].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[19].name | string | `"ERA5 daily mean TotalWind 1998"` |  |
| initConfig.catalog[3].items[2].items[19].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[19].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[19].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1998.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].items[1].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[1].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[1].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1980.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1980-01-01T11:00:00Z&time_end=1980-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[1].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[1].name | string | `"ERA5 daily mean TotalWind 1980"` |  |
| initConfig.catalog[3].items[2].items[1].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[1].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[1].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1980.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].items[20].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[20].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[20].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1999.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1999-01-01T11:00:00Z&time_end=1999-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[20].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[20].name | string | `"ERA5 daily mean TotalWind 1999"` |  |
| initConfig.catalog[3].items[2].items[20].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[20].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[20].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1999.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].items[21].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[21].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[21].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_2000.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2000-01-01T11:00:00Z&time_end=2000-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[21].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[21].name | string | `"ERA5 daily mean TotalWind 2000"` |  |
| initConfig.catalog[3].items[2].items[21].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[21].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[21].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_2000.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].items[22].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[22].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[22].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_2001.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2001-01-01T11:00:00Z&time_end=2001-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[22].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[22].name | string | `"ERA5 daily mean TotalWind 2001"` |  |
| initConfig.catalog[3].items[2].items[22].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[22].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[22].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_2001.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].items[23].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[23].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[23].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_2002.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2002-01-01T11:00:00Z&time_end=2002-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[23].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[23].name | string | `"ERA5 daily mean TotalWind 2002"` |  |
| initConfig.catalog[3].items[2].items[23].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[23].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[23].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_2002.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].items[24].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[24].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[24].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_2003.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2003-01-01T11:00:00Z&time_end=2003-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[24].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[24].name | string | `"ERA5 daily mean TotalWind 2003"` |  |
| initConfig.catalog[3].items[2].items[24].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[24].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[24].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_2003.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].items[25].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[25].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[25].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_2004.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2004-01-01T11:00:00Z&time_end=2004-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[25].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[25].name | string | `"ERA5 daily mean TotalWind 2004"` |  |
| initConfig.catalog[3].items[2].items[25].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[25].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[25].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_2004.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].items[26].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[26].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[26].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_2005.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2005-01-01T11:00:00Z&time_end=2005-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[26].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[26].name | string | `"ERA5 daily mean TotalWind 2005"` |  |
| initConfig.catalog[3].items[2].items[26].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[26].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[26].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_2005.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].items[27].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[27].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[27].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_2006.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2006-01-01T11:00:00Z&time_end=2006-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[27].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[27].name | string | `"ERA5 daily mean TotalWind 2006"` |  |
| initConfig.catalog[3].items[2].items[27].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[27].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[27].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_2006.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].items[28].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[28].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[28].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_2007.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2007-01-01T11:00:00Z&time_end=2007-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[28].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[28].name | string | `"ERA5 daily mean TotalWind 2007"` |  |
| initConfig.catalog[3].items[2].items[28].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[28].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[28].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_2007.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].items[29].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[29].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[29].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_2008.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2008-01-01T11:00:00Z&time_end=2008-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[29].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[29].name | string | `"ERA5 daily mean TotalWind 2008"` |  |
| initConfig.catalog[3].items[2].items[29].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[29].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[29].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_2008.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].items[2].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[2].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[2].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1981.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1981-01-01T11:00:00Z&time_end=1981-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[2].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[2].name | string | `"ERA5 daily mean TotalWind 1981"` |  |
| initConfig.catalog[3].items[2].items[2].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[2].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[2].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1981.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].items[30].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[30].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[30].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_2009.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2009-01-01T11:00:00Z&time_end=2009-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[30].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[30].name | string | `"ERA5 daily mean TotalWind 2009"` |  |
| initConfig.catalog[3].items[2].items[30].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[30].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[30].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_2009.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].items[31].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[31].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[31].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_2010.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2010-01-01T11:00:00Z&time_end=2010-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[31].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[31].name | string | `"ERA5 daily mean TotalWind 2010"` |  |
| initConfig.catalog[3].items[2].items[31].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[31].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[31].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_2010.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].items[32].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[32].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[32].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_2011.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2011-01-01T11:00:00Z&time_end=2011-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[32].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[32].name | string | `"ERA5 daily mean TotalWind 2011"` |  |
| initConfig.catalog[3].items[2].items[32].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[32].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[32].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_2011.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].items[33].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[33].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[33].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_2012.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2012-01-01T11:00:00Z&time_end=2012-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[33].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[33].name | string | `"ERA5 daily mean TotalWind 2012"` |  |
| initConfig.catalog[3].items[2].items[33].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[33].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[33].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_2012.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].items[34].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[34].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[34].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_2013.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2013-01-01T11:00:00Z&time_end=2013-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[34].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[34].name | string | `"ERA5 daily mean TotalWind 2013"` |  |
| initConfig.catalog[3].items[2].items[34].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[34].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[34].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_2013.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].items[35].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[35].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[35].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_2014.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2014-01-01T11:00:00Z&time_end=2014-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[35].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[35].name | string | `"ERA5 daily mean TotalWind 2014"` |  |
| initConfig.catalog[3].items[2].items[35].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[35].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[35].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_2014.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].items[36].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[36].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[36].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_2015.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2015-01-01T11:00:00Z&time_end=2015-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[36].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[36].name | string | `"ERA5 daily mean TotalWind 2015"` |  |
| initConfig.catalog[3].items[2].items[36].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[36].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[36].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_2015.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].items[37].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[37].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[37].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_2016.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2016-01-01T11:00:00Z&time_end=2016-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[37].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[37].name | string | `"ERA5 daily mean TotalWind 2016"` |  |
| initConfig.catalog[3].items[2].items[37].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[37].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[37].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_2016.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].items[38].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[38].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[38].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_2017.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2017-01-01T11:00:00Z&time_end=2017-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[38].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[38].name | string | `"ERA5 daily mean TotalWind 2017"` |  |
| initConfig.catalog[3].items[2].items[38].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[38].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[38].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_2017.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].items[39].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[39].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[39].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_2018.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2018-01-01T11:00:00Z&time_end=2018-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[39].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[39].name | string | `"ERA5 daily mean TotalWind 2018"` |  |
| initConfig.catalog[3].items[2].items[39].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[39].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[39].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_2018.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].items[3].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[3].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[3].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1982.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1982-01-01T11:00:00Z&time_end=1982-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[3].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[3].name | string | `"ERA5 daily mean TotalWind 1982"` |  |
| initConfig.catalog[3].items[2].items[3].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[3].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[3].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1982.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].items[40].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[40].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[40].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_2019.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2019-01-01T11:00:00Z&time_end=2019-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[40].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[40].name | string | `"ERA5 daily mean TotalWind 2019"` |  |
| initConfig.catalog[3].items[2].items[40].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[40].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[40].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_2019.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].items[4].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[4].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[4].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1983.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1983-01-01T11:00:00Z&time_end=1983-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[4].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[4].name | string | `"ERA5 daily mean TotalWind 1983"` |  |
| initConfig.catalog[3].items[2].items[4].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[4].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[4].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1983.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].items[5].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[5].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[5].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1984.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1984-01-01T11:00:00Z&time_end=1984-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[5].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[5].name | string | `"ERA5 daily mean TotalWind 1984"` |  |
| initConfig.catalog[3].items[2].items[5].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[5].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[5].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1984.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].items[6].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[6].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[6].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1985.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1985-01-01T11:00:00Z&time_end=1985-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[6].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[6].name | string | `"ERA5 daily mean TotalWind 1985"` |  |
| initConfig.catalog[3].items[2].items[6].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[6].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[6].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1985.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].items[7].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[7].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[7].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1986.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1986-01-01T11:00:00Z&time_end=1986-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[7].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[7].name | string | `"ERA5 daily mean TotalWind 1986"` |  |
| initConfig.catalog[3].items[2].items[7].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[7].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[7].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1986.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].items[8].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[8].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[8].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1987.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1987-01-01T11:00:00Z&time_end=1987-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[8].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[8].name | string | `"ERA5 daily mean TotalWind 1987"` |  |
| initConfig.catalog[3].items[2].items[8].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[8].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[8].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1987.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].items[9].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[3].items[2].items[9].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[2].items[9].featureInfoTemplate | string | `"<p>ERA5 daily mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1988.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1988-01-01T11:00:00Z&time_end=1988-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[2].items[9].layers | string | `"u10"` |  |
| initConfig.catalog[3].items[2].items[9].name | string | `"ERA5 daily mean TotalWind 1988"` |  |
| initConfig.catalog[3].items[2].items[9].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[3].items[2].items[9].type | string | `"wms"` |  |
| initConfig.catalog[3].items[2].items[9].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_TotalWind/ERA5_daily_mean_TotalWind_1988.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[2].name | string | `"ERA5 daily mean TotalWind"` |  |
| initConfig.catalog[3].items[2].preserveOrder | bool | `true` |  |
| initConfig.catalog[3].items[2].type | string | `"group"` |  |
| initConfig.catalog[3].items[3].isOpen | bool | `false` |  |
| initConfig.catalog[3].items[3].items[0].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[0].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[0].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1979.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1979-01-01T11:00:00Z&time_end=1979-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[0].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[0].name | string | `"ERA5 daily mean mslp 1979"` |  |
| initConfig.catalog[3].items[3].items[0].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[0].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[0].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1979.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].items[10].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[10].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[10].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1989.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1989-01-01T11:00:00Z&time_end=1989-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[10].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[10].name | string | `"ERA5 daily mean mslp 1989"` |  |
| initConfig.catalog[3].items[3].items[10].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[10].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[10].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1989.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].items[11].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[11].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[11].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1990.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1990-01-01T11:00:00Z&time_end=1990-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[11].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[11].name | string | `"ERA5 daily mean mslp 1990"` |  |
| initConfig.catalog[3].items[3].items[11].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[11].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[11].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1990.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].items[12].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[12].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[12].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1991.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1991-01-01T11:00:00Z&time_end=1991-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[12].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[12].name | string | `"ERA5 daily mean mslp 1991"` |  |
| initConfig.catalog[3].items[3].items[12].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[12].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[12].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1991.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].items[13].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[13].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[13].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1992.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1992-01-01T11:00:00Z&time_end=1992-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[13].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[13].name | string | `"ERA5 daily mean mslp 1992"` |  |
| initConfig.catalog[3].items[3].items[13].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[13].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[13].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1992.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].items[14].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[14].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[14].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1993.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1993-01-01T11:00:00Z&time_end=1993-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[14].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[14].name | string | `"ERA5 daily mean mslp 1993"` |  |
| initConfig.catalog[3].items[3].items[14].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[14].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[14].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1993.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].items[15].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[15].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[15].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1994.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1994-01-01T11:00:00Z&time_end=1994-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[15].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[15].name | string | `"ERA5 daily mean mslp 1994"` |  |
| initConfig.catalog[3].items[3].items[15].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[15].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[15].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1994.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].items[16].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[16].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[16].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1995.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1995-01-01T11:00:00Z&time_end=1995-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[16].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[16].name | string | `"ERA5 daily mean mslp 1995"` |  |
| initConfig.catalog[3].items[3].items[16].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[16].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[16].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1995.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].items[17].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[17].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[17].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1996.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1996-01-01T11:00:00Z&time_end=1996-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[17].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[17].name | string | `"ERA5 daily mean mslp 1996"` |  |
| initConfig.catalog[3].items[3].items[17].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[17].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[17].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1996.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].items[18].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[18].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[18].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1997.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1997-01-01T11:00:00Z&time_end=1997-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[18].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[18].name | string | `"ERA5 daily mean mslp 1997"` |  |
| initConfig.catalog[3].items[3].items[18].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[18].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[18].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1997.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].items[19].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[19].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[19].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1998.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1998-01-01T11:00:00Z&time_end=1998-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[19].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[19].name | string | `"ERA5 daily mean mslp 1998"` |  |
| initConfig.catalog[3].items[3].items[19].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[19].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[19].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1998.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].items[1].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[1].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[1].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1980.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1980-01-01T11:00:00Z&time_end=1980-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[1].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[1].name | string | `"ERA5 daily mean mslp 1980"` |  |
| initConfig.catalog[3].items[3].items[1].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[1].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[1].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1980.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].items[20].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[20].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[20].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1999.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1999-01-01T11:00:00Z&time_end=1999-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[20].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[20].name | string | `"ERA5 daily mean mslp 1999"` |  |
| initConfig.catalog[3].items[3].items[20].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[20].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[20].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1999.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].items[21].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[21].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[21].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_2000.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2000-01-01T11:00:00Z&time_end=2000-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[21].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[21].name | string | `"ERA5 daily mean mslp 2000"` |  |
| initConfig.catalog[3].items[3].items[21].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[21].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[21].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_2000.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].items[22].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[22].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[22].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_2001.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2001-01-01T11:00:00Z&time_end=2001-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[22].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[22].name | string | `"ERA5 daily mean mslp 2001"` |  |
| initConfig.catalog[3].items[3].items[22].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[22].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[22].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_2001.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].items[23].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[23].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[23].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_2002.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2002-01-01T11:00:00Z&time_end=2002-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[23].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[23].name | string | `"ERA5 daily mean mslp 2002"` |  |
| initConfig.catalog[3].items[3].items[23].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[23].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[23].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_2002.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].items[24].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[24].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[24].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_2003.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2003-01-01T11:00:00Z&time_end=2003-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[24].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[24].name | string | `"ERA5 daily mean mslp 2003"` |  |
| initConfig.catalog[3].items[3].items[24].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[24].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[24].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_2003.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].items[25].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[25].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[25].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_2004.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2004-01-01T11:00:00Z&time_end=2004-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[25].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[25].name | string | `"ERA5 daily mean mslp 2004"` |  |
| initConfig.catalog[3].items[3].items[25].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[25].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[25].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_2004.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].items[26].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[26].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[26].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_2005.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2005-01-01T11:00:00Z&time_end=2005-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[26].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[26].name | string | `"ERA5 daily mean mslp 2005"` |  |
| initConfig.catalog[3].items[3].items[26].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[26].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[26].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_2005.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].items[27].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[27].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[27].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_2006.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2006-01-01T11:00:00Z&time_end=2006-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[27].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[27].name | string | `"ERA5 daily mean mslp 2006"` |  |
| initConfig.catalog[3].items[3].items[27].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[27].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[27].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_2006.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].items[28].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[28].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[28].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_2007.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2007-01-01T11:00:00Z&time_end=2007-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[28].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[28].name | string | `"ERA5 daily mean mslp 2007"` |  |
| initConfig.catalog[3].items[3].items[28].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[28].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[28].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_2007.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].items[29].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[29].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[29].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_2008.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2008-01-01T11:00:00Z&time_end=2008-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[29].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[29].name | string | `"ERA5 daily mean mslp 2008"` |  |
| initConfig.catalog[3].items[3].items[29].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[29].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[29].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_2008.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].items[2].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[2].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[2].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1981.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1981-01-01T11:00:00Z&time_end=1981-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[2].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[2].name | string | `"ERA5 daily mean mslp 1981"` |  |
| initConfig.catalog[3].items[3].items[2].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[2].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[2].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1981.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].items[30].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[30].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[30].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_2009.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2009-01-01T11:00:00Z&time_end=2009-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[30].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[30].name | string | `"ERA5 daily mean mslp 2009"` |  |
| initConfig.catalog[3].items[3].items[30].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[30].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[30].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_2009.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].items[31].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[31].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[31].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_2010.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2010-01-01T11:00:00Z&time_end=2010-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[31].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[31].name | string | `"ERA5 daily mean mslp 2010"` |  |
| initConfig.catalog[3].items[3].items[31].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[31].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[31].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_2010.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].items[32].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[32].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[32].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_2011.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2011-01-01T11:00:00Z&time_end=2011-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[32].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[32].name | string | `"ERA5 daily mean mslp 2011"` |  |
| initConfig.catalog[3].items[3].items[32].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[32].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[32].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_2011.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].items[33].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[33].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[33].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_2012.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2012-01-01T11:00:00Z&time_end=2012-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[33].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[33].name | string | `"ERA5 daily mean mslp 2012"` |  |
| initConfig.catalog[3].items[3].items[33].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[33].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[33].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_2012.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].items[34].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[34].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[34].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_2013.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2013-01-01T11:00:00Z&time_end=2013-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[34].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[34].name | string | `"ERA5 daily mean mslp 2013"` |  |
| initConfig.catalog[3].items[3].items[34].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[34].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[34].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_2013.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].items[35].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[35].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[35].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_2014.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2014-01-01T11:00:00Z&time_end=2014-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[35].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[35].name | string | `"ERA5 daily mean mslp 2014"` |  |
| initConfig.catalog[3].items[3].items[35].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[35].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[35].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_2014.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].items[36].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[36].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[36].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_2015.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2015-01-01T11:00:00Z&time_end=2015-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[36].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[36].name | string | `"ERA5 daily mean mslp 2015"` |  |
| initConfig.catalog[3].items[3].items[36].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[36].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[36].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_2015.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].items[37].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[37].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[37].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_2016.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2016-01-01T11:00:00Z&time_end=2016-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[37].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[37].name | string | `"ERA5 daily mean mslp 2016"` |  |
| initConfig.catalog[3].items[3].items[37].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[37].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[37].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_2016.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].items[38].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[38].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[38].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_2017.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2017-01-01T11:00:00Z&time_end=2017-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[38].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[38].name | string | `"ERA5 daily mean mslp 2017"` |  |
| initConfig.catalog[3].items[3].items[38].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[38].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[38].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_2017.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].items[39].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[39].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[39].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_2018.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2018-01-01T11:00:00Z&time_end=2018-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[39].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[39].name | string | `"ERA5 daily mean mslp 2018"` |  |
| initConfig.catalog[3].items[3].items[39].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[39].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[39].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_2018.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].items[3].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[3].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[3].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1982.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1982-01-01T11:00:00Z&time_end=1982-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[3].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[3].name | string | `"ERA5 daily mean mslp 1982"` |  |
| initConfig.catalog[3].items[3].items[3].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[3].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[3].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1982.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].items[40].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[40].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[40].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_2019.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2019-01-01T11:00:00Z&time_end=2019-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[40].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[40].name | string | `"ERA5 daily mean mslp 2019"` |  |
| initConfig.catalog[3].items[3].items[40].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[40].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[40].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_2019.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].items[4].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[4].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[4].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1983.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1983-01-01T11:00:00Z&time_end=1983-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[4].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[4].name | string | `"ERA5 daily mean mslp 1983"` |  |
| initConfig.catalog[3].items[3].items[4].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[4].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[4].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1983.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].items[5].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[5].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[5].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1984.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1984-01-01T11:00:00Z&time_end=1984-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[5].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[5].name | string | `"ERA5 daily mean mslp 1984"` |  |
| initConfig.catalog[3].items[3].items[5].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[5].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[5].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1984.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].items[6].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[6].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[6].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1985.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1985-01-01T11:00:00Z&time_end=1985-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[6].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[6].name | string | `"ERA5 daily mean mslp 1985"` |  |
| initConfig.catalog[3].items[3].items[6].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[6].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[6].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1985.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].items[7].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[7].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[7].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1986.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1986-01-01T11:00:00Z&time_end=1986-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[7].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[7].name | string | `"ERA5 daily mean mslp 1986"` |  |
| initConfig.catalog[3].items[3].items[7].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[7].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[7].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1986.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].items[8].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[8].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[8].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1987.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1987-01-01T11:00:00Z&time_end=1987-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[8].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[8].name | string | `"ERA5 daily mean mslp 1987"` |  |
| initConfig.catalog[3].items[3].items[8].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[8].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[8].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1987.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].items[9].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[3].items[3].items[9].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[3].items[3].items[9].featureInfoTemplate | string | `"<p>ERA5 daily mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1988.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1988-01-01T11:00:00Z&time_end=1988-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[3].items[9].layers | string | `"msl"` |  |
| initConfig.catalog[3].items[3].items[9].name | string | `"ERA5 daily mean mslp 1988"` |  |
| initConfig.catalog[3].items[3].items[9].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[3].items[9].type | string | `"wms"` |  |
| initConfig.catalog[3].items[3].items[9].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_mslp/ERA5_daily_mean_mslp_1988.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[3].name | string | `"ERA5 daily mean mslp"` |  |
| initConfig.catalog[3].items[3].preserveOrder | bool | `true` |  |
| initConfig.catalog[3].items[3].type | string | `"group"` |  |
| initConfig.catalog[3].items[4].isOpen | bool | `false` |  |
| initConfig.catalog[3].items[4].items[0].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[0].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[0].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1979.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1979-01-01T11:00:00Z&time_end=1979-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[0].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[0].name | string | `"ERA5 daily mean soil temp L1 1979"` |  |
| initConfig.catalog[3].items[4].items[0].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[0].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[0].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1979.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].items[10].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[10].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[10].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1989.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1989-01-01T11:00:00Z&time_end=1989-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[10].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[10].name | string | `"ERA5 daily mean soil temp L1 1989"` |  |
| initConfig.catalog[3].items[4].items[10].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[10].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[10].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1989.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].items[11].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[11].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[11].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1990.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1990-01-01T11:00:00Z&time_end=1990-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[11].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[11].name | string | `"ERA5 daily mean soil temp L1 1990"` |  |
| initConfig.catalog[3].items[4].items[11].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[11].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[11].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1990.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].items[12].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[12].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[12].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1991.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1991-01-01T11:00:00Z&time_end=1991-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[12].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[12].name | string | `"ERA5 daily mean soil temp L1 1991"` |  |
| initConfig.catalog[3].items[4].items[12].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[12].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[12].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1991.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].items[13].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[13].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[13].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1992.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1992-01-01T11:00:00Z&time_end=1992-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[13].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[13].name | string | `"ERA5 daily mean soil temp L1 1992"` |  |
| initConfig.catalog[3].items[4].items[13].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[13].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[13].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1992.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].items[14].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[14].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[14].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1993.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1993-01-01T11:00:00Z&time_end=1993-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[14].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[14].name | string | `"ERA5 daily mean soil temp L1 1993"` |  |
| initConfig.catalog[3].items[4].items[14].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[14].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[14].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1993.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].items[15].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[15].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[15].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1994.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1994-01-01T11:00:00Z&time_end=1994-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[15].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[15].name | string | `"ERA5 daily mean soil temp L1 1994"` |  |
| initConfig.catalog[3].items[4].items[15].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[15].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[15].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1994.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].items[16].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[16].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[16].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1995.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1995-01-01T11:00:00Z&time_end=1995-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[16].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[16].name | string | `"ERA5 daily mean soil temp L1 1995"` |  |
| initConfig.catalog[3].items[4].items[16].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[16].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[16].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1995.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].items[17].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[17].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[17].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1996.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1996-01-01T11:00:00Z&time_end=1996-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[17].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[17].name | string | `"ERA5 daily mean soil temp L1 1996"` |  |
| initConfig.catalog[3].items[4].items[17].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[17].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[17].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1996.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].items[18].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[18].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[18].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1997.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1997-01-01T11:00:00Z&time_end=1997-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[18].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[18].name | string | `"ERA5 daily mean soil temp L1 1997"` |  |
| initConfig.catalog[3].items[4].items[18].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[18].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[18].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1997.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].items[19].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[19].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[19].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1998.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1998-01-01T11:00:00Z&time_end=1998-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[19].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[19].name | string | `"ERA5 daily mean soil temp L1 1998"` |  |
| initConfig.catalog[3].items[4].items[19].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[19].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[19].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1998.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].items[1].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[1].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[1].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1980.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1980-01-01T11:00:00Z&time_end=1980-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[1].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[1].name | string | `"ERA5 daily mean soil temp L1 1980"` |  |
| initConfig.catalog[3].items[4].items[1].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[1].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[1].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1980.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].items[20].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[20].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[20].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1999.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1999-01-01T11:00:00Z&time_end=1999-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[20].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[20].name | string | `"ERA5 daily mean soil temp L1 1999"` |  |
| initConfig.catalog[3].items[4].items[20].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[20].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[20].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1999.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].items[21].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[21].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[21].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_2000.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2000-01-01T11:00:00Z&time_end=2000-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[21].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[21].name | string | `"ERA5 daily mean soil temp L1 2000"` |  |
| initConfig.catalog[3].items[4].items[21].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[21].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[21].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_2000.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].items[22].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[22].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[22].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_2001.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2001-01-01T11:00:00Z&time_end=2001-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[22].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[22].name | string | `"ERA5 daily mean soil temp L1 2001"` |  |
| initConfig.catalog[3].items[4].items[22].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[22].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[22].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_2001.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].items[23].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[23].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[23].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_2002.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2002-01-01T11:00:00Z&time_end=2002-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[23].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[23].name | string | `"ERA5 daily mean soil temp L1 2002"` |  |
| initConfig.catalog[3].items[4].items[23].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[23].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[23].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_2002.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].items[24].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[24].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[24].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_2003.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2003-01-01T11:00:00Z&time_end=2003-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[24].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[24].name | string | `"ERA5 daily mean soil temp L1 2003"` |  |
| initConfig.catalog[3].items[4].items[24].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[24].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[24].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_2003.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].items[25].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[25].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[25].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_2004.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2004-01-01T11:00:00Z&time_end=2004-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[25].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[25].name | string | `"ERA5 daily mean soil temp L1 2004"` |  |
| initConfig.catalog[3].items[4].items[25].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[25].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[25].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_2004.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].items[26].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[26].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[26].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_2005.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2005-01-01T11:00:00Z&time_end=2005-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[26].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[26].name | string | `"ERA5 daily mean soil temp L1 2005"` |  |
| initConfig.catalog[3].items[4].items[26].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[26].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[26].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_2005.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].items[27].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[27].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[27].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_2006.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2006-01-01T11:00:00Z&time_end=2006-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[27].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[27].name | string | `"ERA5 daily mean soil temp L1 2006"` |  |
| initConfig.catalog[3].items[4].items[27].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[27].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[27].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_2006.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].items[28].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[28].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[28].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_2007.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2007-01-01T11:00:00Z&time_end=2007-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[28].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[28].name | string | `"ERA5 daily mean soil temp L1 2007"` |  |
| initConfig.catalog[3].items[4].items[28].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[28].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[28].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_2007.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].items[29].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[29].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[29].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_2008.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2008-01-01T11:00:00Z&time_end=2008-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[29].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[29].name | string | `"ERA5 daily mean soil temp L1 2008"` |  |
| initConfig.catalog[3].items[4].items[29].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[29].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[29].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_2008.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].items[2].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[2].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[2].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1981.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1981-01-01T11:00:00Z&time_end=1981-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[2].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[2].name | string | `"ERA5 daily mean soil temp L1 1981"` |  |
| initConfig.catalog[3].items[4].items[2].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[2].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[2].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1981.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].items[30].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[30].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[30].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_2009.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2009-01-01T11:00:00Z&time_end=2009-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[30].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[30].name | string | `"ERA5 daily mean soil temp L1 2009"` |  |
| initConfig.catalog[3].items[4].items[30].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[30].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[30].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_2009.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].items[31].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[31].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[31].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_2010.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2010-01-01T11:00:00Z&time_end=2010-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[31].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[31].name | string | `"ERA5 daily mean soil temp L1 2010"` |  |
| initConfig.catalog[3].items[4].items[31].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[31].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[31].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_2010.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].items[32].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[32].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[32].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_2011.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2011-01-01T11:00:00Z&time_end=2011-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[32].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[32].name | string | `"ERA5 daily mean soil temp L1 2011"` |  |
| initConfig.catalog[3].items[4].items[32].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[32].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[32].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_2011.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].items[33].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[33].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[33].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_2012.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2012-01-01T11:00:00Z&time_end=2012-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[33].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[33].name | string | `"ERA5 daily mean soil temp L1 2012"` |  |
| initConfig.catalog[3].items[4].items[33].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[33].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[33].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_2012.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].items[34].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[34].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[34].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_2013.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2013-01-01T11:00:00Z&time_end=2013-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[34].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[34].name | string | `"ERA5 daily mean soil temp L1 2013"` |  |
| initConfig.catalog[3].items[4].items[34].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[34].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[34].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_2013.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].items[35].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[35].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[35].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_2014.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2014-01-01T11:00:00Z&time_end=2014-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[35].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[35].name | string | `"ERA5 daily mean soil temp L1 2014"` |  |
| initConfig.catalog[3].items[4].items[35].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[35].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[35].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_2014.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].items[36].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[36].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[36].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_2015.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2015-01-01T11:00:00Z&time_end=2015-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[36].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[36].name | string | `"ERA5 daily mean soil temp L1 2015"` |  |
| initConfig.catalog[3].items[4].items[36].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[36].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[36].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_2015.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].items[37].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[37].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[37].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_2016.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2016-01-01T11:00:00Z&time_end=2016-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[37].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[37].name | string | `"ERA5 daily mean soil temp L1 2016"` |  |
| initConfig.catalog[3].items[4].items[37].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[37].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[37].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_2016.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].items[38].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[38].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[38].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_2017.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2017-01-01T11:00:00Z&time_end=2017-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[38].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[38].name | string | `"ERA5 daily mean soil temp L1 2017"` |  |
| initConfig.catalog[3].items[4].items[38].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[38].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[38].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_2017.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].items[39].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[39].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[39].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_2018.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2018-01-01T11:00:00Z&time_end=2018-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[39].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[39].name | string | `"ERA5 daily mean soil temp L1 2018"` |  |
| initConfig.catalog[3].items[4].items[39].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[39].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[39].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_2018.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].items[3].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[3].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[3].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1982.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1982-01-01T11:00:00Z&time_end=1982-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[3].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[3].name | string | `"ERA5 daily mean soil temp L1 1982"` |  |
| initConfig.catalog[3].items[4].items[3].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[3].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[3].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1982.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].items[40].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[40].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[40].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_2019.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2019-01-01T11:00:00Z&time_end=2019-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[40].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[40].name | string | `"ERA5 daily mean soil temp L1 2019"` |  |
| initConfig.catalog[3].items[4].items[40].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[40].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[40].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_2019.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].items[4].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[4].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[4].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1983.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1983-01-01T11:00:00Z&time_end=1983-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[4].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[4].name | string | `"ERA5 daily mean soil temp L1 1983"` |  |
| initConfig.catalog[3].items[4].items[4].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[4].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[4].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1983.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].items[5].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[5].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[5].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1984.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1984-01-01T11:00:00Z&time_end=1984-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[5].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[5].name | string | `"ERA5 daily mean soil temp L1 1984"` |  |
| initConfig.catalog[3].items[4].items[5].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[5].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[5].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1984.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].items[6].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[6].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[6].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1985.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1985-01-01T11:00:00Z&time_end=1985-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[6].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[6].name | string | `"ERA5 daily mean soil temp L1 1985"` |  |
| initConfig.catalog[3].items[4].items[6].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[6].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[6].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1985.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].items[7].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[7].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[7].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1986.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1986-01-01T11:00:00Z&time_end=1986-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[7].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[7].name | string | `"ERA5 daily mean soil temp L1 1986"` |  |
| initConfig.catalog[3].items[4].items[7].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[7].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[7].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1986.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].items[8].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[8].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[8].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1987.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1987-01-01T11:00:00Z&time_end=1987-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[8].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[8].name | string | `"ERA5 daily mean soil temp L1 1987"` |  |
| initConfig.catalog[3].items[4].items[8].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[8].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[8].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1987.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].items[9].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[3].items[4].items[9].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[3].items[4].items[9].featureInfoTemplate | string | `"<p>ERA5 daily mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1988.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1988-01-01T11:00:00Z&time_end=1988-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[4].items[9].layers | string | `"stl1"` |  |
| initConfig.catalog[3].items[4].items[9].name | string | `"ERA5 daily mean soil temp L1 1988"` |  |
| initConfig.catalog[3].items[4].items[9].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[4].items[9].type | string | `"wms"` |  |
| initConfig.catalog[3].items[4].items[9].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_temp_L1/ERA5_daily_mean_soil_temp_L1_1988.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[4].name | string | `"ERA5 daily mean soil temp L1"` |  |
| initConfig.catalog[3].items[4].preserveOrder | bool | `true` |  |
| initConfig.catalog[3].items[4].type | string | `"group"` |  |
| initConfig.catalog[3].items[5].isOpen | bool | `false` |  |
| initConfig.catalog[3].items[5].items[0].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[0].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[0].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1979.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1979-01-01T11:00:00Z&time_end=1979-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[0].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[0].name | string | `"ERA5 daily mean soil water L1 1979"` |  |
| initConfig.catalog[3].items[5].items[0].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[0].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[0].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1979.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].items[10].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[10].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[10].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1989.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1989-01-01T11:00:00Z&time_end=1989-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[10].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[10].name | string | `"ERA5 daily mean soil water L1 1989"` |  |
| initConfig.catalog[3].items[5].items[10].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[10].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[10].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1989.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].items[11].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[11].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[11].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1990.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1990-01-01T11:00:00Z&time_end=1990-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[11].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[11].name | string | `"ERA5 daily mean soil water L1 1990"` |  |
| initConfig.catalog[3].items[5].items[11].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[11].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[11].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1990.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].items[12].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[12].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[12].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1991.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1991-01-01T11:00:00Z&time_end=1991-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[12].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[12].name | string | `"ERA5 daily mean soil water L1 1991"` |  |
| initConfig.catalog[3].items[5].items[12].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[12].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[12].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1991.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].items[13].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[13].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[13].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1992.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1992-01-01T11:00:00Z&time_end=1992-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[13].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[13].name | string | `"ERA5 daily mean soil water L1 1992"` |  |
| initConfig.catalog[3].items[5].items[13].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[13].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[13].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1992.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].items[14].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[14].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[14].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1993.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1993-01-01T11:00:00Z&time_end=1993-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[14].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[14].name | string | `"ERA5 daily mean soil water L1 1993"` |  |
| initConfig.catalog[3].items[5].items[14].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[14].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[14].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1993.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].items[15].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[15].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[15].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1994.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1994-01-01T11:00:00Z&time_end=1994-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[15].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[15].name | string | `"ERA5 daily mean soil water L1 1994"` |  |
| initConfig.catalog[3].items[5].items[15].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[15].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[15].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1994.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].items[16].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[16].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[16].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1995.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1995-01-01T11:00:00Z&time_end=1995-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[16].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[16].name | string | `"ERA5 daily mean soil water L1 1995"` |  |
| initConfig.catalog[3].items[5].items[16].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[16].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[16].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1995.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].items[17].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[17].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[17].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1996.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1996-01-01T11:00:00Z&time_end=1996-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[17].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[17].name | string | `"ERA5 daily mean soil water L1 1996"` |  |
| initConfig.catalog[3].items[5].items[17].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[17].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[17].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1996.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].items[18].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[18].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[18].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1997.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1997-01-01T11:00:00Z&time_end=1997-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[18].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[18].name | string | `"ERA5 daily mean soil water L1 1997"` |  |
| initConfig.catalog[3].items[5].items[18].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[18].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[18].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1997.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].items[19].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[19].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[19].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1998.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1998-01-01T11:00:00Z&time_end=1998-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[19].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[19].name | string | `"ERA5 daily mean soil water L1 1998"` |  |
| initConfig.catalog[3].items[5].items[19].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[19].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[19].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1998.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].items[1].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[1].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[1].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1980.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1980-01-01T11:00:00Z&time_end=1980-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[1].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[1].name | string | `"ERA5 daily mean soil water L1 1980"` |  |
| initConfig.catalog[3].items[5].items[1].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[1].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[1].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1980.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].items[20].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[20].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[20].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1999.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1999-01-01T11:00:00Z&time_end=1999-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[20].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[20].name | string | `"ERA5 daily mean soil water L1 1999"` |  |
| initConfig.catalog[3].items[5].items[20].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[20].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[20].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1999.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].items[21].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[21].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[21].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_2000.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2000-01-01T11:00:00Z&time_end=2000-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[21].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[21].name | string | `"ERA5 daily mean soil water L1 2000"` |  |
| initConfig.catalog[3].items[5].items[21].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[21].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[21].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_2000.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].items[22].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[22].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[22].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_2001.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2001-01-01T11:00:00Z&time_end=2001-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[22].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[22].name | string | `"ERA5 daily mean soil water L1 2001"` |  |
| initConfig.catalog[3].items[5].items[22].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[22].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[22].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_2001.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].items[23].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[23].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[23].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_2002.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2002-01-01T11:00:00Z&time_end=2002-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[23].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[23].name | string | `"ERA5 daily mean soil water L1 2002"` |  |
| initConfig.catalog[3].items[5].items[23].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[23].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[23].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_2002.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].items[24].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[24].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[24].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_2003.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2003-01-01T11:00:00Z&time_end=2003-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[24].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[24].name | string | `"ERA5 daily mean soil water L1 2003"` |  |
| initConfig.catalog[3].items[5].items[24].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[24].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[24].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_2003.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].items[25].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[25].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[25].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_2004.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2004-01-01T11:00:00Z&time_end=2004-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[25].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[25].name | string | `"ERA5 daily mean soil water L1 2004"` |  |
| initConfig.catalog[3].items[5].items[25].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[25].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[25].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_2004.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].items[26].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[26].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[26].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_2005.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2005-01-01T11:00:00Z&time_end=2005-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[26].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[26].name | string | `"ERA5 daily mean soil water L1 2005"` |  |
| initConfig.catalog[3].items[5].items[26].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[26].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[26].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_2005.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].items[27].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[27].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[27].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_2006.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2006-01-01T11:00:00Z&time_end=2006-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[27].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[27].name | string | `"ERA5 daily mean soil water L1 2006"` |  |
| initConfig.catalog[3].items[5].items[27].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[27].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[27].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_2006.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].items[28].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[28].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[28].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_2007.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2007-01-01T11:00:00Z&time_end=2007-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[28].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[28].name | string | `"ERA5 daily mean soil water L1 2007"` |  |
| initConfig.catalog[3].items[5].items[28].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[28].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[28].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_2007.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].items[29].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[29].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[29].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_2008.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2008-01-01T11:00:00Z&time_end=2008-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[29].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[29].name | string | `"ERA5 daily mean soil water L1 2008"` |  |
| initConfig.catalog[3].items[5].items[29].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[29].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[29].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_2008.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].items[2].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[2].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[2].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1981.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1981-01-01T11:00:00Z&time_end=1981-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[2].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[2].name | string | `"ERA5 daily mean soil water L1 1981"` |  |
| initConfig.catalog[3].items[5].items[2].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[2].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[2].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1981.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].items[30].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[30].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[30].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_2009.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2009-01-01T11:00:00Z&time_end=2009-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[30].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[30].name | string | `"ERA5 daily mean soil water L1 2009"` |  |
| initConfig.catalog[3].items[5].items[30].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[30].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[30].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_2009.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].items[31].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[31].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[31].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_2010.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2010-01-01T11:00:00Z&time_end=2010-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[31].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[31].name | string | `"ERA5 daily mean soil water L1 2010"` |  |
| initConfig.catalog[3].items[5].items[31].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[31].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[31].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_2010.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].items[32].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[32].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[32].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_2011.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2011-01-01T11:00:00Z&time_end=2011-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[32].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[32].name | string | `"ERA5 daily mean soil water L1 2011"` |  |
| initConfig.catalog[3].items[5].items[32].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[32].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[32].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_2011.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].items[33].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[33].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[33].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_2012.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2012-01-01T11:00:00Z&time_end=2012-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[33].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[33].name | string | `"ERA5 daily mean soil water L1 2012"` |  |
| initConfig.catalog[3].items[5].items[33].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[33].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[33].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_2012.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].items[34].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[34].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[34].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_2013.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2013-01-01T11:00:00Z&time_end=2013-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[34].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[34].name | string | `"ERA5 daily mean soil water L1 2013"` |  |
| initConfig.catalog[3].items[5].items[34].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[34].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[34].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_2013.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].items[35].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[35].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[35].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_2014.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2014-01-01T11:00:00Z&time_end=2014-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[35].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[35].name | string | `"ERA5 daily mean soil water L1 2014"` |  |
| initConfig.catalog[3].items[5].items[35].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[35].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[35].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_2014.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].items[36].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[36].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[36].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_2015.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2015-01-01T11:00:00Z&time_end=2015-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[36].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[36].name | string | `"ERA5 daily mean soil water L1 2015"` |  |
| initConfig.catalog[3].items[5].items[36].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[36].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[36].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_2015.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].items[37].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[37].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[37].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_2016.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2016-01-01T11:00:00Z&time_end=2016-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[37].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[37].name | string | `"ERA5 daily mean soil water L1 2016"` |  |
| initConfig.catalog[3].items[5].items[37].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[37].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[37].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_2016.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].items[38].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[38].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[38].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_2017.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2017-01-01T11:00:00Z&time_end=2017-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[38].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[38].name | string | `"ERA5 daily mean soil water L1 2017"` |  |
| initConfig.catalog[3].items[5].items[38].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[38].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[38].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_2017.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].items[39].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[39].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[39].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_2018.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2018-01-01T11:00:00Z&time_end=2018-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[39].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[39].name | string | `"ERA5 daily mean soil water L1 2018"` |  |
| initConfig.catalog[3].items[5].items[39].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[39].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[39].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_2018.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].items[3].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[3].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[3].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1982.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1982-01-01T11:00:00Z&time_end=1982-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[3].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[3].name | string | `"ERA5 daily mean soil water L1 1982"` |  |
| initConfig.catalog[3].items[5].items[3].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[3].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[3].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1982.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].items[40].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[40].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[40].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_2019.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2019-01-01T11:00:00Z&time_end=2019-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[40].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[40].name | string | `"ERA5 daily mean soil water L1 2019"` |  |
| initConfig.catalog[3].items[5].items[40].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[40].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[40].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_2019.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].items[4].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[4].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[4].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1983.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1983-01-01T11:00:00Z&time_end=1983-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[4].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[4].name | string | `"ERA5 daily mean soil water L1 1983"` |  |
| initConfig.catalog[3].items[5].items[4].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[4].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[4].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1983.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].items[5].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[5].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[5].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1984.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1984-01-01T11:00:00Z&time_end=1984-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[5].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[5].name | string | `"ERA5 daily mean soil water L1 1984"` |  |
| initConfig.catalog[3].items[5].items[5].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[5].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[5].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1984.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].items[6].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[6].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[6].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1985.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1985-01-01T11:00:00Z&time_end=1985-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[6].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[6].name | string | `"ERA5 daily mean soil water L1 1985"` |  |
| initConfig.catalog[3].items[5].items[6].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[6].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[6].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1985.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].items[7].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[7].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[7].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1986.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1986-01-01T11:00:00Z&time_end=1986-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[7].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[7].name | string | `"ERA5 daily mean soil water L1 1986"` |  |
| initConfig.catalog[3].items[5].items[7].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[7].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[7].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1986.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].items[8].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[8].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[8].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1987.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1987-01-01T11:00:00Z&time_end=1987-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[8].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[8].name | string | `"ERA5 daily mean soil water L1 1987"` |  |
| initConfig.catalog[3].items[5].items[8].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[8].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[8].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1987.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].items[9].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[3].items[5].items[9].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[5].items[9].featureInfoTemplate | string | `"<p>ERA5 daily mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1988.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1988-01-01T11:00:00Z&time_end=1988-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[5].items[9].layers | string | `"swvl1"` |  |
| initConfig.catalog[3].items[5].items[9].name | string | `"ERA5 daily mean soil water L1 1988"` |  |
| initConfig.catalog[3].items[5].items[9].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[3].items[5].items[9].type | string | `"wms"` |  |
| initConfig.catalog[3].items[5].items[9].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_soil_water_L1/ERA5_daily_mean_soil_water_L1_1988.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[5].name | string | `"ERA5 daily mean soil water L1"` |  |
| initConfig.catalog[3].items[5].preserveOrder | bool | `true` |  |
| initConfig.catalog[3].items[5].type | string | `"group"` |  |
| initConfig.catalog[3].items[6].isOpen | bool | `false` |  |
| initConfig.catalog[3].items[6].items[0].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[0].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[0].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1979.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1979-01-01T11:00:00Z&time_end=1979-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[0].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[0].name | string | `"ERA5 daily mean sol rad 1979"` |  |
| initConfig.catalog[3].items[6].items[0].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[0].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[0].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1979.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].items[10].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[10].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[10].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1989.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1989-01-01T11:00:00Z&time_end=1989-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[10].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[10].name | string | `"ERA5 daily mean sol rad 1989"` |  |
| initConfig.catalog[3].items[6].items[10].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[10].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[10].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1989.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].items[11].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[11].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[11].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1990.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1990-01-01T11:00:00Z&time_end=1990-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[11].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[11].name | string | `"ERA5 daily mean sol rad 1990"` |  |
| initConfig.catalog[3].items[6].items[11].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[11].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[11].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1990.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].items[12].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[12].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[12].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1991.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1991-01-01T11:00:00Z&time_end=1991-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[12].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[12].name | string | `"ERA5 daily mean sol rad 1991"` |  |
| initConfig.catalog[3].items[6].items[12].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[12].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[12].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1991.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].items[13].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[13].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[13].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1992.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1992-01-01T11:00:00Z&time_end=1992-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[13].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[13].name | string | `"ERA5 daily mean sol rad 1992"` |  |
| initConfig.catalog[3].items[6].items[13].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[13].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[13].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1992.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].items[14].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[14].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[14].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1993.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1993-01-01T11:00:00Z&time_end=1993-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[14].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[14].name | string | `"ERA5 daily mean sol rad 1993"` |  |
| initConfig.catalog[3].items[6].items[14].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[14].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[14].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1993.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].items[15].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[15].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[15].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1994.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1994-01-01T11:00:00Z&time_end=1994-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[15].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[15].name | string | `"ERA5 daily mean sol rad 1994"` |  |
| initConfig.catalog[3].items[6].items[15].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[15].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[15].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1994.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].items[16].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[16].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[16].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1995.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1995-01-01T11:00:00Z&time_end=1995-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[16].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[16].name | string | `"ERA5 daily mean sol rad 1995"` |  |
| initConfig.catalog[3].items[6].items[16].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[16].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[16].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1995.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].items[17].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[17].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[17].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1996.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1996-01-01T11:00:00Z&time_end=1996-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[17].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[17].name | string | `"ERA5 daily mean sol rad 1996"` |  |
| initConfig.catalog[3].items[6].items[17].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[17].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[17].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1996.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].items[18].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[18].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[18].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1997.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1997-01-01T11:00:00Z&time_end=1997-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[18].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[18].name | string | `"ERA5 daily mean sol rad 1997"` |  |
| initConfig.catalog[3].items[6].items[18].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[18].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[18].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1997.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].items[19].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[19].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[19].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1998.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1998-01-01T11:00:00Z&time_end=1998-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[19].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[19].name | string | `"ERA5 daily mean sol rad 1998"` |  |
| initConfig.catalog[3].items[6].items[19].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[19].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[19].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1998.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].items[1].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[1].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[1].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1980.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1980-01-01T11:00:00Z&time_end=1980-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[1].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[1].name | string | `"ERA5 daily mean sol rad 1980"` |  |
| initConfig.catalog[3].items[6].items[1].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[1].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[1].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1980.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].items[20].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[20].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[20].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1999.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1999-01-01T11:00:00Z&time_end=1999-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[20].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[20].name | string | `"ERA5 daily mean sol rad 1999"` |  |
| initConfig.catalog[3].items[6].items[20].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[20].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[20].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1999.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].items[21].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[21].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[21].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_2000.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2000-01-01T11:00:00Z&time_end=2000-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[21].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[21].name | string | `"ERA5 daily mean sol rad 2000"` |  |
| initConfig.catalog[3].items[6].items[21].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[21].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[21].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_2000.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].items[22].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[22].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[22].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_2001.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2001-01-01T11:00:00Z&time_end=2001-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[22].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[22].name | string | `"ERA5 daily mean sol rad 2001"` |  |
| initConfig.catalog[3].items[6].items[22].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[22].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[22].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_2001.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].items[23].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[23].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[23].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_2002.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2002-01-01T11:00:00Z&time_end=2002-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[23].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[23].name | string | `"ERA5 daily mean sol rad 2002"` |  |
| initConfig.catalog[3].items[6].items[23].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[23].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[23].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_2002.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].items[24].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[24].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[24].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_2003.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2003-01-01T11:00:00Z&time_end=2003-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[24].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[24].name | string | `"ERA5 daily mean sol rad 2003"` |  |
| initConfig.catalog[3].items[6].items[24].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[24].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[24].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_2003.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].items[25].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[25].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[25].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_2004.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2004-01-01T11:00:00Z&time_end=2004-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[25].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[25].name | string | `"ERA5 daily mean sol rad 2004"` |  |
| initConfig.catalog[3].items[6].items[25].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[25].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[25].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_2004.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].items[26].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[26].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[26].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_2005.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2005-01-01T11:00:00Z&time_end=2005-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[26].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[26].name | string | `"ERA5 daily mean sol rad 2005"` |  |
| initConfig.catalog[3].items[6].items[26].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[26].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[26].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_2005.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].items[27].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[27].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[27].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_2006.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2006-01-01T11:00:00Z&time_end=2006-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[27].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[27].name | string | `"ERA5 daily mean sol rad 2006"` |  |
| initConfig.catalog[3].items[6].items[27].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[27].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[27].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_2006.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].items[28].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[28].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[28].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_2007.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2007-01-01T11:00:00Z&time_end=2007-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[28].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[28].name | string | `"ERA5 daily mean sol rad 2007"` |  |
| initConfig.catalog[3].items[6].items[28].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[28].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[28].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_2007.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].items[29].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[29].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[29].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_2008.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2008-01-01T11:00:00Z&time_end=2008-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[29].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[29].name | string | `"ERA5 daily mean sol rad 2008"` |  |
| initConfig.catalog[3].items[6].items[29].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[29].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[29].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_2008.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].items[2].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[2].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[2].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1981.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1981-01-01T11:00:00Z&time_end=1981-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[2].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[2].name | string | `"ERA5 daily mean sol rad 1981"` |  |
| initConfig.catalog[3].items[6].items[2].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[2].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[2].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1981.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].items[30].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[30].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[30].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_2009.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2009-01-01T11:00:00Z&time_end=2009-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[30].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[30].name | string | `"ERA5 daily mean sol rad 2009"` |  |
| initConfig.catalog[3].items[6].items[30].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[30].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[30].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_2009.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].items[31].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[31].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[31].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_2010.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2010-01-01T11:00:00Z&time_end=2010-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[31].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[31].name | string | `"ERA5 daily mean sol rad 2010"` |  |
| initConfig.catalog[3].items[6].items[31].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[31].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[31].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_2010.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].items[32].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[32].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[32].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_2011.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2011-01-01T11:00:00Z&time_end=2011-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[32].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[32].name | string | `"ERA5 daily mean sol rad 2011"` |  |
| initConfig.catalog[3].items[6].items[32].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[32].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[32].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_2011.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].items[33].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[33].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[33].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_2012.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2012-01-01T11:00:00Z&time_end=2012-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[33].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[33].name | string | `"ERA5 daily mean sol rad 2012"` |  |
| initConfig.catalog[3].items[6].items[33].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[33].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[33].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_2012.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].items[34].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[34].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[34].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_2013.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2013-01-01T11:00:00Z&time_end=2013-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[34].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[34].name | string | `"ERA5 daily mean sol rad 2013"` |  |
| initConfig.catalog[3].items[6].items[34].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[34].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[34].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_2013.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].items[35].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[35].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[35].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_2014.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2014-01-01T11:00:00Z&time_end=2014-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[35].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[35].name | string | `"ERA5 daily mean sol rad 2014"` |  |
| initConfig.catalog[3].items[6].items[35].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[35].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[35].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_2014.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].items[36].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[36].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[36].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_2015.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2015-01-01T11:00:00Z&time_end=2015-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[36].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[36].name | string | `"ERA5 daily mean sol rad 2015"` |  |
| initConfig.catalog[3].items[6].items[36].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[36].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[36].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_2015.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].items[37].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[37].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[37].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_2016.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2016-01-01T11:00:00Z&time_end=2016-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[37].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[37].name | string | `"ERA5 daily mean sol rad 2016"` |  |
| initConfig.catalog[3].items[6].items[37].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[37].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[37].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_2016.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].items[38].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[38].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[38].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_2017.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2017-01-01T11:00:00Z&time_end=2017-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[38].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[38].name | string | `"ERA5 daily mean sol rad 2017"` |  |
| initConfig.catalog[3].items[6].items[38].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[38].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[38].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_2017.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].items[39].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[39].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[39].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_2018.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2018-01-01T11:00:00Z&time_end=2018-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[39].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[39].name | string | `"ERA5 daily mean sol rad 2018"` |  |
| initConfig.catalog[3].items[6].items[39].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[39].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[39].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_2018.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].items[3].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[3].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[3].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1982.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1982-01-01T11:00:00Z&time_end=1982-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[3].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[3].name | string | `"ERA5 daily mean sol rad 1982"` |  |
| initConfig.catalog[3].items[6].items[3].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[3].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[3].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1982.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].items[40].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[40].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[40].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_2019.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2019-01-01T11:00:00Z&time_end=2019-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[40].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[40].name | string | `"ERA5 daily mean sol rad 2019"` |  |
| initConfig.catalog[3].items[6].items[40].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[40].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[40].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_2019.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].items[4].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[4].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[4].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1983.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1983-01-01T11:00:00Z&time_end=1983-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[4].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[4].name | string | `"ERA5 daily mean sol rad 1983"` |  |
| initConfig.catalog[3].items[6].items[4].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[4].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[4].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1983.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].items[5].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[5].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[5].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1984.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1984-01-01T11:00:00Z&time_end=1984-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[5].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[5].name | string | `"ERA5 daily mean sol rad 1984"` |  |
| initConfig.catalog[3].items[6].items[5].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[5].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[5].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1984.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].items[6].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[6].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[6].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1985.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1985-01-01T11:00:00Z&time_end=1985-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[6].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[6].name | string | `"ERA5 daily mean sol rad 1985"` |  |
| initConfig.catalog[3].items[6].items[6].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[6].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[6].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1985.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].items[7].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[7].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[7].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1986.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1986-01-01T11:00:00Z&time_end=1986-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[7].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[7].name | string | `"ERA5 daily mean sol rad 1986"` |  |
| initConfig.catalog[3].items[6].items[7].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[7].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[7].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1986.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].items[8].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[8].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[8].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1987.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1987-01-01T11:00:00Z&time_end=1987-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[8].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[8].name | string | `"ERA5 daily mean sol rad 1987"` |  |
| initConfig.catalog[3].items[6].items[8].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[8].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[8].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1987.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].items[9].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[3].items[6].items[9].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[3].items[6].items[9].featureInfoTemplate | string | `"<p>ERA5 daily mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1988.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1988-01-01T11:00:00Z&time_end=1988-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[6].items[9].layers | string | `"ssr"` |  |
| initConfig.catalog[3].items[6].items[9].name | string | `"ERA5 daily mean sol rad 1988"` |  |
| initConfig.catalog[3].items[6].items[9].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[3].items[6].items[9].type | string | `"wms"` |  |
| initConfig.catalog[3].items[6].items[9].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_mean_sol_rad/ERA5_daily_mean_sol_rad_1988.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[6].name | string | `"ERA5 daily mean sol rad"` |  |
| initConfig.catalog[3].items[6].preserveOrder | bool | `true` |  |
| initConfig.catalog[3].items[6].type | string | `"group"` |  |
| initConfig.catalog[3].items[7].isOpen | bool | `false` |  |
| initConfig.catalog[3].items[7].items[0].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[0].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[0].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1979.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1979-01-01T11:00:00Z&time_end=1979-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[0].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[0].name | string | `"ERA5 daily total precipitation 1979"` |  |
| initConfig.catalog[3].items[7].items[0].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[0].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[0].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1979.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].items[10].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[10].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[10].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1989.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1989-01-01T11:00:00Z&time_end=1989-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[10].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[10].name | string | `"ERA5 daily total precipitation 1989"` |  |
| initConfig.catalog[3].items[7].items[10].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[10].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[10].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1989.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].items[11].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[11].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[11].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1990.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1990-01-01T11:00:00Z&time_end=1990-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[11].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[11].name | string | `"ERA5 daily total precipitation 1990"` |  |
| initConfig.catalog[3].items[7].items[11].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[11].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[11].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1990.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].items[12].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[12].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[12].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1991.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1991-01-01T11:00:00Z&time_end=1991-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[12].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[12].name | string | `"ERA5 daily total precipitation 1991"` |  |
| initConfig.catalog[3].items[7].items[12].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[12].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[12].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1991.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].items[13].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[13].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[13].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1992.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1992-01-01T11:00:00Z&time_end=1992-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[13].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[13].name | string | `"ERA5 daily total precipitation 1992"` |  |
| initConfig.catalog[3].items[7].items[13].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[13].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[13].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1992.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].items[14].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[14].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[14].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1993.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1993-01-01T11:00:00Z&time_end=1993-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[14].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[14].name | string | `"ERA5 daily total precipitation 1993"` |  |
| initConfig.catalog[3].items[7].items[14].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[14].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[14].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1993.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].items[15].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[15].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[15].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1994.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1994-01-01T11:00:00Z&time_end=1994-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[15].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[15].name | string | `"ERA5 daily total precipitation 1994"` |  |
| initConfig.catalog[3].items[7].items[15].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[15].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[15].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1994.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].items[16].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[16].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[16].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1995.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1995-01-01T11:00:00Z&time_end=1995-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[16].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[16].name | string | `"ERA5 daily total precipitation 1995"` |  |
| initConfig.catalog[3].items[7].items[16].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[16].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[16].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1995.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].items[17].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[17].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[17].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1996.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1996-01-01T11:00:00Z&time_end=1996-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[17].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[17].name | string | `"ERA5 daily total precipitation 1996"` |  |
| initConfig.catalog[3].items[7].items[17].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[17].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[17].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1996.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].items[18].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[18].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[18].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1997.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1997-01-01T11:00:00Z&time_end=1997-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[18].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[18].name | string | `"ERA5 daily total precipitation 1997"` |  |
| initConfig.catalog[3].items[7].items[18].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[18].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[18].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1997.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].items[19].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[19].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[19].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1998.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1998-01-01T11:00:00Z&time_end=1998-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[19].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[19].name | string | `"ERA5 daily total precipitation 1998"` |  |
| initConfig.catalog[3].items[7].items[19].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[19].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[19].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1998.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].items[1].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[1].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[1].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1980.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1980-01-01T11:00:00Z&time_end=1980-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[1].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[1].name | string | `"ERA5 daily total precipitation 1980"` |  |
| initConfig.catalog[3].items[7].items[1].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[1].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[1].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1980.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].items[20].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[20].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[20].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1999.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1999-01-01T11:00:00Z&time_end=1999-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[20].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[20].name | string | `"ERA5 daily total precipitation 1999"` |  |
| initConfig.catalog[3].items[7].items[20].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[20].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[20].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1999.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].items[21].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[21].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[21].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_2000.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2000-01-01T11:00:00Z&time_end=2000-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[21].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[21].name | string | `"ERA5 daily total precipitation 2000"` |  |
| initConfig.catalog[3].items[7].items[21].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[21].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[21].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_2000.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].items[22].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[22].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[22].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_2001.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2001-01-01T11:00:00Z&time_end=2001-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[22].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[22].name | string | `"ERA5 daily total precipitation 2001"` |  |
| initConfig.catalog[3].items[7].items[22].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[22].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[22].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_2001.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].items[23].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[23].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[23].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_2002.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2002-01-01T11:00:00Z&time_end=2002-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[23].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[23].name | string | `"ERA5 daily total precipitation 2002"` |  |
| initConfig.catalog[3].items[7].items[23].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[23].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[23].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_2002.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].items[24].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[24].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[24].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_2003.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2003-01-01T11:00:00Z&time_end=2003-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[24].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[24].name | string | `"ERA5 daily total precipitation 2003"` |  |
| initConfig.catalog[3].items[7].items[24].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[24].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[24].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_2003.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].items[25].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[25].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[25].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_2004.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2004-01-01T11:00:00Z&time_end=2004-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[25].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[25].name | string | `"ERA5 daily total precipitation 2004"` |  |
| initConfig.catalog[3].items[7].items[25].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[25].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[25].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_2004.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].items[26].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[26].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[26].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_2005.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2005-01-01T11:00:00Z&time_end=2005-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[26].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[26].name | string | `"ERA5 daily total precipitation 2005"` |  |
| initConfig.catalog[3].items[7].items[26].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[26].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[26].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_2005.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].items[27].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[27].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[27].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_2006.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2006-01-01T11:00:00Z&time_end=2006-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[27].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[27].name | string | `"ERA5 daily total precipitation 2006"` |  |
| initConfig.catalog[3].items[7].items[27].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[27].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[27].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_2006.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].items[28].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[28].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[28].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_2007.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2007-01-01T11:00:00Z&time_end=2007-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[28].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[28].name | string | `"ERA5 daily total precipitation 2007"` |  |
| initConfig.catalog[3].items[7].items[28].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[28].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[28].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_2007.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].items[29].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[29].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[29].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_2008.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2008-01-01T11:00:00Z&time_end=2008-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[29].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[29].name | string | `"ERA5 daily total precipitation 2008"` |  |
| initConfig.catalog[3].items[7].items[29].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[29].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[29].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_2008.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].items[2].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[2].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[2].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1981.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1981-01-01T11:00:00Z&time_end=1981-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[2].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[2].name | string | `"ERA5 daily total precipitation 1981"` |  |
| initConfig.catalog[3].items[7].items[2].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[2].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[2].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1981.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].items[30].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[30].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[30].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_2009.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2009-01-01T11:00:00Z&time_end=2009-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[30].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[30].name | string | `"ERA5 daily total precipitation 2009"` |  |
| initConfig.catalog[3].items[7].items[30].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[30].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[30].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_2009.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].items[31].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[31].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[31].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_2010.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2010-01-01T11:00:00Z&time_end=2010-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[31].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[31].name | string | `"ERA5 daily total precipitation 2010"` |  |
| initConfig.catalog[3].items[7].items[31].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[31].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[31].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_2010.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].items[32].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[32].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[32].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_2011.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2011-01-01T11:00:00Z&time_end=2011-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[32].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[32].name | string | `"ERA5 daily total precipitation 2011"` |  |
| initConfig.catalog[3].items[7].items[32].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[32].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[32].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_2011.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].items[33].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[33].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[33].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_2012.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2012-01-01T11:00:00Z&time_end=2012-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[33].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[33].name | string | `"ERA5 daily total precipitation 2012"` |  |
| initConfig.catalog[3].items[7].items[33].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[33].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[33].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_2012.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].items[34].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[34].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[34].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_2013.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2013-01-01T11:00:00Z&time_end=2013-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[34].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[34].name | string | `"ERA5 daily total precipitation 2013"` |  |
| initConfig.catalog[3].items[7].items[34].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[34].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[34].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_2013.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].items[35].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[35].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[35].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_2014.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2014-01-01T11:00:00Z&time_end=2014-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[35].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[35].name | string | `"ERA5 daily total precipitation 2014"` |  |
| initConfig.catalog[3].items[7].items[35].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[35].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[35].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_2014.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].items[36].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[36].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[36].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_2015.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2015-01-01T11:00:00Z&time_end=2015-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[36].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[36].name | string | `"ERA5 daily total precipitation 2015"` |  |
| initConfig.catalog[3].items[7].items[36].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[36].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[36].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_2015.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].items[37].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[37].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[37].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_2016.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2016-01-01T11:00:00Z&time_end=2016-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[37].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[37].name | string | `"ERA5 daily total precipitation 2016"` |  |
| initConfig.catalog[3].items[7].items[37].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[37].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[37].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_2016.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].items[38].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[38].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[38].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_2017.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2017-01-01T11:00:00Z&time_end=2017-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[38].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[38].name | string | `"ERA5 daily total precipitation 2017"` |  |
| initConfig.catalog[3].items[7].items[38].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[38].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[38].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_2017.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].items[39].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[39].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[39].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_2018.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2018-01-01T11:00:00Z&time_end=2018-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[39].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[39].name | string | `"ERA5 daily total precipitation 2018"` |  |
| initConfig.catalog[3].items[7].items[39].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[39].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[39].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_2018.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].items[3].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[3].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[3].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1982.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1982-01-01T11:00:00Z&time_end=1982-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[3].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[3].name | string | `"ERA5 daily total precipitation 1982"` |  |
| initConfig.catalog[3].items[7].items[3].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[3].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[3].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1982.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].items[40].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[40].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[40].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_2019.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2019-01-01T11:00:00Z&time_end=2019-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[40].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[40].name | string | `"ERA5 daily total precipitation 2019"` |  |
| initConfig.catalog[3].items[7].items[40].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[40].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[40].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_2019.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].items[4].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[4].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[4].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1983.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1983-01-01T11:00:00Z&time_end=1983-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[4].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[4].name | string | `"ERA5 daily total precipitation 1983"` |  |
| initConfig.catalog[3].items[7].items[4].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[4].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[4].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1983.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].items[5].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[5].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[5].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1984.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1984-01-01T11:00:00Z&time_end=1984-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[5].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[5].name | string | `"ERA5 daily total precipitation 1984"` |  |
| initConfig.catalog[3].items[7].items[5].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[5].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[5].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1984.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].items[6].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[6].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[6].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1985.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1985-01-01T11:00:00Z&time_end=1985-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[6].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[6].name | string | `"ERA5 daily total precipitation 1985"` |  |
| initConfig.catalog[3].items[7].items[6].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[6].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[6].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1985.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].items[7].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[7].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[7].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1986.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1986-01-01T11:00:00Z&time_end=1986-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[7].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[7].name | string | `"ERA5 daily total precipitation 1986"` |  |
| initConfig.catalog[3].items[7].items[7].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[7].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[7].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1986.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].items[8].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[8].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[8].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1987.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1987-01-01T11:00:00Z&time_end=1987-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[8].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[8].name | string | `"ERA5 daily total precipitation 1987"` |  |
| initConfig.catalog[3].items[7].items[8].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[8].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[8].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1987.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].items[9].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[3].items[7].items[9].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[3].items[7].items[9].featureInfoTemplate | string | `"<p>ERA5 daily total precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1988.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1988-01-01T11:00:00Z&time_end=1988-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[3].items[7].items[9].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[3].items[7].items[9].name | string | `"ERA5 daily total precipitation 1988"` |  |
| initConfig.catalog[3].items[7].items[9].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[3].items[7].items[9].type | string | `"wms"` |  |
| initConfig.catalog[3].items[7].items[9].url | string | `"http://thredds:8080/thredds/wms/ERA5_daily_total_precipitation/ERA5_daily_total_precipitation_1988.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].items[7].name | string | `"ERA5 daily total precipitation"` |  |
| initConfig.catalog[3].items[7].preserveOrder | bool | `true` |  |
| initConfig.catalog[3].items[7].type | string | `"group"` |  |
| initConfig.catalog[3].name | string | `"ERA5 Daily"` |  |
| initConfig.catalog[3].preserveOrder | bool | `true` |  |
| initConfig.catalog[3].type | string | `"group"` |  |
| initConfig.catalog[4].isOpen | bool | `false` |  |
| initConfig.catalog[4].items[0].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[4].items[0].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[4].items[0].featureInfoTemplate | string | `"<p>ERA5 monthly mean 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/monthly/ERA5_monthly_mean_2mTemp_1979_2019.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1979-01-16T11:30:00Z&time_end=2019-12-16T11:30:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[4].items[0].layers | string | `"t2m"` |  |
| initConfig.catalog[4].items[0].name | string | `"ERA5 monthly mean 2mTemp"` |  |
| initConfig.catalog[4].items[0].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[4].items[0].type | string | `"wms"` |  |
| initConfig.catalog[4].items[0].url | string | `"http://thredds:8080/thredds/wms/monthly/ERA5_monthly_mean_2mTemp_1979_2019.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[4].items[1].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[4].items[1].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[4].items[1].featureInfoTemplate | string | `"<p>ERA5 monthly mean RH</p><chart src=\"http://thredds:8080/thredds/ncss/monthly/ERA5_monthly_mean_RH_1979_2019.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1979-01-16T11:30:00Z&time_end=2019-12-16T11:30:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[4].items[1].layers | string | `"t2m"` |  |
| initConfig.catalog[4].items[1].name | string | `"ERA5 monthly mean RH"` |  |
| initConfig.catalog[4].items[1].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[4].items[1].type | string | `"wms"` |  |
| initConfig.catalog[4].items[1].url | string | `"http://thredds:8080/thredds/wms/monthly/ERA5_monthly_mean_RH_1979_2019.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[4].items[2].featureInfoTemplate | string | `"<p>ERA5 monthly mean SST</p><chart src=\"http://thredds:8080/thredds/ncss/monthly/ERA5_monthly_mean_SST_1979_2019.nc?var=sst&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1979-01-16T11:30:00Z&time_end=2019-12-16T11:30:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[4].items[2].layers | string | `"sst"` |  |
| initConfig.catalog[4].items[2].name | string | `"ERA5 monthly mean SST"` |  |
| initConfig.catalog[4].items[2].type | string | `"wms"` |  |
| initConfig.catalog[4].items[2].url | string | `"http://thredds:8080/thredds/wms/monthly/ERA5_monthly_mean_SST_1979_2019.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[4].items[3].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[4].items[3].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[4].items[3].featureInfoTemplate | string | `"<p>ERA5 monthly mean TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/monthly/ERA5_monthly_mean_TotalWind_1979_2019.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1979-01-16T11:30:00Z&time_end=2019-12-16T11:30:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[4].items[3].layers | string | `"u10"` |  |
| initConfig.catalog[4].items[3].name | string | `"ERA5 monthly mean TotalWind"` |  |
| initConfig.catalog[4].items[3].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[4].items[3].type | string | `"wms"` |  |
| initConfig.catalog[4].items[3].url | string | `"http://thredds:8080/thredds/wms/monthly/ERA5_monthly_mean_TotalWind_1979_2019.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[4].items[4].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[4].items[4].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[4].items[4].featureInfoTemplate | string | `"<p>ERA5 monthly mean mslp</p><chart src=\"http://thredds:8080/thredds/ncss/monthly/ERA5_monthly_mean_mslp_1979_2019.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1979-01-16T11:30:00Z&time_end=2019-12-16T11:30:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[4].items[4].layers | string | `"msl"` |  |
| initConfig.catalog[4].items[4].name | string | `"ERA5 monthly mean mslp"` |  |
| initConfig.catalog[4].items[4].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[4].items[4].type | string | `"wms"` |  |
| initConfig.catalog[4].items[4].url | string | `"http://thredds:8080/thredds/wms/monthly/ERA5_monthly_mean_mslp_1979_2019.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[4].items[5].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[4].items[5].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[4].items[5].featureInfoTemplate | string | `"<p>ERA5 monthly mean soil temp L1</p><chart src=\"http://thredds:8080/thredds/ncss/monthly/ERA5_monthly_mean_soil_temp_L1_1979_2019.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1979-01-16T11:30:00Z&time_end=2019-12-16T11:30:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[4].items[5].layers | string | `"stl1"` |  |
| initConfig.catalog[4].items[5].name | string | `"ERA5 monthly mean soil temp L1"` |  |
| initConfig.catalog[4].items[5].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[4].items[5].type | string | `"wms"` |  |
| initConfig.catalog[4].items[5].url | string | `"http://thredds:8080/thredds/wms/monthly/ERA5_monthly_mean_soil_temp_L1_1979_2019.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[4].items[6].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[4].items[6].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[4].items[6].featureInfoTemplate | string | `"<p>ERA5 monthly mean soil water L1</p><chart src=\"http://thredds:8080/thredds/ncss/monthly/ERA5_monthly_mean_soil_water_L1_1979_2019.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1979-01-16T11:30:00Z&time_end=2019-12-16T11:30:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[4].items[6].layers | string | `"swvl1"` |  |
| initConfig.catalog[4].items[6].name | string | `"ERA5 monthly mean soil water L1"` |  |
| initConfig.catalog[4].items[6].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[4].items[6].type | string | `"wms"` |  |
| initConfig.catalog[4].items[6].url | string | `"http://thredds:8080/thredds/wms/monthly/ERA5_monthly_mean_soil_water_L1_1979_2019.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[4].items[7].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[4].items[7].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[4].items[7].featureInfoTemplate | string | `"<p>ERA5 monthly mean sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/monthly/ERA5_monthly_mean_sol_rad_1979_2019.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1979-01-16T11:30:00Z&time_end=2019-12-16T11:30:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[4].items[7].layers | string | `"ssr"` |  |
| initConfig.catalog[4].items[7].name | string | `"ERA5 monthly mean sol rad"` |  |
| initConfig.catalog[4].items[7].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[4].items[7].type | string | `"wms"` |  |
| initConfig.catalog[4].items[7].url | string | `"http://thredds:8080/thredds/wms/monthly/ERA5_monthly_mean_sol_rad_1979_2019.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[4].items[8].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[4].items[8].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[4].items[8].featureInfoTemplate | string | `"<p>ERA5 monthly precipitation</p><chart src=\"http://thredds:8080/thredds/ncss/monthly/ERA5_monthly_precipitation_1979_2019.nc?var=tp&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1979-01-16T11:30:00Z&time_end=2019-12-16T11:30:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[4].items[8].layers | string | `"tp"` |  |
| initConfig.catalog[4].items[8].name | string | `"ERA5 monthly precipitation"` |  |
| initConfig.catalog[4].items[8].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[4].items[8].type | string | `"wms"` |  |
| initConfig.catalog[4].items[8].url | string | `"http://thredds:8080/thredds/wms/monthly/ERA5_monthly_precipitation_1979_2019.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[4].name | string | `"ERA5 Monthly"` |  |
| initConfig.catalog[4].preserveOrder | bool | `true` |  |
| initConfig.catalog[4].type | string | `"group"` |  |
| initConfig.catalog[5].isOpen | bool | `false` |  |
| initConfig.catalog[5].items[0].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[5].items[0].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[5].items[0].featureInfoTemplate | string | `"<p>ERA5 30year 2mTemp</p><chart src=\"http://thredds:8080/thredds/ncss/30year/ERA5_30year_2mTemp.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1979-01-16T11:30:00Z&time_end=2019-12-16T11:30:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[5].items[0].layers | string | `"t2m"` |  |
| initConfig.catalog[5].items[0].name | string | `"ERA5 30year 2mTemp"` |  |
| initConfig.catalog[5].items[0].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[5].items[0].type | string | `"wms"` |  |
| initConfig.catalog[5].items[0].url | string | `"http://thredds:8080/thredds/wms/30year/ERA5_30year_2mTemp.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[5].items[1].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[5].items[1].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[5].items[1].featureInfoTemplate | string | `"<p>ERA5 30year RH</p><chart src=\"http://thredds:8080/thredds/ncss/30year/ERA5_30year_RH.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1979-01-16T11:30:00Z&time_end=2019-12-16T11:30:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[5].items[1].layers | string | `"t2m"` |  |
| initConfig.catalog[5].items[1].name | string | `"ERA5 30year RH"` |  |
| initConfig.catalog[5].items[1].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[5].items[1].type | string | `"wms"` |  |
| initConfig.catalog[5].items[1].url | string | `"http://thredds:8080/thredds/wms/30year/ERA5_30year_RH.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[5].items[2].featureInfoTemplate | string | `"<p>ERA5 30year SST</p><chart src=\"http://thredds:8080/thredds/ncss/30year/ERA5_30year_SST.nc?var=sst&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1979-01-16T11:30:00Z&time_end=2019-12-16T11:30:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[5].items[2].layers | string | `"sst"` |  |
| initConfig.catalog[5].items[2].name | string | `"ERA5 30year SST"` |  |
| initConfig.catalog[5].items[2].type | string | `"wms"` |  |
| initConfig.catalog[5].items[2].url | string | `"http://thredds:8080/thredds/wms/30year/ERA5_30year_SST.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[5].items[3].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[5].items[3].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[5].items[3].featureInfoTemplate | string | `"<p>ERA5 30year TotalWind</p><chart src=\"http://thredds:8080/thredds/ncss/30year/ERA5_30year_TotalWind.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1979-01-16T11:30:00Z&time_end=2019-12-16T11:30:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[5].items[3].layers | string | `"u10"` |  |
| initConfig.catalog[5].items[3].name | string | `"ERA5 30year TotalWind"` |  |
| initConfig.catalog[5].items[3].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[5].items[3].type | string | `"wms"` |  |
| initConfig.catalog[5].items[3].url | string | `"http://thredds:8080/thredds/wms/30year/ERA5_30year_TotalWind.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[5].items[4].colorScaleMaximum | int | `104000` |  |
| initConfig.catalog[5].items[4].colorScaleMinimum | int | `96500` |  |
| initConfig.catalog[5].items[4].featureInfoTemplate | string | `"<p>ERA5 30year mslp</p><chart src=\"http://thredds:8080/thredds/ncss/30year/ERA5_30year_mslp.nc?var=msl&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1979-01-16T11:30:00Z&time_end=2019-12-16T11:30:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[5].items[4].layers | string | `"msl"` |  |
| initConfig.catalog[5].items[4].name | string | `"ERA5 30year mslp"` |  |
| initConfig.catalog[5].items[4].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[5].items[4].type | string | `"wms"` |  |
| initConfig.catalog[5].items[4].url | string | `"http://thredds:8080/thredds/wms/30year/ERA5_30year_mslp.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[5].items[5].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[5].items[5].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[5].items[5].featureInfoTemplate | string | `"<p>ERA5 30year soil temp 1</p><chart src=\"http://thredds:8080/thredds/ncss/30year/ERA5_30year_soil_temp_1.nc?var=stl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1979-01-16T11:30:00Z&time_end=2019-12-16T11:30:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[5].items[5].layers | string | `"stl1"` |  |
| initConfig.catalog[5].items[5].name | string | `"ERA5 30year soil temp 1"` |  |
| initConfig.catalog[5].items[5].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[5].items[5].type | string | `"wms"` |  |
| initConfig.catalog[5].items[5].url | string | `"http://thredds:8080/thredds/wms/30year/ERA5_30year_soil_temp_1.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[5].items[6].colorScaleMaximum | int | `1` |  |
| initConfig.catalog[5].items[6].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[5].items[6].featureInfoTemplate | string | `"<p>ERA5 30year soil water 1</p><chart src=\"http://thredds:8080/thredds/ncss/30year/ERA5_30year_soil_water_1.nc?var=swvl1&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1979-01-16T11:30:00Z&time_end=2019-12-16T11:30:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[5].items[6].layers | string | `"swvl1"` |  |
| initConfig.catalog[5].items[6].name | string | `"ERA5 30year soil water 1"` |  |
| initConfig.catalog[5].items[6].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[5].items[6].type | string | `"wms"` |  |
| initConfig.catalog[5].items[6].url | string | `"http://thredds:8080/thredds/wms/30year/ERA5_30year_soil_water_1.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[5].items[7].colorScaleMaximum | int | `1291000` |  |
| initConfig.catalog[5].items[7].colorScaleMinimum | int | `25860` |  |
| initConfig.catalog[5].items[7].featureInfoTemplate | string | `"<p>ERA5 30year sol rad</p><chart src=\"http://thredds:8080/thredds/ncss/30year/ERA5_30year_sol_rad.nc?var=ssr&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1979-01-16T11:30:00Z&time_end=2019-12-16T11:30:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[5].items[7].layers | string | `"ssr"` |  |
| initConfig.catalog[5].items[7].name | string | `"ERA5 30year sol rad"` |  |
| initConfig.catalog[5].items[7].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[5].items[7].type | string | `"wms"` |  |
| initConfig.catalog[5].items[7].url | string | `"http://thredds:8080/thredds/wms/30year/ERA5_30year_sol_rad.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[5].items[8].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[5].items[8].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[5].items[8].featureInfoTemplate | string | `"<p>ERA5 30year TotalPrecip</p><chart src=\"http://thredds:8080/thredds/ncss/30year/ERA5_30year_TotalPrecip.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1979-01-16T11:30:00Z&time_end=2019-12-16T11:30:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[5].items[8].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[5].items[8].name | string | `"ERA5 30year TotalPrecip"` |  |
| initConfig.catalog[5].items[8].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[5].items[8].type | string | `"wms"` |  |
| initConfig.catalog[5].items[8].url | string | `"http://thredds:8080/thredds/wms/30year/ERA5_30year_TotalPrecip.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[5].name | string | `"ERA5 30year Average"` |  |
| initConfig.catalog[5].preserveOrder | bool | `true` |  |
| initConfig.catalog[5].type | string | `"group"` |  |
| initConfig.catalog[6].isOpen | bool | `false` |  |
| initConfig.catalog[6].items[0].isOpen | bool | `false` |  |
| initConfig.catalog[6].items[0].items[0].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[6].items[0].items[0].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[6].items[0].items[0].featureInfoTemplate | string | `"<p>ERA5-Land daily mean 2mTemp 1981</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_1981.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1981-01-01T11:00:00Z&time_end=1981-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[0].items[0].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[0].items[0].name | string | `"ERA5-Land daily mean 2mTemp 1981"` |  |
| initConfig.catalog[6].items[0].items[0].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[6].items[0].items[0].type | string | `"wms"` |  |
| initConfig.catalog[6].items[0].items[0].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_1981.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[0].items[10].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[6].items[0].items[10].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[6].items[0].items[10].featureInfoTemplate | string | `"<p>ERA5-Land daily mean 2mTemp 1991</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_1991.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1991-01-01T11:00:00Z&time_end=1991-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[0].items[10].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[0].items[10].name | string | `"ERA5-Land daily mean 2mTemp 1991"` |  |
| initConfig.catalog[6].items[0].items[10].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[6].items[0].items[10].type | string | `"wms"` |  |
| initConfig.catalog[6].items[0].items[10].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_1991.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[0].items[11].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[6].items[0].items[11].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[6].items[0].items[11].featureInfoTemplate | string | `"<p>ERA5-Land daily mean 2mTemp 1992</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_1992.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1992-01-01T11:00:00Z&time_end=1992-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[0].items[11].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[0].items[11].name | string | `"ERA5-Land daily mean 2mTemp 1992"` |  |
| initConfig.catalog[6].items[0].items[11].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[6].items[0].items[11].type | string | `"wms"` |  |
| initConfig.catalog[6].items[0].items[11].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_1992.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[0].items[12].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[6].items[0].items[12].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[6].items[0].items[12].featureInfoTemplate | string | `"<p>ERA5-Land daily mean 2mTemp 1993</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_1993.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1993-01-01T11:00:00Z&time_end=1993-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[0].items[12].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[0].items[12].name | string | `"ERA5-Land daily mean 2mTemp 1993"` |  |
| initConfig.catalog[6].items[0].items[12].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[6].items[0].items[12].type | string | `"wms"` |  |
| initConfig.catalog[6].items[0].items[12].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_1993.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[0].items[13].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[6].items[0].items[13].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[6].items[0].items[13].featureInfoTemplate | string | `"<p>ERA5-Land daily mean 2mTemp 1994</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_1994.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1994-01-01T11:00:00Z&time_end=1994-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[0].items[13].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[0].items[13].name | string | `"ERA5-Land daily mean 2mTemp 1994"` |  |
| initConfig.catalog[6].items[0].items[13].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[6].items[0].items[13].type | string | `"wms"` |  |
| initConfig.catalog[6].items[0].items[13].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_1994.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[0].items[14].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[6].items[0].items[14].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[6].items[0].items[14].featureInfoTemplate | string | `"<p>ERA5-Land daily mean 2mTemp 1995</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_1995.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1995-01-01T11:00:00Z&time_end=1995-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[0].items[14].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[0].items[14].name | string | `"ERA5-Land daily mean 2mTemp 1995"` |  |
| initConfig.catalog[6].items[0].items[14].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[6].items[0].items[14].type | string | `"wms"` |  |
| initConfig.catalog[6].items[0].items[14].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_1995.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[0].items[15].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[6].items[0].items[15].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[6].items[0].items[15].featureInfoTemplate | string | `"<p>ERA5-Land daily mean 2mTemp 1996</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_1996.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1996-01-01T11:00:00Z&time_end=1996-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[0].items[15].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[0].items[15].name | string | `"ERA5-Land daily mean 2mTemp 1996"` |  |
| initConfig.catalog[6].items[0].items[15].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[6].items[0].items[15].type | string | `"wms"` |  |
| initConfig.catalog[6].items[0].items[15].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_1996.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[0].items[16].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[6].items[0].items[16].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[6].items[0].items[16].featureInfoTemplate | string | `"<p>ERA5-Land daily mean 2mTemp 1997</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_1997.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1997-01-01T11:00:00Z&time_end=1997-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[0].items[16].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[0].items[16].name | string | `"ERA5-Land daily mean 2mTemp 1997"` |  |
| initConfig.catalog[6].items[0].items[16].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[6].items[0].items[16].type | string | `"wms"` |  |
| initConfig.catalog[6].items[0].items[16].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_1997.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[0].items[17].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[6].items[0].items[17].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[6].items[0].items[17].featureInfoTemplate | string | `"<p>ERA5-Land daily mean 2mTemp 1998</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_1998.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1998-01-01T11:00:00Z&time_end=1998-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[0].items[17].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[0].items[17].name | string | `"ERA5-Land daily mean 2mTemp 1998"` |  |
| initConfig.catalog[6].items[0].items[17].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[6].items[0].items[17].type | string | `"wms"` |  |
| initConfig.catalog[6].items[0].items[17].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_1998.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[0].items[18].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[6].items[0].items[18].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[6].items[0].items[18].featureInfoTemplate | string | `"<p>ERA5-Land daily mean 2mTemp 1999</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_1999.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1999-01-01T11:00:00Z&time_end=1999-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[0].items[18].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[0].items[18].name | string | `"ERA5-Land daily mean 2mTemp 1999"` |  |
| initConfig.catalog[6].items[0].items[18].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[6].items[0].items[18].type | string | `"wms"` |  |
| initConfig.catalog[6].items[0].items[18].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_1999.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[0].items[19].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[6].items[0].items[19].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[6].items[0].items[19].featureInfoTemplate | string | `"<p>ERA5-Land daily mean 2mTemp 2000</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_2000.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2000-01-01T11:00:00Z&time_end=2000-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[0].items[19].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[0].items[19].name | string | `"ERA5-Land daily mean 2mTemp 2000"` |  |
| initConfig.catalog[6].items[0].items[19].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[6].items[0].items[19].type | string | `"wms"` |  |
| initConfig.catalog[6].items[0].items[19].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_2000.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[0].items[1].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[6].items[0].items[1].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[6].items[0].items[1].featureInfoTemplate | string | `"<p>ERA5-Land daily mean 2mTemp 1982</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_1982.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1982-01-01T11:00:00Z&time_end=1982-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[0].items[1].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[0].items[1].name | string | `"ERA5-Land daily mean 2mTemp 1982"` |  |
| initConfig.catalog[6].items[0].items[1].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[6].items[0].items[1].type | string | `"wms"` |  |
| initConfig.catalog[6].items[0].items[1].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_1982.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[0].items[20].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[6].items[0].items[20].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[6].items[0].items[20].featureInfoTemplate | string | `"<p>ERA5-Land daily mean 2mTemp 2001</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_2001.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2001-01-01T11:00:00Z&time_end=2001-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[0].items[20].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[0].items[20].name | string | `"ERA5-Land daily mean 2mTemp 2001"` |  |
| initConfig.catalog[6].items[0].items[20].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[6].items[0].items[20].type | string | `"wms"` |  |
| initConfig.catalog[6].items[0].items[20].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_2001.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[0].items[21].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[6].items[0].items[21].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[6].items[0].items[21].featureInfoTemplate | string | `"<p>ERA5-Land daily mean 2mTemp 2002</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_2002.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2002-01-01T11:00:00Z&time_end=2002-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[0].items[21].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[0].items[21].name | string | `"ERA5-Land daily mean 2mTemp 2002"` |  |
| initConfig.catalog[6].items[0].items[21].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[6].items[0].items[21].type | string | `"wms"` |  |
| initConfig.catalog[6].items[0].items[21].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_2002.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[0].items[22].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[6].items[0].items[22].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[6].items[0].items[22].featureInfoTemplate | string | `"<p>ERA5-Land daily mean 2mTemp 2003</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_2003.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2003-01-01T11:00:00Z&time_end=2003-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[0].items[22].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[0].items[22].name | string | `"ERA5-Land daily mean 2mTemp 2003"` |  |
| initConfig.catalog[6].items[0].items[22].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[6].items[0].items[22].type | string | `"wms"` |  |
| initConfig.catalog[6].items[0].items[22].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_2003.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[0].items[23].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[6].items[0].items[23].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[6].items[0].items[23].featureInfoTemplate | string | `"<p>ERA5-Land daily mean 2mTemp 2004</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_2004.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2004-01-01T11:00:00Z&time_end=2004-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[0].items[23].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[0].items[23].name | string | `"ERA5-Land daily mean 2mTemp 2004"` |  |
| initConfig.catalog[6].items[0].items[23].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[6].items[0].items[23].type | string | `"wms"` |  |
| initConfig.catalog[6].items[0].items[23].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_2004.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[0].items[24].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[6].items[0].items[24].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[6].items[0].items[24].featureInfoTemplate | string | `"<p>ERA5-Land daily mean 2mTemp 2005</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_2005.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2005-01-01T11:00:00Z&time_end=2005-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[0].items[24].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[0].items[24].name | string | `"ERA5-Land daily mean 2mTemp 2005"` |  |
| initConfig.catalog[6].items[0].items[24].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[6].items[0].items[24].type | string | `"wms"` |  |
| initConfig.catalog[6].items[0].items[24].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_2005.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[0].items[25].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[6].items[0].items[25].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[6].items[0].items[25].featureInfoTemplate | string | `"<p>ERA5-Land daily mean 2mTemp 2006</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_2006.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2006-01-01T11:00:00Z&time_end=2006-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[0].items[25].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[0].items[25].name | string | `"ERA5-Land daily mean 2mTemp 2006"` |  |
| initConfig.catalog[6].items[0].items[25].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[6].items[0].items[25].type | string | `"wms"` |  |
| initConfig.catalog[6].items[0].items[25].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_2006.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[0].items[26].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[6].items[0].items[26].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[6].items[0].items[26].featureInfoTemplate | string | `"<p>ERA5-Land daily mean 2mTemp 2007</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_2007.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2007-01-01T11:00:00Z&time_end=2007-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[0].items[26].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[0].items[26].name | string | `"ERA5-Land daily mean 2mTemp 2007"` |  |
| initConfig.catalog[6].items[0].items[26].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[6].items[0].items[26].type | string | `"wms"` |  |
| initConfig.catalog[6].items[0].items[26].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_2007.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[0].items[27].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[6].items[0].items[27].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[6].items[0].items[27].featureInfoTemplate | string | `"<p>ERA5-Land daily mean 2mTemp 2008</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_2008.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2008-01-01T11:00:00Z&time_end=2008-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[0].items[27].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[0].items[27].name | string | `"ERA5-Land daily mean 2mTemp 2008"` |  |
| initConfig.catalog[6].items[0].items[27].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[6].items[0].items[27].type | string | `"wms"` |  |
| initConfig.catalog[6].items[0].items[27].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_2008.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[0].items[28].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[6].items[0].items[28].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[6].items[0].items[28].featureInfoTemplate | string | `"<p>ERA5-Land daily mean 2mTemp 2009</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_2009.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2009-01-01T11:00:00Z&time_end=2009-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[0].items[28].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[0].items[28].name | string | `"ERA5-Land daily mean 2mTemp 2009"` |  |
| initConfig.catalog[6].items[0].items[28].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[6].items[0].items[28].type | string | `"wms"` |  |
| initConfig.catalog[6].items[0].items[28].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_2009.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[0].items[29].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[6].items[0].items[29].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[6].items[0].items[29].featureInfoTemplate | string | `"<p>ERA5-Land daily mean 2mTemp 2010</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_2010.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2010-01-01T11:00:00Z&time_end=2010-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[0].items[29].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[0].items[29].name | string | `"ERA5-Land daily mean 2mTemp 2010"` |  |
| initConfig.catalog[6].items[0].items[29].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[6].items[0].items[29].type | string | `"wms"` |  |
| initConfig.catalog[6].items[0].items[29].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_2010.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[0].items[2].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[6].items[0].items[2].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[6].items[0].items[2].featureInfoTemplate | string | `"<p>ERA5-Land daily mean 2mTemp 1983</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_1983.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1983-01-01T11:00:00Z&time_end=1983-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[0].items[2].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[0].items[2].name | string | `"ERA5-Land daily mean 2mTemp 1983"` |  |
| initConfig.catalog[6].items[0].items[2].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[6].items[0].items[2].type | string | `"wms"` |  |
| initConfig.catalog[6].items[0].items[2].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_1983.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[0].items[30].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[6].items[0].items[30].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[6].items[0].items[30].featureInfoTemplate | string | `"<p>ERA5-Land daily mean 2mTemp 2011</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_2011.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2011-01-01T11:00:00Z&time_end=2011-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[0].items[30].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[0].items[30].name | string | `"ERA5-Land daily mean 2mTemp 2011"` |  |
| initConfig.catalog[6].items[0].items[30].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[6].items[0].items[30].type | string | `"wms"` |  |
| initConfig.catalog[6].items[0].items[30].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_2011.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[0].items[31].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[6].items[0].items[31].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[6].items[0].items[31].featureInfoTemplate | string | `"<p>ERA5-Land daily mean 2mTemp 2012</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_2012.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2012-01-01T11:00:00Z&time_end=2012-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[0].items[31].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[0].items[31].name | string | `"ERA5-Land daily mean 2mTemp 2012"` |  |
| initConfig.catalog[6].items[0].items[31].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[6].items[0].items[31].type | string | `"wms"` |  |
| initConfig.catalog[6].items[0].items[31].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_2012.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[0].items[32].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[6].items[0].items[32].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[6].items[0].items[32].featureInfoTemplate | string | `"<p>ERA5-Land daily mean 2mTemp 2013</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_2013.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2013-01-01T11:00:00Z&time_end=2013-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[0].items[32].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[0].items[32].name | string | `"ERA5-Land daily mean 2mTemp 2013"` |  |
| initConfig.catalog[6].items[0].items[32].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[6].items[0].items[32].type | string | `"wms"` |  |
| initConfig.catalog[6].items[0].items[32].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_2013.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[0].items[33].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[6].items[0].items[33].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[6].items[0].items[33].featureInfoTemplate | string | `"<p>ERA5-Land daily mean 2mTemp 2014</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_2014.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2014-01-01T11:00:00Z&time_end=2014-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[0].items[33].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[0].items[33].name | string | `"ERA5-Land daily mean 2mTemp 2014"` |  |
| initConfig.catalog[6].items[0].items[33].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[6].items[0].items[33].type | string | `"wms"` |  |
| initConfig.catalog[6].items[0].items[33].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_2014.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[0].items[34].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[6].items[0].items[34].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[6].items[0].items[34].featureInfoTemplate | string | `"<p>ERA5-Land daily mean 2mTemp 2015</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_2015.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2015-01-01T11:00:00Z&time_end=2015-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[0].items[34].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[0].items[34].name | string | `"ERA5-Land daily mean 2mTemp 2015"` |  |
| initConfig.catalog[6].items[0].items[34].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[6].items[0].items[34].type | string | `"wms"` |  |
| initConfig.catalog[6].items[0].items[34].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_2015.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[0].items[35].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[6].items[0].items[35].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[6].items[0].items[35].featureInfoTemplate | string | `"<p>ERA5-Land daily mean 2mTemp 2016</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_2016.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2016-01-01T11:00:00Z&time_end=2016-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[0].items[35].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[0].items[35].name | string | `"ERA5-Land daily mean 2mTemp 2016"` |  |
| initConfig.catalog[6].items[0].items[35].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[6].items[0].items[35].type | string | `"wms"` |  |
| initConfig.catalog[6].items[0].items[35].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_2016.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[0].items[36].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[6].items[0].items[36].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[6].items[0].items[36].featureInfoTemplate | string | `"<p>ERA5-Land daily mean 2mTemp 2017</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_2017.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2017-01-01T11:00:00Z&time_end=2017-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[0].items[36].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[0].items[36].name | string | `"ERA5-Land daily mean 2mTemp 2017"` |  |
| initConfig.catalog[6].items[0].items[36].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[6].items[0].items[36].type | string | `"wms"` |  |
| initConfig.catalog[6].items[0].items[36].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_2017.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[0].items[37].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[6].items[0].items[37].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[6].items[0].items[37].featureInfoTemplate | string | `"<p>ERA5-Land daily mean 2mTemp 2018</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_2018.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2018-01-01T11:00:00Z&time_end=2018-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[0].items[37].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[0].items[37].name | string | `"ERA5-Land daily mean 2mTemp 2018"` |  |
| initConfig.catalog[6].items[0].items[37].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[6].items[0].items[37].type | string | `"wms"` |  |
| initConfig.catalog[6].items[0].items[37].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_2018.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[0].items[38].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[6].items[0].items[38].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[6].items[0].items[38].featureInfoTemplate | string | `"<p>ERA5-Land daily mean 2mTemp 2019</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_2019.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2019-01-01T11:00:00Z&time_end=2019-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[0].items[38].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[0].items[38].name | string | `"ERA5-Land daily mean 2mTemp 2019"` |  |
| initConfig.catalog[6].items[0].items[38].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[6].items[0].items[38].type | string | `"wms"` |  |
| initConfig.catalog[6].items[0].items[38].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_2019.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[0].items[3].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[6].items[0].items[3].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[6].items[0].items[3].featureInfoTemplate | string | `"<p>ERA5-Land daily mean 2mTemp 1984</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_1984.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1984-01-01T11:00:00Z&time_end=1984-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[0].items[3].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[0].items[3].name | string | `"ERA5-Land daily mean 2mTemp 1984"` |  |
| initConfig.catalog[6].items[0].items[3].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[6].items[0].items[3].type | string | `"wms"` |  |
| initConfig.catalog[6].items[0].items[3].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_1984.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[0].items[4].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[6].items[0].items[4].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[6].items[0].items[4].featureInfoTemplate | string | `"<p>ERA5-Land daily mean 2mTemp 1985</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_1985.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1985-01-01T11:00:00Z&time_end=1985-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[0].items[4].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[0].items[4].name | string | `"ERA5-Land daily mean 2mTemp 1985"` |  |
| initConfig.catalog[6].items[0].items[4].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[6].items[0].items[4].type | string | `"wms"` |  |
| initConfig.catalog[6].items[0].items[4].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_1985.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[0].items[5].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[6].items[0].items[5].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[6].items[0].items[5].featureInfoTemplate | string | `"<p>ERA5-Land daily mean 2mTemp 1986</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_1986.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1986-01-01T11:00:00Z&time_end=1986-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[0].items[5].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[0].items[5].name | string | `"ERA5-Land daily mean 2mTemp 1986"` |  |
| initConfig.catalog[6].items[0].items[5].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[6].items[0].items[5].type | string | `"wms"` |  |
| initConfig.catalog[6].items[0].items[5].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_1986.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[0].items[6].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[6].items[0].items[6].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[6].items[0].items[6].featureInfoTemplate | string | `"<p>ERA5-Land daily mean 2mTemp 1987</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_1987.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1987-01-01T11:00:00Z&time_end=1987-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[0].items[6].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[0].items[6].name | string | `"ERA5-Land daily mean 2mTemp 1987"` |  |
| initConfig.catalog[6].items[0].items[6].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[6].items[0].items[6].type | string | `"wms"` |  |
| initConfig.catalog[6].items[0].items[6].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_1987.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[0].items[7].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[6].items[0].items[7].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[6].items[0].items[7].featureInfoTemplate | string | `"<p>ERA5-Land daily mean 2mTemp 1988</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_1988.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1988-01-01T11:00:00Z&time_end=1988-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[0].items[7].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[0].items[7].name | string | `"ERA5-Land daily mean 2mTemp 1988"` |  |
| initConfig.catalog[6].items[0].items[7].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[6].items[0].items[7].type | string | `"wms"` |  |
| initConfig.catalog[6].items[0].items[7].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_1988.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[0].items[8].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[6].items[0].items[8].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[6].items[0].items[8].featureInfoTemplate | string | `"<p>ERA5-Land daily mean 2mTemp 1989</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_1989.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1989-01-01T11:00:00Z&time_end=1989-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[0].items[8].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[0].items[8].name | string | `"ERA5-Land daily mean 2mTemp 1989"` |  |
| initConfig.catalog[6].items[0].items[8].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[6].items[0].items[8].type | string | `"wms"` |  |
| initConfig.catalog[6].items[0].items[8].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_1989.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[0].items[9].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[6].items[0].items[9].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[6].items[0].items[9].featureInfoTemplate | string | `"<p>ERA5-Land daily mean 2mTemp 1990</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_1990.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1990-01-01T11:00:00Z&time_end=1990-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[0].items[9].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[0].items[9].name | string | `"ERA5-Land daily mean 2mTemp 1990"` |  |
| initConfig.catalog[6].items[0].items[9].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[6].items[0].items[9].type | string | `"wms"` |  |
| initConfig.catalog[6].items[0].items[9].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_2mTemp/ERA5-Land_daily_mean_2mTemp_1990.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[0].name | string | `"ERA5-Land daily mean 2mTemp"` |  |
| initConfig.catalog[6].items[0].preserveOrder | bool | `true` |  |
| initConfig.catalog[6].items[0].type | string | `"group"` |  |
| initConfig.catalog[6].items[1].isOpen | bool | `false` |  |
| initConfig.catalog[6].items[1].items[0].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[6].items[1].items[0].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[1].items[0].featureInfoTemplate | string | `"<p>ERA5-Land daily mean RH 1981</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_1981.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1981-01-01T11:00:00Z&time_end=1981-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[1].items[0].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[1].items[0].name | string | `"ERA5-Land daily mean RH 1981"` |  |
| initConfig.catalog[6].items[1].items[0].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[6].items[1].items[0].type | string | `"wms"` |  |
| initConfig.catalog[6].items[1].items[0].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_1981.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[1].items[10].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[6].items[1].items[10].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[1].items[10].featureInfoTemplate | string | `"<p>ERA5-Land daily mean RH 1991</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_1991.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1991-01-01T11:00:00Z&time_end=1991-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[1].items[10].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[1].items[10].name | string | `"ERA5-Land daily mean RH 1991"` |  |
| initConfig.catalog[6].items[1].items[10].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[6].items[1].items[10].type | string | `"wms"` |  |
| initConfig.catalog[6].items[1].items[10].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_1991.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[1].items[11].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[6].items[1].items[11].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[1].items[11].featureInfoTemplate | string | `"<p>ERA5-Land daily mean RH 1992</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_1992.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1992-01-01T11:00:00Z&time_end=1992-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[1].items[11].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[1].items[11].name | string | `"ERA5-Land daily mean RH 1992"` |  |
| initConfig.catalog[6].items[1].items[11].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[6].items[1].items[11].type | string | `"wms"` |  |
| initConfig.catalog[6].items[1].items[11].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_1992.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[1].items[12].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[6].items[1].items[12].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[1].items[12].featureInfoTemplate | string | `"<p>ERA5-Land daily mean RH 1993</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_1993.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1993-01-01T11:00:00Z&time_end=1993-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[1].items[12].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[1].items[12].name | string | `"ERA5-Land daily mean RH 1993"` |  |
| initConfig.catalog[6].items[1].items[12].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[6].items[1].items[12].type | string | `"wms"` |  |
| initConfig.catalog[6].items[1].items[12].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_1993.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[1].items[13].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[6].items[1].items[13].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[1].items[13].featureInfoTemplate | string | `"<p>ERA5-Land daily mean RH 1994</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_1994.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1994-01-01T11:00:00Z&time_end=1994-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[1].items[13].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[1].items[13].name | string | `"ERA5-Land daily mean RH 1994"` |  |
| initConfig.catalog[6].items[1].items[13].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[6].items[1].items[13].type | string | `"wms"` |  |
| initConfig.catalog[6].items[1].items[13].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_1994.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[1].items[14].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[6].items[1].items[14].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[1].items[14].featureInfoTemplate | string | `"<p>ERA5-Land daily mean RH 1995</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_1995.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1995-01-01T11:00:00Z&time_end=1995-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[1].items[14].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[1].items[14].name | string | `"ERA5-Land daily mean RH 1995"` |  |
| initConfig.catalog[6].items[1].items[14].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[6].items[1].items[14].type | string | `"wms"` |  |
| initConfig.catalog[6].items[1].items[14].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_1995.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[1].items[15].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[6].items[1].items[15].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[1].items[15].featureInfoTemplate | string | `"<p>ERA5-Land daily mean RH 1996</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_1996.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1996-01-01T11:00:00Z&time_end=1996-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[1].items[15].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[1].items[15].name | string | `"ERA5-Land daily mean RH 1996"` |  |
| initConfig.catalog[6].items[1].items[15].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[6].items[1].items[15].type | string | `"wms"` |  |
| initConfig.catalog[6].items[1].items[15].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_1996.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[1].items[16].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[6].items[1].items[16].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[1].items[16].featureInfoTemplate | string | `"<p>ERA5-Land daily mean RH 1997</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_1997.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1997-01-01T11:00:00Z&time_end=1997-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[1].items[16].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[1].items[16].name | string | `"ERA5-Land daily mean RH 1997"` |  |
| initConfig.catalog[6].items[1].items[16].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[6].items[1].items[16].type | string | `"wms"` |  |
| initConfig.catalog[6].items[1].items[16].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_1997.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[1].items[17].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[6].items[1].items[17].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[1].items[17].featureInfoTemplate | string | `"<p>ERA5-Land daily mean RH 1998</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_1998.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1998-01-01T11:00:00Z&time_end=1998-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[1].items[17].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[1].items[17].name | string | `"ERA5-Land daily mean RH 1998"` |  |
| initConfig.catalog[6].items[1].items[17].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[6].items[1].items[17].type | string | `"wms"` |  |
| initConfig.catalog[6].items[1].items[17].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_1998.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[1].items[18].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[6].items[1].items[18].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[1].items[18].featureInfoTemplate | string | `"<p>ERA5-Land daily mean RH 1999</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_1999.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1999-01-01T11:00:00Z&time_end=1999-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[1].items[18].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[1].items[18].name | string | `"ERA5-Land daily mean RH 1999"` |  |
| initConfig.catalog[6].items[1].items[18].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[6].items[1].items[18].type | string | `"wms"` |  |
| initConfig.catalog[6].items[1].items[18].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_1999.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[1].items[19].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[6].items[1].items[19].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[1].items[19].featureInfoTemplate | string | `"<p>ERA5-Land daily mean RH 2000</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_2000.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2000-01-01T11:00:00Z&time_end=2000-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[1].items[19].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[1].items[19].name | string | `"ERA5-Land daily mean RH 2000"` |  |
| initConfig.catalog[6].items[1].items[19].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[6].items[1].items[19].type | string | `"wms"` |  |
| initConfig.catalog[6].items[1].items[19].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_2000.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[1].items[1].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[6].items[1].items[1].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[1].items[1].featureInfoTemplate | string | `"<p>ERA5-Land daily mean RH 1982</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_1982.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1982-01-01T11:00:00Z&time_end=1982-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[1].items[1].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[1].items[1].name | string | `"ERA5-Land daily mean RH 1982"` |  |
| initConfig.catalog[6].items[1].items[1].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[6].items[1].items[1].type | string | `"wms"` |  |
| initConfig.catalog[6].items[1].items[1].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_1982.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[1].items[20].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[6].items[1].items[20].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[1].items[20].featureInfoTemplate | string | `"<p>ERA5-Land daily mean RH 2001</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_2001.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2001-01-01T11:00:00Z&time_end=2001-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[1].items[20].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[1].items[20].name | string | `"ERA5-Land daily mean RH 2001"` |  |
| initConfig.catalog[6].items[1].items[20].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[6].items[1].items[20].type | string | `"wms"` |  |
| initConfig.catalog[6].items[1].items[20].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_2001.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[1].items[21].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[6].items[1].items[21].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[1].items[21].featureInfoTemplate | string | `"<p>ERA5-Land daily mean RH 2002</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_2002.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2002-01-01T11:00:00Z&time_end=2002-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[1].items[21].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[1].items[21].name | string | `"ERA5-Land daily mean RH 2002"` |  |
| initConfig.catalog[6].items[1].items[21].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[6].items[1].items[21].type | string | `"wms"` |  |
| initConfig.catalog[6].items[1].items[21].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_2002.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[1].items[22].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[6].items[1].items[22].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[1].items[22].featureInfoTemplate | string | `"<p>ERA5-Land daily mean RH 2003</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_2003.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2003-01-01T11:00:00Z&time_end=2003-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[1].items[22].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[1].items[22].name | string | `"ERA5-Land daily mean RH 2003"` |  |
| initConfig.catalog[6].items[1].items[22].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[6].items[1].items[22].type | string | `"wms"` |  |
| initConfig.catalog[6].items[1].items[22].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_2003.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[1].items[23].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[6].items[1].items[23].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[1].items[23].featureInfoTemplate | string | `"<p>ERA5-Land daily mean RH 2004</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_2004.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2004-01-01T11:00:00Z&time_end=2004-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[1].items[23].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[1].items[23].name | string | `"ERA5-Land daily mean RH 2004"` |  |
| initConfig.catalog[6].items[1].items[23].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[6].items[1].items[23].type | string | `"wms"` |  |
| initConfig.catalog[6].items[1].items[23].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_2004.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[1].items[24].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[6].items[1].items[24].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[1].items[24].featureInfoTemplate | string | `"<p>ERA5-Land daily mean RH 2005</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_2005.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2005-01-01T11:00:00Z&time_end=2005-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[1].items[24].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[1].items[24].name | string | `"ERA5-Land daily mean RH 2005"` |  |
| initConfig.catalog[6].items[1].items[24].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[6].items[1].items[24].type | string | `"wms"` |  |
| initConfig.catalog[6].items[1].items[24].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_2005.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[1].items[25].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[6].items[1].items[25].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[1].items[25].featureInfoTemplate | string | `"<p>ERA5-Land daily mean RH 2006</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_2006.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2006-01-01T11:00:00Z&time_end=2006-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[1].items[25].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[1].items[25].name | string | `"ERA5-Land daily mean RH 2006"` |  |
| initConfig.catalog[6].items[1].items[25].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[6].items[1].items[25].type | string | `"wms"` |  |
| initConfig.catalog[6].items[1].items[25].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_2006.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[1].items[26].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[6].items[1].items[26].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[1].items[26].featureInfoTemplate | string | `"<p>ERA5-Land daily mean RH 2007</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_2007.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2007-01-01T11:00:00Z&time_end=2007-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[1].items[26].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[1].items[26].name | string | `"ERA5-Land daily mean RH 2007"` |  |
| initConfig.catalog[6].items[1].items[26].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[6].items[1].items[26].type | string | `"wms"` |  |
| initConfig.catalog[6].items[1].items[26].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_2007.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[1].items[27].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[6].items[1].items[27].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[1].items[27].featureInfoTemplate | string | `"<p>ERA5-Land daily mean RH 2008</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_2008.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2008-01-01T11:00:00Z&time_end=2008-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[1].items[27].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[1].items[27].name | string | `"ERA5-Land daily mean RH 2008"` |  |
| initConfig.catalog[6].items[1].items[27].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[6].items[1].items[27].type | string | `"wms"` |  |
| initConfig.catalog[6].items[1].items[27].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_2008.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[1].items[28].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[6].items[1].items[28].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[1].items[28].featureInfoTemplate | string | `"<p>ERA5-Land daily mean RH 2009</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_2009.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2009-01-01T11:00:00Z&time_end=2009-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[1].items[28].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[1].items[28].name | string | `"ERA5-Land daily mean RH 2009"` |  |
| initConfig.catalog[6].items[1].items[28].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[6].items[1].items[28].type | string | `"wms"` |  |
| initConfig.catalog[6].items[1].items[28].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_2009.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[1].items[29].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[6].items[1].items[29].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[1].items[29].featureInfoTemplate | string | `"<p>ERA5-Land daily mean RH 2010</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_2010.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2010-01-01T11:00:00Z&time_end=2010-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[1].items[29].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[1].items[29].name | string | `"ERA5-Land daily mean RH 2010"` |  |
| initConfig.catalog[6].items[1].items[29].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[6].items[1].items[29].type | string | `"wms"` |  |
| initConfig.catalog[6].items[1].items[29].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_2010.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[1].items[2].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[6].items[1].items[2].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[1].items[2].featureInfoTemplate | string | `"<p>ERA5-Land daily mean RH 1983</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_1983.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1983-01-01T11:00:00Z&time_end=1983-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[1].items[2].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[1].items[2].name | string | `"ERA5-Land daily mean RH 1983"` |  |
| initConfig.catalog[6].items[1].items[2].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[6].items[1].items[2].type | string | `"wms"` |  |
| initConfig.catalog[6].items[1].items[2].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_1983.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[1].items[30].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[6].items[1].items[30].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[1].items[30].featureInfoTemplate | string | `"<p>ERA5-Land daily mean RH 2011</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_2011.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2011-01-01T11:00:00Z&time_end=2011-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[1].items[30].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[1].items[30].name | string | `"ERA5-Land daily mean RH 2011"` |  |
| initConfig.catalog[6].items[1].items[30].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[6].items[1].items[30].type | string | `"wms"` |  |
| initConfig.catalog[6].items[1].items[30].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_2011.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[1].items[31].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[6].items[1].items[31].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[1].items[31].featureInfoTemplate | string | `"<p>ERA5-Land daily mean RH 2012</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_2012.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2012-01-01T11:00:00Z&time_end=2012-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[1].items[31].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[1].items[31].name | string | `"ERA5-Land daily mean RH 2012"` |  |
| initConfig.catalog[6].items[1].items[31].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[6].items[1].items[31].type | string | `"wms"` |  |
| initConfig.catalog[6].items[1].items[31].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_2012.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[1].items[32].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[6].items[1].items[32].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[1].items[32].featureInfoTemplate | string | `"<p>ERA5-Land daily mean RH 2013</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_2013.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2013-01-01T11:00:00Z&time_end=2013-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[1].items[32].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[1].items[32].name | string | `"ERA5-Land daily mean RH 2013"` |  |
| initConfig.catalog[6].items[1].items[32].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[6].items[1].items[32].type | string | `"wms"` |  |
| initConfig.catalog[6].items[1].items[32].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_2013.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[1].items[33].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[6].items[1].items[33].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[1].items[33].featureInfoTemplate | string | `"<p>ERA5-Land daily mean RH 2014</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_2014.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2014-01-01T11:00:00Z&time_end=2014-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[1].items[33].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[1].items[33].name | string | `"ERA5-Land daily mean RH 2014"` |  |
| initConfig.catalog[6].items[1].items[33].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[6].items[1].items[33].type | string | `"wms"` |  |
| initConfig.catalog[6].items[1].items[33].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_2014.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[1].items[34].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[6].items[1].items[34].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[1].items[34].featureInfoTemplate | string | `"<p>ERA5-Land daily mean RH 2015</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_2015.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2015-01-01T11:00:00Z&time_end=2015-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[1].items[34].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[1].items[34].name | string | `"ERA5-Land daily mean RH 2015"` |  |
| initConfig.catalog[6].items[1].items[34].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[6].items[1].items[34].type | string | `"wms"` |  |
| initConfig.catalog[6].items[1].items[34].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_2015.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[1].items[35].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[6].items[1].items[35].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[1].items[35].featureInfoTemplate | string | `"<p>ERA5-Land daily mean RH 2016</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_2016.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2016-01-01T11:00:00Z&time_end=2016-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[1].items[35].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[1].items[35].name | string | `"ERA5-Land daily mean RH 2016"` |  |
| initConfig.catalog[6].items[1].items[35].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[6].items[1].items[35].type | string | `"wms"` |  |
| initConfig.catalog[6].items[1].items[35].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_2016.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[1].items[36].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[6].items[1].items[36].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[1].items[36].featureInfoTemplate | string | `"<p>ERA5-Land daily mean RH 2017</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_2017.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2017-01-01T11:00:00Z&time_end=2017-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[1].items[36].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[1].items[36].name | string | `"ERA5-Land daily mean RH 2017"` |  |
| initConfig.catalog[6].items[1].items[36].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[6].items[1].items[36].type | string | `"wms"` |  |
| initConfig.catalog[6].items[1].items[36].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_2017.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[1].items[37].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[6].items[1].items[37].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[1].items[37].featureInfoTemplate | string | `"<p>ERA5-Land daily mean RH 2018</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_2018.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2018-01-01T11:00:00Z&time_end=2018-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[1].items[37].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[1].items[37].name | string | `"ERA5-Land daily mean RH 2018"` |  |
| initConfig.catalog[6].items[1].items[37].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[6].items[1].items[37].type | string | `"wms"` |  |
| initConfig.catalog[6].items[1].items[37].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_2018.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[1].items[38].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[6].items[1].items[38].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[1].items[38].featureInfoTemplate | string | `"<p>ERA5-Land daily mean RH 2019</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_2019.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2019-01-01T11:00:00Z&time_end=2019-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[1].items[38].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[1].items[38].name | string | `"ERA5-Land daily mean RH 2019"` |  |
| initConfig.catalog[6].items[1].items[38].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[6].items[1].items[38].type | string | `"wms"` |  |
| initConfig.catalog[6].items[1].items[38].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_2019.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[1].items[3].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[6].items[1].items[3].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[1].items[3].featureInfoTemplate | string | `"<p>ERA5-Land daily mean RH 1984</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_1984.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1984-01-01T11:00:00Z&time_end=1984-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[1].items[3].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[1].items[3].name | string | `"ERA5-Land daily mean RH 1984"` |  |
| initConfig.catalog[6].items[1].items[3].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[6].items[1].items[3].type | string | `"wms"` |  |
| initConfig.catalog[6].items[1].items[3].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_1984.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[1].items[4].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[6].items[1].items[4].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[1].items[4].featureInfoTemplate | string | `"<p>ERA5-Land daily mean RH 1985</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_1985.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1985-01-01T11:00:00Z&time_end=1985-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[1].items[4].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[1].items[4].name | string | `"ERA5-Land daily mean RH 1985"` |  |
| initConfig.catalog[6].items[1].items[4].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[6].items[1].items[4].type | string | `"wms"` |  |
| initConfig.catalog[6].items[1].items[4].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_1985.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[1].items[5].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[6].items[1].items[5].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[1].items[5].featureInfoTemplate | string | `"<p>ERA5-Land daily mean RH 1986</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_1986.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1986-01-01T11:00:00Z&time_end=1986-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[1].items[5].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[1].items[5].name | string | `"ERA5-Land daily mean RH 1986"` |  |
| initConfig.catalog[6].items[1].items[5].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[6].items[1].items[5].type | string | `"wms"` |  |
| initConfig.catalog[6].items[1].items[5].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_1986.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[1].items[6].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[6].items[1].items[6].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[1].items[6].featureInfoTemplate | string | `"<p>ERA5-Land daily mean RH 1987</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_1987.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1987-01-01T11:00:00Z&time_end=1987-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[1].items[6].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[1].items[6].name | string | `"ERA5-Land daily mean RH 1987"` |  |
| initConfig.catalog[6].items[1].items[6].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[6].items[1].items[6].type | string | `"wms"` |  |
| initConfig.catalog[6].items[1].items[6].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_1987.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[1].items[7].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[6].items[1].items[7].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[1].items[7].featureInfoTemplate | string | `"<p>ERA5-Land daily mean RH 1988</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_1988.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1988-01-01T11:00:00Z&time_end=1988-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[1].items[7].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[1].items[7].name | string | `"ERA5-Land daily mean RH 1988"` |  |
| initConfig.catalog[6].items[1].items[7].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[6].items[1].items[7].type | string | `"wms"` |  |
| initConfig.catalog[6].items[1].items[7].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_1988.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[1].items[8].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[6].items[1].items[8].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[1].items[8].featureInfoTemplate | string | `"<p>ERA5-Land daily mean RH 1989</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_1989.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1989-01-01T11:00:00Z&time_end=1989-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[1].items[8].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[1].items[8].name | string | `"ERA5-Land daily mean RH 1989"` |  |
| initConfig.catalog[6].items[1].items[8].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[6].items[1].items[8].type | string | `"wms"` |  |
| initConfig.catalog[6].items[1].items[8].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_1989.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[1].items[9].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[6].items[1].items[9].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[1].items[9].featureInfoTemplate | string | `"<p>ERA5-Land daily mean RH 1990</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_1990.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1990-01-01T11:00:00Z&time_end=1990-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[1].items[9].layers | string | `"t2m"` |  |
| initConfig.catalog[6].items[1].items[9].name | string | `"ERA5-Land daily mean RH 1990"` |  |
| initConfig.catalog[6].items[1].items[9].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[6].items[1].items[9].type | string | `"wms"` |  |
| initConfig.catalog[6].items[1].items[9].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_RH/ERA5-Land_daily_mean_RH_1990.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[1].name | string | `"ERA5-Land daily mean RH"` |  |
| initConfig.catalog[6].items[1].preserveOrder | bool | `true` |  |
| initConfig.catalog[6].items[1].type | string | `"group"` |  |
| initConfig.catalog[6].items[2].isOpen | bool | `false` |  |
| initConfig.catalog[6].items[2].items[0].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[6].items[2].items[0].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[2].items[0].featureInfoTemplate | string | `"<p>ERA5-Land daily mean TotalWind 2001</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_TotalWind/ERA5-Land_daily_mean_TotalWind_2001.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2001-01-01T11:00:00Z&time_end=2001-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[2].items[0].layers | string | `"u10"` |  |
| initConfig.catalog[6].items[2].items[0].name | string | `"ERA5-Land daily mean TotalWind 2001"` |  |
| initConfig.catalog[6].items[2].items[0].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[6].items[2].items[0].type | string | `"wms"` |  |
| initConfig.catalog[6].items[2].items[0].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_TotalWind/ERA5-Land_daily_mean_TotalWind_2001.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[2].items[10].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[6].items[2].items[10].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[2].items[10].featureInfoTemplate | string | `"<p>ERA5-Land daily mean TotalWind 2011</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_TotalWind/ERA5-Land_daily_mean_TotalWind_2011.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2011-01-01T11:00:00Z&time_end=2011-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[2].items[10].layers | string | `"u10"` |  |
| initConfig.catalog[6].items[2].items[10].name | string | `"ERA5-Land daily mean TotalWind 2011"` |  |
| initConfig.catalog[6].items[2].items[10].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[6].items[2].items[10].type | string | `"wms"` |  |
| initConfig.catalog[6].items[2].items[10].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_TotalWind/ERA5-Land_daily_mean_TotalWind_2011.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[2].items[11].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[6].items[2].items[11].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[2].items[11].featureInfoTemplate | string | `"<p>ERA5-Land daily mean TotalWind 2012</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_TotalWind/ERA5-Land_daily_mean_TotalWind_2012.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2012-01-01T11:00:00Z&time_end=2012-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[2].items[11].layers | string | `"u10"` |  |
| initConfig.catalog[6].items[2].items[11].name | string | `"ERA5-Land daily mean TotalWind 2012"` |  |
| initConfig.catalog[6].items[2].items[11].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[6].items[2].items[11].type | string | `"wms"` |  |
| initConfig.catalog[6].items[2].items[11].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_TotalWind/ERA5-Land_daily_mean_TotalWind_2012.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[2].items[12].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[6].items[2].items[12].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[2].items[12].featureInfoTemplate | string | `"<p>ERA5-Land daily mean TotalWind 2013</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_TotalWind/ERA5-Land_daily_mean_TotalWind_2013.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2013-01-01T11:00:00Z&time_end=2013-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[2].items[12].layers | string | `"u10"` |  |
| initConfig.catalog[6].items[2].items[12].name | string | `"ERA5-Land daily mean TotalWind 2013"` |  |
| initConfig.catalog[6].items[2].items[12].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[6].items[2].items[12].type | string | `"wms"` |  |
| initConfig.catalog[6].items[2].items[12].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_TotalWind/ERA5-Land_daily_mean_TotalWind_2013.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[2].items[13].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[6].items[2].items[13].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[2].items[13].featureInfoTemplate | string | `"<p>ERA5-Land daily mean TotalWind 2014</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_TotalWind/ERA5-Land_daily_mean_TotalWind_2014.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2014-01-01T11:00:00Z&time_end=2014-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[2].items[13].layers | string | `"u10"` |  |
| initConfig.catalog[6].items[2].items[13].name | string | `"ERA5-Land daily mean TotalWind 2014"` |  |
| initConfig.catalog[6].items[2].items[13].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[6].items[2].items[13].type | string | `"wms"` |  |
| initConfig.catalog[6].items[2].items[13].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_TotalWind/ERA5-Land_daily_mean_TotalWind_2014.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[2].items[14].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[6].items[2].items[14].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[2].items[14].featureInfoTemplate | string | `"<p>ERA5-Land daily mean TotalWind 2015</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_TotalWind/ERA5-Land_daily_mean_TotalWind_2015.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2015-01-01T11:00:00Z&time_end=2015-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[2].items[14].layers | string | `"u10"` |  |
| initConfig.catalog[6].items[2].items[14].name | string | `"ERA5-Land daily mean TotalWind 2015"` |  |
| initConfig.catalog[6].items[2].items[14].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[6].items[2].items[14].type | string | `"wms"` |  |
| initConfig.catalog[6].items[2].items[14].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_TotalWind/ERA5-Land_daily_mean_TotalWind_2015.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[2].items[15].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[6].items[2].items[15].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[2].items[15].featureInfoTemplate | string | `"<p>ERA5-Land daily mean TotalWind 2016</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_TotalWind/ERA5-Land_daily_mean_TotalWind_2016.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2016-01-01T11:00:00Z&time_end=2016-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[2].items[15].layers | string | `"u10"` |  |
| initConfig.catalog[6].items[2].items[15].name | string | `"ERA5-Land daily mean TotalWind 2016"` |  |
| initConfig.catalog[6].items[2].items[15].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[6].items[2].items[15].type | string | `"wms"` |  |
| initConfig.catalog[6].items[2].items[15].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_TotalWind/ERA5-Land_daily_mean_TotalWind_2016.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[2].items[16].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[6].items[2].items[16].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[2].items[16].featureInfoTemplate | string | `"<p>ERA5-Land daily mean TotalWind 2017</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_TotalWind/ERA5-Land_daily_mean_TotalWind_2017.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2017-01-01T11:00:00Z&time_end=2017-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[2].items[16].layers | string | `"u10"` |  |
| initConfig.catalog[6].items[2].items[16].name | string | `"ERA5-Land daily mean TotalWind 2017"` |  |
| initConfig.catalog[6].items[2].items[16].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[6].items[2].items[16].type | string | `"wms"` |  |
| initConfig.catalog[6].items[2].items[16].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_TotalWind/ERA5-Land_daily_mean_TotalWind_2017.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[2].items[17].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[6].items[2].items[17].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[2].items[17].featureInfoTemplate | string | `"<p>ERA5-Land daily mean TotalWind 2018</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_TotalWind/ERA5-Land_daily_mean_TotalWind_2018.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2018-01-01T11:00:00Z&time_end=2018-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[2].items[17].layers | string | `"u10"` |  |
| initConfig.catalog[6].items[2].items[17].name | string | `"ERA5-Land daily mean TotalWind 2018"` |  |
| initConfig.catalog[6].items[2].items[17].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[6].items[2].items[17].type | string | `"wms"` |  |
| initConfig.catalog[6].items[2].items[17].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_TotalWind/ERA5-Land_daily_mean_TotalWind_2018.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[2].items[18].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[6].items[2].items[18].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[2].items[18].featureInfoTemplate | string | `"<p>ERA5-Land daily mean TotalWind 2019</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_TotalWind/ERA5-Land_daily_mean_TotalWind_2019.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2019-01-01T11:00:00Z&time_end=2019-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[2].items[18].layers | string | `"u10"` |  |
| initConfig.catalog[6].items[2].items[18].name | string | `"ERA5-Land daily mean TotalWind 2019"` |  |
| initConfig.catalog[6].items[2].items[18].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[6].items[2].items[18].type | string | `"wms"` |  |
| initConfig.catalog[6].items[2].items[18].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_TotalWind/ERA5-Land_daily_mean_TotalWind_2019.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[2].items[1].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[6].items[2].items[1].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[2].items[1].featureInfoTemplate | string | `"<p>ERA5-Land daily mean TotalWind 2002</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_TotalWind/ERA5-Land_daily_mean_TotalWind_2002.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2002-01-01T11:00:00Z&time_end=2002-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[2].items[1].layers | string | `"u10"` |  |
| initConfig.catalog[6].items[2].items[1].name | string | `"ERA5-Land daily mean TotalWind 2002"` |  |
| initConfig.catalog[6].items[2].items[1].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[6].items[2].items[1].type | string | `"wms"` |  |
| initConfig.catalog[6].items[2].items[1].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_TotalWind/ERA5-Land_daily_mean_TotalWind_2002.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[2].items[2].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[6].items[2].items[2].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[2].items[2].featureInfoTemplate | string | `"<p>ERA5-Land daily mean TotalWind 2003</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_TotalWind/ERA5-Land_daily_mean_TotalWind_2003.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2003-01-01T11:00:00Z&time_end=2003-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[2].items[2].layers | string | `"u10"` |  |
| initConfig.catalog[6].items[2].items[2].name | string | `"ERA5-Land daily mean TotalWind 2003"` |  |
| initConfig.catalog[6].items[2].items[2].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[6].items[2].items[2].type | string | `"wms"` |  |
| initConfig.catalog[6].items[2].items[2].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_TotalWind/ERA5-Land_daily_mean_TotalWind_2003.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[2].items[3].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[6].items[2].items[3].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[2].items[3].featureInfoTemplate | string | `"<p>ERA5-Land daily mean TotalWind 2004</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_TotalWind/ERA5-Land_daily_mean_TotalWind_2004.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2004-01-01T11:00:00Z&time_end=2004-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[2].items[3].layers | string | `"u10"` |  |
| initConfig.catalog[6].items[2].items[3].name | string | `"ERA5-Land daily mean TotalWind 2004"` |  |
| initConfig.catalog[6].items[2].items[3].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[6].items[2].items[3].type | string | `"wms"` |  |
| initConfig.catalog[6].items[2].items[3].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_TotalWind/ERA5-Land_daily_mean_TotalWind_2004.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[2].items[4].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[6].items[2].items[4].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[2].items[4].featureInfoTemplate | string | `"<p>ERA5-Land daily mean TotalWind 2005</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_TotalWind/ERA5-Land_daily_mean_TotalWind_2005.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2005-01-01T11:00:00Z&time_end=2005-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[2].items[4].layers | string | `"u10"` |  |
| initConfig.catalog[6].items[2].items[4].name | string | `"ERA5-Land daily mean TotalWind 2005"` |  |
| initConfig.catalog[6].items[2].items[4].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[6].items[2].items[4].type | string | `"wms"` |  |
| initConfig.catalog[6].items[2].items[4].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_TotalWind/ERA5-Land_daily_mean_TotalWind_2005.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[2].items[5].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[6].items[2].items[5].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[2].items[5].featureInfoTemplate | string | `"<p>ERA5-Land daily mean TotalWind 2006</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_TotalWind/ERA5-Land_daily_mean_TotalWind_2006.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2006-01-01T11:00:00Z&time_end=2006-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[2].items[5].layers | string | `"u10"` |  |
| initConfig.catalog[6].items[2].items[5].name | string | `"ERA5-Land daily mean TotalWind 2006"` |  |
| initConfig.catalog[6].items[2].items[5].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[6].items[2].items[5].type | string | `"wms"` |  |
| initConfig.catalog[6].items[2].items[5].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_TotalWind/ERA5-Land_daily_mean_TotalWind_2006.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[2].items[6].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[6].items[2].items[6].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[2].items[6].featureInfoTemplate | string | `"<p>ERA5-Land daily mean TotalWind 2007</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_TotalWind/ERA5-Land_daily_mean_TotalWind_2007.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2007-01-01T11:00:00Z&time_end=2007-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[2].items[6].layers | string | `"u10"` |  |
| initConfig.catalog[6].items[2].items[6].name | string | `"ERA5-Land daily mean TotalWind 2007"` |  |
| initConfig.catalog[6].items[2].items[6].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[6].items[2].items[6].type | string | `"wms"` |  |
| initConfig.catalog[6].items[2].items[6].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_TotalWind/ERA5-Land_daily_mean_TotalWind_2007.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[2].items[7].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[6].items[2].items[7].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[2].items[7].featureInfoTemplate | string | `"<p>ERA5-Land daily mean TotalWind 2008</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_TotalWind/ERA5-Land_daily_mean_TotalWind_2008.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2008-01-01T11:00:00Z&time_end=2008-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[2].items[7].layers | string | `"u10"` |  |
| initConfig.catalog[6].items[2].items[7].name | string | `"ERA5-Land daily mean TotalWind 2008"` |  |
| initConfig.catalog[6].items[2].items[7].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[6].items[2].items[7].type | string | `"wms"` |  |
| initConfig.catalog[6].items[2].items[7].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_TotalWind/ERA5-Land_daily_mean_TotalWind_2008.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[2].items[8].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[6].items[2].items[8].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[2].items[8].featureInfoTemplate | string | `"<p>ERA5-Land daily mean TotalWind 2009</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_TotalWind/ERA5-Land_daily_mean_TotalWind_2009.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2009-01-01T11:00:00Z&time_end=2009-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[2].items[8].layers | string | `"u10"` |  |
| initConfig.catalog[6].items[2].items[8].name | string | `"ERA5-Land daily mean TotalWind 2009"` |  |
| initConfig.catalog[6].items[2].items[8].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[6].items[2].items[8].type | string | `"wms"` |  |
| initConfig.catalog[6].items[2].items[8].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_TotalWind/ERA5-Land_daily_mean_TotalWind_2009.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[2].items[9].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[6].items[2].items[9].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[2].items[9].featureInfoTemplate | string | `"<p>ERA5-Land daily mean TotalWind 2010</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_mean_TotalWind/ERA5-Land_daily_mean_TotalWind_2010.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2010-01-01T11:00:00Z&time_end=2010-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[2].items[9].layers | string | `"u10"` |  |
| initConfig.catalog[6].items[2].items[9].name | string | `"ERA5-Land daily mean TotalWind 2010"` |  |
| initConfig.catalog[6].items[2].items[9].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[6].items[2].items[9].type | string | `"wms"` |  |
| initConfig.catalog[6].items[2].items[9].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_mean_TotalWind/ERA5-Land_daily_mean_TotalWind_2010.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[2].name | string | `"ERA5-Land daily mean TotalWind"` |  |
| initConfig.catalog[6].items[2].preserveOrder | bool | `true` |  |
| initConfig.catalog[6].items[2].type | string | `"group"` |  |
| initConfig.catalog[6].items[3].isOpen | bool | `false` |  |
| initConfig.catalog[6].items[3].items[0].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[6].items[3].items[0].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[3].items[0].featureInfoTemplate | string | `"<p>ERA5-Land daily total precipitation 1981</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_1981.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1981-01-01T11:00:00Z&time_end=1981-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[3].items[0].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[6].items[3].items[0].name | string | `"ERA5-Land daily total precipitation 1981"` |  |
| initConfig.catalog[6].items[3].items[0].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[6].items[3].items[0].type | string | `"wms"` |  |
| initConfig.catalog[6].items[3].items[0].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_1981.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[3].items[10].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[6].items[3].items[10].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[3].items[10].featureInfoTemplate | string | `"<p>ERA5-Land daily total precipitation 1991</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_1991.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1991-01-01T11:00:00Z&time_end=1991-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[3].items[10].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[6].items[3].items[10].name | string | `"ERA5-Land daily total precipitation 1991"` |  |
| initConfig.catalog[6].items[3].items[10].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[6].items[3].items[10].type | string | `"wms"` |  |
| initConfig.catalog[6].items[3].items[10].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_1991.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[3].items[11].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[6].items[3].items[11].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[3].items[11].featureInfoTemplate | string | `"<p>ERA5-Land daily total precipitation 1992</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_1992.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1992-01-01T11:00:00Z&time_end=1992-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[3].items[11].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[6].items[3].items[11].name | string | `"ERA5-Land daily total precipitation 1992"` |  |
| initConfig.catalog[6].items[3].items[11].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[6].items[3].items[11].type | string | `"wms"` |  |
| initConfig.catalog[6].items[3].items[11].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_1992.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[3].items[12].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[6].items[3].items[12].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[3].items[12].featureInfoTemplate | string | `"<p>ERA5-Land daily total precipitation 1993</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_1993.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1993-01-01T11:00:00Z&time_end=1993-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[3].items[12].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[6].items[3].items[12].name | string | `"ERA5-Land daily total precipitation 1993"` |  |
| initConfig.catalog[6].items[3].items[12].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[6].items[3].items[12].type | string | `"wms"` |  |
| initConfig.catalog[6].items[3].items[12].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_1993.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[3].items[13].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[6].items[3].items[13].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[3].items[13].featureInfoTemplate | string | `"<p>ERA5-Land daily total precipitation 1994</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_1994.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1994-01-01T11:00:00Z&time_end=1994-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[3].items[13].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[6].items[3].items[13].name | string | `"ERA5-Land daily total precipitation 1994"` |  |
| initConfig.catalog[6].items[3].items[13].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[6].items[3].items[13].type | string | `"wms"` |  |
| initConfig.catalog[6].items[3].items[13].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_1994.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[3].items[14].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[6].items[3].items[14].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[3].items[14].featureInfoTemplate | string | `"<p>ERA5-Land daily total precipitation 1995</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_1995.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1995-01-01T11:00:00Z&time_end=1995-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[3].items[14].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[6].items[3].items[14].name | string | `"ERA5-Land daily total precipitation 1995"` |  |
| initConfig.catalog[6].items[3].items[14].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[6].items[3].items[14].type | string | `"wms"` |  |
| initConfig.catalog[6].items[3].items[14].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_1995.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[3].items[15].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[6].items[3].items[15].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[3].items[15].featureInfoTemplate | string | `"<p>ERA5-Land daily total precipitation 1996</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_1996.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1996-01-01T11:00:00Z&time_end=1996-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[3].items[15].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[6].items[3].items[15].name | string | `"ERA5-Land daily total precipitation 1996"` |  |
| initConfig.catalog[6].items[3].items[15].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[6].items[3].items[15].type | string | `"wms"` |  |
| initConfig.catalog[6].items[3].items[15].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_1996.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[3].items[16].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[6].items[3].items[16].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[3].items[16].featureInfoTemplate | string | `"<p>ERA5-Land daily total precipitation 1997</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_1997.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1997-01-01T11:00:00Z&time_end=1997-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[3].items[16].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[6].items[3].items[16].name | string | `"ERA5-Land daily total precipitation 1997"` |  |
| initConfig.catalog[6].items[3].items[16].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[6].items[3].items[16].type | string | `"wms"` |  |
| initConfig.catalog[6].items[3].items[16].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_1997.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[3].items[17].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[6].items[3].items[17].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[3].items[17].featureInfoTemplate | string | `"<p>ERA5-Land daily total precipitation 1998</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_1998.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1998-01-01T11:00:00Z&time_end=1998-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[3].items[17].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[6].items[3].items[17].name | string | `"ERA5-Land daily total precipitation 1998"` |  |
| initConfig.catalog[6].items[3].items[17].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[6].items[3].items[17].type | string | `"wms"` |  |
| initConfig.catalog[6].items[3].items[17].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_1998.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[3].items[18].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[6].items[3].items[18].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[3].items[18].featureInfoTemplate | string | `"<p>ERA5-Land daily total precipitation 1999</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_1999.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1999-01-01T11:00:00Z&time_end=1999-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[3].items[18].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[6].items[3].items[18].name | string | `"ERA5-Land daily total precipitation 1999"` |  |
| initConfig.catalog[6].items[3].items[18].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[6].items[3].items[18].type | string | `"wms"` |  |
| initConfig.catalog[6].items[3].items[18].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_1999.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[3].items[19].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[6].items[3].items[19].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[3].items[19].featureInfoTemplate | string | `"<p>ERA5-Land daily total precipitation 2000</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_2000.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2000-01-01T11:00:00Z&time_end=2000-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[3].items[19].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[6].items[3].items[19].name | string | `"ERA5-Land daily total precipitation 2000"` |  |
| initConfig.catalog[6].items[3].items[19].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[6].items[3].items[19].type | string | `"wms"` |  |
| initConfig.catalog[6].items[3].items[19].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_2000.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[3].items[1].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[6].items[3].items[1].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[3].items[1].featureInfoTemplate | string | `"<p>ERA5-Land daily total precipitation 1982</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_1982.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1982-01-01T11:00:00Z&time_end=1982-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[3].items[1].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[6].items[3].items[1].name | string | `"ERA5-Land daily total precipitation 1982"` |  |
| initConfig.catalog[6].items[3].items[1].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[6].items[3].items[1].type | string | `"wms"` |  |
| initConfig.catalog[6].items[3].items[1].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_1982.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[3].items[20].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[6].items[3].items[20].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[3].items[20].featureInfoTemplate | string | `"<p>ERA5-Land daily total precipitation 2001</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_2001.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2001-01-01T11:00:00Z&time_end=2001-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[3].items[20].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[6].items[3].items[20].name | string | `"ERA5-Land daily total precipitation 2001"` |  |
| initConfig.catalog[6].items[3].items[20].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[6].items[3].items[20].type | string | `"wms"` |  |
| initConfig.catalog[6].items[3].items[20].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_2001.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[3].items[21].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[6].items[3].items[21].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[3].items[21].featureInfoTemplate | string | `"<p>ERA5-Land daily total precipitation 2002</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_2002.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2002-01-01T11:00:00Z&time_end=2002-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[3].items[21].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[6].items[3].items[21].name | string | `"ERA5-Land daily total precipitation 2002"` |  |
| initConfig.catalog[6].items[3].items[21].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[6].items[3].items[21].type | string | `"wms"` |  |
| initConfig.catalog[6].items[3].items[21].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_2002.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[3].items[22].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[6].items[3].items[22].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[3].items[22].featureInfoTemplate | string | `"<p>ERA5-Land daily total precipitation 2003</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_2003.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2003-01-01T11:00:00Z&time_end=2003-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[3].items[22].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[6].items[3].items[22].name | string | `"ERA5-Land daily total precipitation 2003"` |  |
| initConfig.catalog[6].items[3].items[22].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[6].items[3].items[22].type | string | `"wms"` |  |
| initConfig.catalog[6].items[3].items[22].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_2003.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[3].items[23].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[6].items[3].items[23].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[3].items[23].featureInfoTemplate | string | `"<p>ERA5-Land daily total precipitation 2004</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_2004.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2004-01-01T11:00:00Z&time_end=2004-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[3].items[23].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[6].items[3].items[23].name | string | `"ERA5-Land daily total precipitation 2004"` |  |
| initConfig.catalog[6].items[3].items[23].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[6].items[3].items[23].type | string | `"wms"` |  |
| initConfig.catalog[6].items[3].items[23].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_2004.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[3].items[24].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[6].items[3].items[24].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[3].items[24].featureInfoTemplate | string | `"<p>ERA5-Land daily total precipitation 2005</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_2005.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2005-01-01T11:00:00Z&time_end=2005-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[3].items[24].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[6].items[3].items[24].name | string | `"ERA5-Land daily total precipitation 2005"` |  |
| initConfig.catalog[6].items[3].items[24].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[6].items[3].items[24].type | string | `"wms"` |  |
| initConfig.catalog[6].items[3].items[24].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_2005.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[3].items[25].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[6].items[3].items[25].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[3].items[25].featureInfoTemplate | string | `"<p>ERA5-Land daily total precipitation 2006</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_2006.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2006-01-01T11:00:00Z&time_end=2006-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[3].items[25].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[6].items[3].items[25].name | string | `"ERA5-Land daily total precipitation 2006"` |  |
| initConfig.catalog[6].items[3].items[25].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[6].items[3].items[25].type | string | `"wms"` |  |
| initConfig.catalog[6].items[3].items[25].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_2006.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[3].items[26].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[6].items[3].items[26].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[3].items[26].featureInfoTemplate | string | `"<p>ERA5-Land daily total precipitation 2007</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_2007.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2007-01-01T11:00:00Z&time_end=2007-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[3].items[26].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[6].items[3].items[26].name | string | `"ERA5-Land daily total precipitation 2007"` |  |
| initConfig.catalog[6].items[3].items[26].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[6].items[3].items[26].type | string | `"wms"` |  |
| initConfig.catalog[6].items[3].items[26].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_2007.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[3].items[27].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[6].items[3].items[27].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[3].items[27].featureInfoTemplate | string | `"<p>ERA5-Land daily total precipitation 2008</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_2008.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2008-01-01T11:00:00Z&time_end=2008-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[3].items[27].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[6].items[3].items[27].name | string | `"ERA5-Land daily total precipitation 2008"` |  |
| initConfig.catalog[6].items[3].items[27].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[6].items[3].items[27].type | string | `"wms"` |  |
| initConfig.catalog[6].items[3].items[27].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_2008.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[3].items[28].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[6].items[3].items[28].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[3].items[28].featureInfoTemplate | string | `"<p>ERA5-Land daily total precipitation 2009</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_2009.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2009-01-01T11:00:00Z&time_end=2009-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[3].items[28].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[6].items[3].items[28].name | string | `"ERA5-Land daily total precipitation 2009"` |  |
| initConfig.catalog[6].items[3].items[28].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[6].items[3].items[28].type | string | `"wms"` |  |
| initConfig.catalog[6].items[3].items[28].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_2009.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[3].items[29].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[6].items[3].items[29].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[3].items[29].featureInfoTemplate | string | `"<p>ERA5-Land daily total precipitation 2010</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_2010.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2010-01-01T11:00:00Z&time_end=2010-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[3].items[29].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[6].items[3].items[29].name | string | `"ERA5-Land daily total precipitation 2010"` |  |
| initConfig.catalog[6].items[3].items[29].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[6].items[3].items[29].type | string | `"wms"` |  |
| initConfig.catalog[6].items[3].items[29].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_2010.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[3].items[2].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[6].items[3].items[2].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[3].items[2].featureInfoTemplate | string | `"<p>ERA5-Land daily total precipitation 1983</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_1983.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1983-01-01T11:00:00Z&time_end=1983-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[3].items[2].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[6].items[3].items[2].name | string | `"ERA5-Land daily total precipitation 1983"` |  |
| initConfig.catalog[6].items[3].items[2].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[6].items[3].items[2].type | string | `"wms"` |  |
| initConfig.catalog[6].items[3].items[2].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_1983.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[3].items[30].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[6].items[3].items[30].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[3].items[30].featureInfoTemplate | string | `"<p>ERA5-Land daily total precipitation 2011</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_2011.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2011-01-01T11:00:00Z&time_end=2011-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[3].items[30].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[6].items[3].items[30].name | string | `"ERA5-Land daily total precipitation 2011"` |  |
| initConfig.catalog[6].items[3].items[30].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[6].items[3].items[30].type | string | `"wms"` |  |
| initConfig.catalog[6].items[3].items[30].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_2011.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[3].items[31].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[6].items[3].items[31].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[3].items[31].featureInfoTemplate | string | `"<p>ERA5-Land daily total precipitation 2012</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_2012.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2012-01-01T11:00:00Z&time_end=2012-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[3].items[31].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[6].items[3].items[31].name | string | `"ERA5-Land daily total precipitation 2012"` |  |
| initConfig.catalog[6].items[3].items[31].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[6].items[3].items[31].type | string | `"wms"` |  |
| initConfig.catalog[6].items[3].items[31].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_2012.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[3].items[32].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[6].items[3].items[32].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[3].items[32].featureInfoTemplate | string | `"<p>ERA5-Land daily total precipitation 2013</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_2013.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2013-01-01T11:00:00Z&time_end=2013-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[3].items[32].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[6].items[3].items[32].name | string | `"ERA5-Land daily total precipitation 2013"` |  |
| initConfig.catalog[6].items[3].items[32].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[6].items[3].items[32].type | string | `"wms"` |  |
| initConfig.catalog[6].items[3].items[32].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_2013.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[3].items[33].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[6].items[3].items[33].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[3].items[33].featureInfoTemplate | string | `"<p>ERA5-Land daily total precipitation 2014</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_2014.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2014-01-01T11:00:00Z&time_end=2014-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[3].items[33].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[6].items[3].items[33].name | string | `"ERA5-Land daily total precipitation 2014"` |  |
| initConfig.catalog[6].items[3].items[33].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[6].items[3].items[33].type | string | `"wms"` |  |
| initConfig.catalog[6].items[3].items[33].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_2014.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[3].items[34].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[6].items[3].items[34].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[3].items[34].featureInfoTemplate | string | `"<p>ERA5-Land daily total precipitation 2015</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_2015.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2015-01-01T11:00:00Z&time_end=2015-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[3].items[34].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[6].items[3].items[34].name | string | `"ERA5-Land daily total precipitation 2015"` |  |
| initConfig.catalog[6].items[3].items[34].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[6].items[3].items[34].type | string | `"wms"` |  |
| initConfig.catalog[6].items[3].items[34].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_2015.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[3].items[35].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[6].items[3].items[35].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[3].items[35].featureInfoTemplate | string | `"<p>ERA5-Land daily total precipitation 2016</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_2016.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2016-01-01T11:00:00Z&time_end=2016-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[3].items[35].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[6].items[3].items[35].name | string | `"ERA5-Land daily total precipitation 2016"` |  |
| initConfig.catalog[6].items[3].items[35].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[6].items[3].items[35].type | string | `"wms"` |  |
| initConfig.catalog[6].items[3].items[35].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_2016.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[3].items[36].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[6].items[3].items[36].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[3].items[36].featureInfoTemplate | string | `"<p>ERA5-Land daily total precipitation 2017</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_2017.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2017-01-01T11:00:00Z&time_end=2017-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[3].items[36].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[6].items[3].items[36].name | string | `"ERA5-Land daily total precipitation 2017"` |  |
| initConfig.catalog[6].items[3].items[36].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[6].items[3].items[36].type | string | `"wms"` |  |
| initConfig.catalog[6].items[3].items[36].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_2017.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[3].items[37].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[6].items[3].items[37].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[3].items[37].featureInfoTemplate | string | `"<p>ERA5-Land daily total precipitation 2018</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_2018.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2018-01-01T11:00:00Z&time_end=2018-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[3].items[37].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[6].items[3].items[37].name | string | `"ERA5-Land daily total precipitation 2018"` |  |
| initConfig.catalog[6].items[3].items[37].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[6].items[3].items[37].type | string | `"wms"` |  |
| initConfig.catalog[6].items[3].items[37].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_2018.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[3].items[38].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[6].items[3].items[38].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[3].items[38].featureInfoTemplate | string | `"<p>ERA5-Land daily total precipitation 2019</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_2019.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2019-01-01T11:00:00Z&time_end=2019-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[3].items[38].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[6].items[3].items[38].name | string | `"ERA5-Land daily total precipitation 2019"` |  |
| initConfig.catalog[6].items[3].items[38].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[6].items[3].items[38].type | string | `"wms"` |  |
| initConfig.catalog[6].items[3].items[38].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_2019.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[3].items[3].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[6].items[3].items[3].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[3].items[3].featureInfoTemplate | string | `"<p>ERA5-Land daily total precipitation 1984</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_1984.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1984-01-01T11:00:00Z&time_end=1984-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[3].items[3].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[6].items[3].items[3].name | string | `"ERA5-Land daily total precipitation 1984"` |  |
| initConfig.catalog[6].items[3].items[3].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[6].items[3].items[3].type | string | `"wms"` |  |
| initConfig.catalog[6].items[3].items[3].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_1984.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[3].items[4].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[6].items[3].items[4].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[3].items[4].featureInfoTemplate | string | `"<p>ERA5-Land daily total precipitation 1985</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_1985.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1985-01-01T11:00:00Z&time_end=1985-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[3].items[4].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[6].items[3].items[4].name | string | `"ERA5-Land daily total precipitation 1985"` |  |
| initConfig.catalog[6].items[3].items[4].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[6].items[3].items[4].type | string | `"wms"` |  |
| initConfig.catalog[6].items[3].items[4].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_1985.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[3].items[5].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[6].items[3].items[5].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[3].items[5].featureInfoTemplate | string | `"<p>ERA5-Land daily total precipitation 1986</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_1986.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1986-01-01T11:00:00Z&time_end=1986-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[3].items[5].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[6].items[3].items[5].name | string | `"ERA5-Land daily total precipitation 1986"` |  |
| initConfig.catalog[6].items[3].items[5].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[6].items[3].items[5].type | string | `"wms"` |  |
| initConfig.catalog[6].items[3].items[5].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_1986.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[3].items[6].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[6].items[3].items[6].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[3].items[6].featureInfoTemplate | string | `"<p>ERA5-Land daily total precipitation 1987</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_1987.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1987-01-01T11:00:00Z&time_end=1987-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[3].items[6].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[6].items[3].items[6].name | string | `"ERA5-Land daily total precipitation 1987"` |  |
| initConfig.catalog[6].items[3].items[6].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[6].items[3].items[6].type | string | `"wms"` |  |
| initConfig.catalog[6].items[3].items[6].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_1987.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[3].items[7].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[6].items[3].items[7].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[3].items[7].featureInfoTemplate | string | `"<p>ERA5-Land daily total precipitation 1988</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_1988.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1988-01-01T11:00:00Z&time_end=1988-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[3].items[7].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[6].items[3].items[7].name | string | `"ERA5-Land daily total precipitation 1988"` |  |
| initConfig.catalog[6].items[3].items[7].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[6].items[3].items[7].type | string | `"wms"` |  |
| initConfig.catalog[6].items[3].items[7].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_1988.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[3].items[8].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[6].items[3].items[8].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[3].items[8].featureInfoTemplate | string | `"<p>ERA5-Land daily total precipitation 1989</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_1989.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1989-01-01T11:00:00Z&time_end=1989-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[3].items[8].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[6].items[3].items[8].name | string | `"ERA5-Land daily total precipitation 1989"` |  |
| initConfig.catalog[6].items[3].items[8].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[6].items[3].items[8].type | string | `"wms"` |  |
| initConfig.catalog[6].items[3].items[8].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_1989.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[3].items[9].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[6].items[3].items[9].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[6].items[3].items[9].featureInfoTemplate | string | `"<p>ERA5-Land daily total precipitation 1990</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_1990.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1990-01-01T11:00:00Z&time_end=1990-12-31T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[6].items[3].items[9].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[6].items[3].items[9].name | string | `"ERA5-Land daily total precipitation 1990"` |  |
| initConfig.catalog[6].items[3].items[9].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[6].items[3].items[9].type | string | `"wms"` |  |
| initConfig.catalog[6].items[3].items[9].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_daily_total_precipitation/ERA5-Land_daily_total_precipitation_1990.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[6].items[3].name | string | `"ERA5-Land daily total precipitation"` |  |
| initConfig.catalog[6].items[3].preserveOrder | bool | `true` |  |
| initConfig.catalog[6].items[3].type | string | `"group"` |  |
| initConfig.catalog[6].name | string | `"ERA5-Land daily"` |  |
| initConfig.catalog[6].preserveOrder | bool | `true` |  |
| initConfig.catalog[6].type | string | `"group"` |  |
| initConfig.catalog[7].isOpen | bool | `false` |  |
| initConfig.catalog[7].items[0].isOpen | bool | `false` |  |
| initConfig.catalog[7].items[0].items[0].colorScaleMaximum | int | `50` |  |
| initConfig.catalog[7].items[0].items[0].colorScaleMinimum | int | `-50` |  |
| initConfig.catalog[7].items[0].items[0].featureInfoTemplate | string | `"<p>ERA5-Land monthly mean 2mTemp 1981 2019</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_monthly/ERA5-Land_monthly_mean_2mTemp_1981_2019.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1981-01-16T12:00:00Z&time_end=2019-12-16T11:30:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[7].items[0].items[0].layers | string | `"t2m"` |  |
| initConfig.catalog[7].items[0].items[0].name | string | `"ERA5-Land monthly mean 2mTemp 1981 2019"` |  |
| initConfig.catalog[7].items[0].items[0].styles | string | `"boxfill/red-yellow"` |  |
| initConfig.catalog[7].items[0].items[0].type | string | `"wms"` |  |
| initConfig.catalog[7].items[0].items[0].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_monthly/ERA5-Land_monthly_mean_2mTemp_1981_2019.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[7].items[0].name | string | `"ERA5-Land monthly mean 2mTemp"` |  |
| initConfig.catalog[7].items[0].preserveOrder | bool | `true` |  |
| initConfig.catalog[7].items[0].type | string | `"group"` |  |
| initConfig.catalog[7].items[1].isOpen | bool | `false` |  |
| initConfig.catalog[7].items[1].items[0].colorScaleMaximum | int | `100` |  |
| initConfig.catalog[7].items[1].items[0].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[7].items[1].items[0].featureInfoTemplate | string | `"<p>ERA5-Land monthly mean RH 1981 2019</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_monthly/ERA5-Land_monthly_mean_RH_1981_2019.nc?var=t2m&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1981-01-16T12:00:00Z&time_end=2019-12-16T11:30:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[7].items[1].items[0].layers | string | `"t2m"` |  |
| initConfig.catalog[7].items[1].items[0].name | string | `"ERA5-Land monthly mean RH 1981 2019"` |  |
| initConfig.catalog[7].items[1].items[0].styles | string | `"boxfill/green-purple"` |  |
| initConfig.catalog[7].items[1].items[0].type | string | `"wms"` |  |
| initConfig.catalog[7].items[1].items[0].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_monthly/ERA5-Land_monthly_mean_RH_1981_2019.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[7].items[1].name | string | `"ERA5-Land monthly mean RH"` |  |
| initConfig.catalog[7].items[1].preserveOrder | bool | `true` |  |
| initConfig.catalog[7].items[1].type | string | `"group"` |  |
| initConfig.catalog[7].items[2].isOpen | bool | `false` |  |
| initConfig.catalog[7].items[2].items[0].colorScaleMaximum | int | `13` |  |
| initConfig.catalog[7].items[2].items[0].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[7].items[2].items[0].featureInfoTemplate | string | `"<p>ERA5-Land monthly mean TotalWind 2001 2019</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_monthly/ERA5-Land_monthly_mean_TotalWind_2001_2019.nc?var=u10&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2001-01-16T12:00:00Z&time_end=2019-12-16T11:30:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[7].items[2].items[0].layers | string | `"u10"` |  |
| initConfig.catalog[7].items[2].items[0].name | string | `"ERA5-Land monthly mean TotalWind 2001 2019"` |  |
| initConfig.catalog[7].items[2].items[0].styles | string | `"boxfill/rainbow"` |  |
| initConfig.catalog[7].items[2].items[0].type | string | `"wms"` |  |
| initConfig.catalog[7].items[2].items[0].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_monthly/ERA5-Land_monthly_mean_TotalWind_2001_2019.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[7].items[2].name | string | `"ERA5-Land monthly mean TotalWind"` |  |
| initConfig.catalog[7].items[2].preserveOrder | bool | `true` |  |
| initConfig.catalog[7].items[2].type | string | `"group"` |  |
| initConfig.catalog[7].items[3].isOpen | bool | `false` |  |
| initConfig.catalog[7].items[3].items[0].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[7].items[3].items[0].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[7].items[3].items[0].featureInfoTemplate | string | `"<p>ERA5-Land monthly total precipitation 1981 2019</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_monthly/ERA5-Land_monthly_total_precipitation_1981_2019.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1981-01-16T12:00:00Z&time_end=2019-12-16T11:30:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[7].items[3].items[0].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[7].items[3].items[0].name | string | `"ERA5-Land monthly total precipitation 1981 2019"` |  |
| initConfig.catalog[7].items[3].items[0].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[7].items[3].items[0].type | string | `"wms"` |  |
| initConfig.catalog[7].items[3].items[0].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_monthly/ERA5-Land_monthly_total_precipitation_1981_2019.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[7].items[3].name | string | `"ERA5-Land monthly total precipitation"` |  |
| initConfig.catalog[7].items[3].preserveOrder | bool | `true` |  |
| initConfig.catalog[7].items[3].type | string | `"group"` |  |
| initConfig.catalog[7].name | string | `"ERA5-Land monthly"` |  |
| initConfig.catalog[7].preserveOrder | bool | `true` |  |
| initConfig.catalog[7].type | string | `"group"` |  |
| initConfig.catalog[8].isOpen | bool | `false` |  |
| initConfig.catalog[8].items[0].isOpen | bool | `false` |  |
| initConfig.catalog[8].items[0].items[0].colorScaleMaximum | int | `1000` |  |
| initConfig.catalog[8].items[0].items[0].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[8].items[0].items[0].featureInfoTemplate | string | `"<p>ERA5-Land 30year TotalPrecip</p><chart src=\"http://thredds:8080/thredds/ncss/ERA5-Land_30year/ERA5-Land_30year_TotalPrecip.nc?var=precipitation_rate&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1995-07-03T12:00:00Z&time_end=1996-07-01T11:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[8].items[0].items[0].layers | string | `"precipitation_rate"` |  |
| initConfig.catalog[8].items[0].items[0].name | string | `"ERA5-Land 30year TotalPrecip"` |  |
| initConfig.catalog[8].items[0].items[0].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[8].items[0].items[0].type | string | `"wms"` |  |
| initConfig.catalog[8].items[0].items[0].url | string | `"http://thredds:8080/thredds/wms/ERA5-Land_30year/ERA5-Land_30year_TotalPrecip.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[8].items[0].name | string | `"ERA5-Land 30year TotalPrecip"` |  |
| initConfig.catalog[8].items[0].preserveOrder | bool | `true` |  |
| initConfig.catalog[8].items[0].type | string | `"group"` |  |
| initConfig.catalog[8].name | string | `"ERA5-Land 30year"` |  |
| initConfig.catalog[8].preserveOrder | bool | `true` |  |
| initConfig.catalog[8].type | string | `"group"` |  |
| initConfig.catalog[9].isOpen | bool | `false` |  |
| initConfig.catalog[9].items[0].colorScaleMaximum | int | `150` |  |
| initConfig.catalog[9].items[0].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[9].items[0].featureInfoTemplate | string | `"<p>TRMM daily 3B42 1998</p><chart src=\"http://thredds:8080/thredds/ncss/TRMM/TRMM_3B42.1998.daily_V7.nc?var=precip&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1998-01-01T00:00:00Z&time_end=1998-12-31T00:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[9].items[0].layers | string | `"precip"` |  |
| initConfig.catalog[9].items[0].name | string | `"TRMM daily 1998"` |  |
| initConfig.catalog[9].items[0].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[9].items[0].type | string | `"wms"` |  |
| initConfig.catalog[9].items[0].url | string | `"http://thredds:8080/thredds/wms/TRMM/TRMM_3B42.1998.daily_V7.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[9].items[10].colorScaleMaximum | int | `150` |  |
| initConfig.catalog[9].items[10].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[9].items[10].featureInfoTemplate | string | `"<p>TRMM daily 3B42 2008</p><chart src=\"http://thredds:8080/thredds/ncss/TRMM/TRMM_3B42.2008.daily_V7.nc?var=precip&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2008-01-01T00:00:00Z&time_end=2008-12-31T00:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[9].items[10].layers | string | `"precip"` |  |
| initConfig.catalog[9].items[10].name | string | `"TRMM daily 2008"` |  |
| initConfig.catalog[9].items[10].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[9].items[10].type | string | `"wms"` |  |
| initConfig.catalog[9].items[10].url | string | `"http://thredds:8080/thredds/wms/TRMM/TRMM_3B42.2008.daily_V7.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[9].items[11].colorScaleMaximum | int | `150` |  |
| initConfig.catalog[9].items[11].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[9].items[11].featureInfoTemplate | string | `"<p>TRMM daily 3B42 2009</p><chart src=\"http://thredds:8080/thredds/ncss/TRMM/TRMM_3B42.2009.daily_V7.nc?var=precip&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2009-01-01T00:00:00Z&time_end=2009-12-31T00:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[9].items[11].layers | string | `"precip"` |  |
| initConfig.catalog[9].items[11].name | string | `"TRMM daily 2009"` |  |
| initConfig.catalog[9].items[11].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[9].items[11].type | string | `"wms"` |  |
| initConfig.catalog[9].items[11].url | string | `"http://thredds:8080/thredds/wms/TRMM/TRMM_3B42.2009.daily_V7.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[9].items[12].colorScaleMaximum | int | `150` |  |
| initConfig.catalog[9].items[12].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[9].items[12].featureInfoTemplate | string | `"<p>TRMM daily 3B42 2010</p><chart src=\"http://thredds:8080/thredds/ncss/TRMM/TRMM_3B42.2010.daily_V7.nc?var=precip&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2010-01-01T00:00:00Z&time_end=2010-12-31T00:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[9].items[12].layers | string | `"precip"` |  |
| initConfig.catalog[9].items[12].name | string | `"TRMM daily 2010"` |  |
| initConfig.catalog[9].items[12].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[9].items[12].type | string | `"wms"` |  |
| initConfig.catalog[9].items[12].url | string | `"http://thredds:8080/thredds/wms/TRMM/TRMM_3B42.2010.daily_V7.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[9].items[13].colorScaleMaximum | int | `150` |  |
| initConfig.catalog[9].items[13].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[9].items[13].featureInfoTemplate | string | `"<p>TRMM daily 3B42 2011</p><chart src=\"http://thredds:8080/thredds/ncss/TRMM/TRMM_3B42.2011.daily_V7.nc?var=precip&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2011-01-01T00:00:00Z&time_end=2011-12-31T00:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[9].items[13].layers | string | `"precip"` |  |
| initConfig.catalog[9].items[13].name | string | `"TRMM daily 2011"` |  |
| initConfig.catalog[9].items[13].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[9].items[13].type | string | `"wms"` |  |
| initConfig.catalog[9].items[13].url | string | `"http://thredds:8080/thredds/wms/TRMM/TRMM_3B42.2011.daily_V7.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[9].items[14].colorScaleMaximum | int | `150` |  |
| initConfig.catalog[9].items[14].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[9].items[14].featureInfoTemplate | string | `"<p>TRMM daily 3B42 2012</p><chart src=\"http://thredds:8080/thredds/ncss/TRMM/TRMM_3B42.2012.daily_V7.nc?var=precip&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2012-01-01T00:00:00Z&time_end=2012-12-31T00:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[9].items[14].layers | string | `"precip"` |  |
| initConfig.catalog[9].items[14].name | string | `"TRMM daily 2012"` |  |
| initConfig.catalog[9].items[14].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[9].items[14].type | string | `"wms"` |  |
| initConfig.catalog[9].items[14].url | string | `"http://thredds:8080/thredds/wms/TRMM/TRMM_3B42.2012.daily_V7.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[9].items[15].colorScaleMaximum | int | `150` |  |
| initConfig.catalog[9].items[15].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[9].items[15].featureInfoTemplate | string | `"<p>TRMM daily 3B42 2013</p><chart src=\"http://thredds:8080/thredds/ncss/TRMM/TRMM_3B42.2013.daily_V7.nc?var=precip&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2013-01-01T00:00:00Z&time_end=2013-12-31T00:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[9].items[15].layers | string | `"precip"` |  |
| initConfig.catalog[9].items[15].name | string | `"TRMM daily 2013"` |  |
| initConfig.catalog[9].items[15].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[9].items[15].type | string | `"wms"` |  |
| initConfig.catalog[9].items[15].url | string | `"http://thredds:8080/thredds/wms/TRMM/TRMM_3B42.2013.daily_V7.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[9].items[1].colorScaleMaximum | int | `150` |  |
| initConfig.catalog[9].items[1].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[9].items[1].featureInfoTemplate | string | `"<p>TRMM daily 3B42 1999</p><chart src=\"http://thredds:8080/thredds/ncss/TRMM/TRMM_3B42.1999.daily_V7.nc?var=precip&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=1999-01-01T00:00:00Z&time_end=1999-12-31T00:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[9].items[1].layers | string | `"precip"` |  |
| initConfig.catalog[9].items[1].name | string | `"TRMM daily 1999"` |  |
| initConfig.catalog[9].items[1].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[9].items[1].type | string | `"wms"` |  |
| initConfig.catalog[9].items[1].url | string | `"http://thredds:8080/thredds/wms/TRMM/TRMM_3B42.1999.daily_V7.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[9].items[2].colorScaleMaximum | int | `150` |  |
| initConfig.catalog[9].items[2].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[9].items[2].featureInfoTemplate | string | `"<p>TRMM daily 3B42 2000</p><chart src=\"http://thredds:8080/thredds/ncss/TRMM/TRMM_3B42.2000.daily_V7.nc?var=precip&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2000-01-01T00:00:00Z&time_end=2000-12-31T00:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[9].items[2].layers | string | `"precip"` |  |
| initConfig.catalog[9].items[2].name | string | `"TRMM daily 2000"` |  |
| initConfig.catalog[9].items[2].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[9].items[2].type | string | `"wms"` |  |
| initConfig.catalog[9].items[2].url | string | `"http://thredds:8080/thredds/wms/TRMM/TRMM_3B42.2000.daily_V7.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[9].items[3].colorScaleMaximum | int | `150` |  |
| initConfig.catalog[9].items[3].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[9].items[3].featureInfoTemplate | string | `"<p>TRMM daily 3B42 2001</p><chart src=\"http://thredds:8080/thredds/ncss/TRMM/TRMM_3B42.2001.daily_V7.nc?var=precip&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2001-01-01T00:00:00Z&time_end=2001-12-31T00:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[9].items[3].layers | string | `"precip"` |  |
| initConfig.catalog[9].items[3].name | string | `"TRMM daily 2001"` |  |
| initConfig.catalog[9].items[3].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[9].items[3].type | string | `"wms"` |  |
| initConfig.catalog[9].items[3].url | string | `"http://thredds:8080/thredds/wms/TRMM/TRMM_3B42.2001.daily_V7.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[9].items[4].colorScaleMaximum | int | `150` |  |
| initConfig.catalog[9].items[4].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[9].items[4].featureInfoTemplate | string | `"<p>TRMM daily 3B42 2002</p><chart src=\"http://thredds:8080/thredds/ncss/TRMM/TRMM_3B42.2002.daily_V7.nc?var=precip&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2002-01-01T00:00:00Z&time_end=2002-12-31T00:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[9].items[4].layers | string | `"precip"` |  |
| initConfig.catalog[9].items[4].name | string | `"TRMM daily 2002"` |  |
| initConfig.catalog[9].items[4].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[9].items[4].type | string | `"wms"` |  |
| initConfig.catalog[9].items[4].url | string | `"http://thredds:8080/thredds/wms/TRMM/TRMM_3B42.2002.daily_V7.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[9].items[5].colorScaleMaximum | int | `150` |  |
| initConfig.catalog[9].items[5].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[9].items[5].featureInfoTemplate | string | `"<p>TRMM daily 3B42 2003</p><chart src=\"http://thredds:8080/thredds/ncss/TRMM/TRMM_3B42.2003.daily_V7.nc?var=precip&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2003-01-01T00:00:00Z&time_end=2003-12-31T00:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[9].items[5].layers | string | `"precip"` |  |
| initConfig.catalog[9].items[5].name | string | `"TRMM daily 2003"` |  |
| initConfig.catalog[9].items[5].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[9].items[5].type | string | `"wms"` |  |
| initConfig.catalog[9].items[5].url | string | `"http://thredds:8080/thredds/wms/TRMM/TRMM_3B42.2003.daily_V7.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[9].items[6].colorScaleMaximum | int | `150` |  |
| initConfig.catalog[9].items[6].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[9].items[6].featureInfoTemplate | string | `"<p>TRMM daily 3B42 2004</p><chart src=\"http://thredds:8080/thredds/ncss/TRMM/TRMM_3B42.2004.daily_V7.nc?var=precip&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2004-01-01T00:00:00Z&time_end=2004-12-31T00:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[9].items[6].layers | string | `"precip"` |  |
| initConfig.catalog[9].items[6].name | string | `"TRMM daily 2004"` |  |
| initConfig.catalog[9].items[6].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[9].items[6].type | string | `"wms"` |  |
| initConfig.catalog[9].items[6].url | string | `"http://thredds:8080/thredds/wms/TRMM/TRMM_3B42.2004.daily_V7.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[9].items[7].colorScaleMaximum | int | `150` |  |
| initConfig.catalog[9].items[7].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[9].items[7].featureInfoTemplate | string | `"<p>TRMM daily 3B42 2005</p><chart src=\"http://thredds:8080/thredds/ncss/TRMM/TRMM_3B42.2005.daily_V7.nc?var=precip&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2005-01-01T00:00:00Z&time_end=2005-12-31T00:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[9].items[7].layers | string | `"precip"` |  |
| initConfig.catalog[9].items[7].name | string | `"TRMM daily 2005"` |  |
| initConfig.catalog[9].items[7].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[9].items[7].type | string | `"wms"` |  |
| initConfig.catalog[9].items[7].url | string | `"http://thredds:8080/thredds/wms/TRMM/TRMM_3B42.2005.daily_V7.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[9].items[8].colorScaleMaximum | int | `150` |  |
| initConfig.catalog[9].items[8].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[9].items[8].featureInfoTemplate | string | `"<p>TRMM daily 3B42 2006</p><chart src=\"http://thredds:8080/thredds/ncss/TRMM/TRMM_3B42.2006.daily_V7.nc?var=precip&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2006-01-01T00:00:00Z&time_end=2006-12-31T00:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[9].items[8].layers | string | `"precip"` |  |
| initConfig.catalog[9].items[8].name | string | `"TRMM daily 2006"` |  |
| initConfig.catalog[9].items[8].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[9].items[8].type | string | `"wms"` |  |
| initConfig.catalog[9].items[8].url | string | `"http://thredds:8080/thredds/wms/TRMM/TRMM_3B42.2006.daily_V7.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[9].items[9].colorScaleMaximum | int | `150` |  |
| initConfig.catalog[9].items[9].colorScaleMinimum | int | `0` |  |
| initConfig.catalog[9].items[9].featureInfoTemplate | string | `"<p>TRMM daily 3B42 2007</p><chart src=\"http://thredds:8080/thredds/ncss/TRMM/TRMM_3B42.2007.daily_V7.nc?var=precip&latitude={{terria.coords.latitude}}&longitude={{terria.coords.longitude}}&time_start=2007-01-01T00:00:00Z&time_end=2007-12-31T00:00:00Z&accept=csv\" y-column=\"3\" hide-buttons=\"True\"></chart>"` |  |
| initConfig.catalog[9].items[9].layers | string | `"precip"` |  |
| initConfig.catalog[9].items[9].name | string | `"TRMM daily 2007"` |  |
| initConfig.catalog[9].items[9].styles | string | `"boxfill/blu-yellow"` |  |
| initConfig.catalog[9].items[9].type | string | `"wms"` |  |
| initConfig.catalog[9].items[9].url | string | `"http://thredds:8080/thredds/wms/TRMM/TRMM_3B42.2007.daily_V7.nc?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[9].name | string | `"TRMM"` |  |
| initConfig.catalog[9].preserveOrder | bool | `true` |  |
| initConfig.catalog[9].type | string | `"group"` |  |
| initConfig.homeCamera.east | int | `177` |  |
| initConfig.homeCamera.north | int | `-5` |  |
| initConfig.homeCamera.south | int | `-24` |  |
| initConfig.homeCamera.west | int | `152` |  |
| initConfig.viewerMode | string | `"2d"` |  |
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
