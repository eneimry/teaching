---
layout: default
title: Session 1
parent: Tectonic Geomorphology
nav_order: 2
---

<!-- ---
layout: default
title: Session 1
permalink: /tecto/session-1
--- -->

# Session 1 - Introduction and DEM manipulation

## Objectives of the day

1. Clarify everything that is possible to clarify (and solve problems ?). **Write questions in the chat of the TP channel on Teams**.
   - CISM login / Access to the UCLouvain network in the coming days.
   - Workflow of the morphometric analysis for the Tros-Marets river.
2. Download the **filled** DEM of your study area and create a project in QGIS. It is important that everybody manipulates the DEM and QGIS. Even if you do not like physical geography, learning QGIS is an important transversal skill to develop !
   - Projection: UTM 31 N (EPSG:32631). Make sure that both your data frame and all your outputs are in this projection.
   - [Link](https://nextcloud.cism.ucl.ac.be/s/3JRTbXY6kqe9cyM)
3. Qualitative morphometric analysis of the study area
   - Compute Hillshade and Slope as raster layers.
   - Highlight (map features in a shapefile) high slopes, discontinuities in the landscape, valley widening, river network
     pattern
   - Link your qualitative observations with the geological setting and literature

-----

## Data

DEM data to use locally, i.e. in QGIS: [Link](https://nextcloud.cism.ucl.ac.be/s/3JRTbXY6kqe9cyM)

## Qualitative analysis

### Set DEM symbology

To properly render a DEM in a GIS, the idea is to ask QGIS to render values only on the currently visible range of pixel values. To do so:

1. Open the properties of the layer.
2. Open the "Symbology" tab.
3. In the "Min/Max Value Settings" section, define "Statistics Extent" as "Updated canvas" in the dropdown menu.
    ![raster-rendering](imgs/qgis-stretch-values.png)
4. Zoom in on small portions of the DEM. You will see that the colour of the pixels will adapt to the range of the visible elevation.

### Slope and hillshade

Computing hillshade and slope will help you to get a better visualisation of the topography. Both toolboxes are available in the menu "Raster > Analysis".

The typical purpose of the hillshade it to create a 3D impression of your DEM. To do that, the hillshade should be superimposed to the DEM with a given transparency. To set the transparency, choose the tab "Transparency" in the layer properties.

### Transversal profiles

Draw transversal profiles to capture the global topography of the area, using the plugin "Profile tool" (see additional resources). Export the output into a text file and process it in Excel or R.

### Analysis of the DEM

If it helps, first compute the river network. The DEM that you downloaded is **already filled**.

Using the hillshaded DEM, you can do the following steps just by visual inspection :

- characterise the drainage river pattern (dentritic, parallel, rectangular), and changes
- highlight discontinuities in the drainage pattern, meandering behaviour, ...
- identify ridges, depressions, discontinuities in the topography
- map human infrastructures that divert the course of the rivers.

### Confront your observations with literature / geological setting
