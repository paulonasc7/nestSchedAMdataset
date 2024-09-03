# Nesting and scheduling in Additive Manufacturing
This repository contains instances and respective results for the Additive Manufacturing (AM) nesting and scheduling problem and was created based on the following works:
 - "Optimal decomposition approach for solving large nesting and scheduling problems of additive manufacturing systems"
 - "Improving the efficiency of Logic-based Benders Decomposition for production scheduling problmes"

## The AM nesting and scheduling problem
The AM nesting and scheduling problem consists of grouping a set of parts into batches and, subsequently, assigning and sequencing those batches in the machines available. This resembles a classical batch processing machine scheduling problem. The caveat is that the process of grouping parts into batches requires a 2D or 3D packing problem to guarantee that parts within a batch can be positioned in the building platform of the AM machine without overlapping. In this case, a 2D packing problem with irregular-shaped parts is considered, which is designated as nesting. To tackle nesting, the dotted-board model is used, where the building platform of the AM machines (i.e., the placement area) is represented by a mesh of dots that are evenly distributed and parts have a positioning point that is assigned to one of those dots.

## Data
Each folder contains the instances randomly generated for each number of parts. In the "1.Polygons" folder, the parts (polygons) created can be seen in allPolygons.txt. The area of the parts (area.txt) can also be seen. In the "2.PartsSpecs" folder it is possible to see all the instances that were tested for the parts created. Each instance has information about the parts' release date, processing time, due date, and area. For more information on how these release dates, processing times, and due dates were calculated, see the original paper. The indices of the parts follow the order by which they appear in the respective files.

## Results
The results of the COPCSP algorithm and the MIPCSP algorithm can be seen in the Results folder. The files with the results are named "nbParts-nbDots-nbMachines.xlsx", where nbParts is the number of parts to schedule, nBdots is the number of dots used to represent the building platform, and nbMachines is the number of machines considered. Each file has the results for all of the instances that consider the respective combination.
