---
layout: default
title: GDAL tools
parent: Tricks and tips
nav_order: 2
---

# Useful GDAL commands

## Mosaic raster files

To mosaic a list of DEM files, all the tiles should be in the same folder. Only the tiles that need to be mosaicked should be in the folder.

```bash
gdalwarp PATH_TO_FOLDER/* MY_DEM_MOSAIC.tif
```

## Reproject and convert to .bil format

LSDTopotools requires DEM in `bil` format, projected in the UTM coordinate system. The easiest way to properly format files is using the following procedure.

```bash
# Project DEM into UTM projection
gdalwarp -t_srs EPSG:32631 -of ENVI -dstnodata -9999 -tr 10 10 -r bilinear input_filename.tif output_filename.bil

# Convert the DEM into a ENVI BIL format
gdal_translate -of ENVI dem-input.tif dem-output.bil
```

More info [here](https://lsdtopotools.github.io/LSDTT_documentation/LSDTT_introduction_to_geospatial_data.html).

## Zip / Unzip folders

To zip folders:

```bash
zip -r MY_ZIPPED_FILE.zip MY_FOLDER_TO_ZIP
```

To unzip folders:

```bash
unzip MY_ZIPPED_FILE.zip
```
