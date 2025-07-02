# FLOPY_GA
Groundwater Optimization Code
This repository contains Python code for optimizing groundwater pumping and injection strategies using a genetic algorithm (PyGAD) coupled with groundwater flow and transport simulations (MODFLOW and MT3DMS via FloPy). The goal is to minimize the maximum concentration of a contaminant in the model domain.

Dependencies
This code requires the following Python libraries:

pygad: For implementing the genetic algorithm.
flopy: For interacting with MODFLOW and MT3DMS.
numpy: For numerical operations.
matplotlib: For plotting results.
You will also need compiled versions of MODFLOW and MT3DMS accessible from your system's PATH, or you will need to specify the paths to the executables in your Flopy model definition.

Required User Inputs
Before running the code, you need to provide the following input files from your MODFLOW and MT3DMS simulations:

optim.MODFLOW.IN: The main MODFLOW input file for your model. This file is loaded by flopy.modflow.Modflow.load().
mt3d.in: The main MT3DMS input file for your transport simulation. This file is loaded by flopy.mt3d.mt.Mt3dms.load().
These files are typically generated from a groundwater modeling program like Processing Modflow or GMS. Ensure these files are in the same directory as your Python script, or provide the full path to the files.

Usage
Ensure Dependencies are Installed: Make sure you have pygad, flopy, numpy, and matplotlib installed in your Python environment. You can install them using pip:
