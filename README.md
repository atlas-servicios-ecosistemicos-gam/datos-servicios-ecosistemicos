# Datos de servicios ecosistémicos

## Servicios ecosistémicos
### GAM

```shell
cd gam

# Energía hidroeléctrica - embalses
ogr2ogr -f GeoJSON -nln embalses_gam -t_srs EPSG:4326 -makevalid embalses_gam.geojson EmbGAM.shp
del EmbGAM.*

# Densidad de carbono en biomasa forestal
gdalwarp -t_srs EPSG:3857 -of vrt carbono_forestal_gam.tif /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ carbono_forestal_gam_web.tif
del carbono_forestal_gam.*
gdalwarp -t_srs EPSG:4326 -of vrt carbono_forestal_gam_web.tif /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ carbono_forestal_gam.tif
```
