# Datos de servicios ecosistémicos

## Servicios ecosistémicos
### GAM

```shell
cd gam

# Embalses
ogr2ogr -f GeoJSON -nln embalses_gam -t_srs EPSG:4326 -makevalid embalses_gam.geojson EmbGAM.shp
del EmbGAM.*
```
