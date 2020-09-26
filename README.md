# RasterTools

This is a set of small Java programs to conduct common tasks in preparing data for species distribution modeling. The programs need to be run from the command-line, using a command like `java -jar nameOfProgram.jar`. When run like this, the program will print out the flags that can be used to specify input files and control the program.

The applymask.jar program applies a landmask to an environmental raster. We have used this to homogenize the landmask between rasters in Bio-ORACLE. It adds no-data-values where data is available in pixels that are not supposed to have data and interpolates from surrounding pixels if a pixel that is supposed to have data doesn't have data.

The extractDataForCoordinates.jar program extracts data from a set of rasters in a folder for a file with species occurrence records (geographic coordinates). We use this to generate SWD files for Maxent runs.

The moveCoordinatesToClosestDataPixel.jar program reads a set of occurrence records. For every record that is situated in a no-data-pixel, the record is moved to the closest pixel that has data. The new coordinates are provided in csv format suitable for Maxent runs.

### Citation
If you find these tools useful, please cite them in your work. I recommend citing them as follows:
Verbruggen H. (2017) RasterTools: moveCoordinatesToClosestDataPixel.jar version 1.04. https://github.com/hverbruggen/RasterTools
(or similar citation for the other scripts).

### Notes and disclaimer
The RasterTools are in development and have not been tested extensively. It is quite plausible that incorrectly formatted input could lead to nonsensical output.
