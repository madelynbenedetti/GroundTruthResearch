# Sumamry of all files
Repository storing all used codes for research concerning “Establishing Ground Truth for Seismic Wave Velocities in Root-Soil Systems of the Critical Zone”. All code is written in Python and stored in Google Colab files. Due to my limited experience with complex Python code, many of these scripts were written with AI assistance to streamline the process.

**Velocities Vs. Mediums Plot.ipynb** - This script is to create a velocity vs. medium plot from benchtop experimental data. This includes dry and wet wood (parallel or perpendicular), soil samples, and aluminum. The script produces a linear and an exponential box-and-whisker plot, as well as a list of average velocities for each medium. 

**"SSC Set-Up Figures.ipynb"** - This script is used to develop the SSC cross-section and SSC Birds-Eye View figures. The user selects which objects they’d like to show or hide (e.g., shot locations, compaction zone, labels, sensor groups). The code outputs a figure for different experimental setups.

**The primary program: SSC_First_Arrivals_Ray_Tracing.ipynb** - This is the script where all first arrivals are picked. The program accepts .asd trace files and produces an interactive graph for making first-arrival picks. The picks are stored in a .pkl file, which can be used as a save state. Once all picks are made, they are exported to a CSV. During this, the program ray-traces the shortest path from the shot to each sensor based on the first-arrival picks. Experimental data is saved to a [Hugging Face](https://huggingface.co/datasets/mbenedetti212/SSC_All_Experiment_Traces) dataset.


