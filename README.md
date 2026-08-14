# The Effects of Applied Stress and Root-Soil Systems on Seismic Wave Velocities: Establishing Laboratory Ground Truth

## Research Overview

Trees and their root-soil systems play a key role in slope stability and natural hazard mitigation. By reinforcing the surrounding soil, root systems can reduce the likelihood of landslides, erosion, and slope failure. However, the subsurface root structure responsible for this effect remains poorly understood, limiting its incorporation into hazard assessment, infrastructure planning, and land management strategies.

Building on this gap, our research draws inspiration from the work of Brady Flinchum, who examined the extent of shear strengthening beneath longleaf pines, and Shiv M. Gupta, who characterized subsurface Critical Zone structure beneath Giant Sequoias. We aim to ground-truth root-driven shear strengthening through a series of controlled lab experiments conducted in the Seismic Soil Chamber (SSC). These experiments progress from simple to increasingly complex configurations, allowing us to isolate the relative contributions of overlying compaction and the presence, orientation, and moisture content of wood. The resulting data will inform an effective medium theory describing the mechanical behavior of root-soil systems. Finally, we will compare our results with Flinchum and Gupta’s field data and synthetic models to assess the accuracy and real-world implications of our findings.

## Research Objectives
* Create reproducible experiments to examine how tree roots and overlying stress influence seismic wave velocities in soil.
* Produce 2D seismic travel-time tomography models to resolve buried anomalies and stress bulbs (when overlying compaction is applied).
* Understand how overlying compaction and the presence of wood/roots appear in seismic tomography maps to better inform the findings of Flinchum and Gupta.
* Develop an effective medium theory of root-soil systems beneath trees for application in non-invasive root mapping and slope stability.

## Experimental design: Seismic Soil Chamber (SSC)










# About this repository
This repository contains all code used in research on “The Effects of Applied Stress and Root-Soil Systems on Seismic Wave Velocities: Establishing Laboratory Ground Truth”. All code is written in Python and stored in Google Colab files.

**Velocities Vs. Mediums Plot.ipynb** - This script is to create a velocity vs. medium plot from benchtop experimental data. This includes dry and wet wood (in parallel or perpendicular orientations), soil samples, and aluminum. The script produces linear and exponential box-and-whisker plots, as well as a list of average velocities for each medium. 

**SSC Set-Up Figures.ipynb** - This script is used to develop the SSC cross-section and SSC Birds-Eye View figures. The user selects which objects they’d like to show or hide (e.g., shot locations, compaction zone, labels, sensor groups). The code outputs a figure for different experimental setups.

**The primary program: SSC_First_Arrivals_Ray_Tracing.ipynb** - This is the script where all first arrivals are picked. The program accepts .asd trace files and produces an interactive graph for making first-arrival picks. The picks are stored in a .pkl file, which can be used as a save state. Once all picks are made, they are exported to a CSV. During this, the program ray-traces the shortest path from the shot to each sensor based on the first-arrival picks. Experimental data is saved to a [Hugging Face](https://huggingface.co/datasets/mbenedetti212/SSC_All_Experiment_Traces) dataset.


