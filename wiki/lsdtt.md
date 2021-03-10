---
layout: default
title: LSDTopoTools
parent: Tricks and tips
nav_order: 2
---

# LSDTopoTools tips

LSDTopotools requires DEM in `bil` format, projected in the UTM coordinate system. The easiest way to properly format files is using the following procedure.

```bash
# Project DEM into UTM projection
gdalwarp -t_srs '+proj=utm +zone=31 +datum=WGS84' -of ENVI -dstnodata -9999 -tr 10 10 -r bilinear input_filename.tif output_filename.bil
# Convert the DEM into a ENVI BIL format
gdal_translate -of ENVI dem-input.tif dem-output.bil
```

More info [here](https://lsdtopotools.github.io/LSDTT_documentation/LSDTT_introduction_to_geospatial_data.html).
