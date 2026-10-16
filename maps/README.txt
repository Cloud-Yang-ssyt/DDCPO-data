Grid-map data accompanying the DDCPO manuscript

Contents
Five binary input grids, of sizes 20x20, 30x30, 40x40, 50x50 and 60x60,
used for the path-planning illustrations in Figures 5 and 6.

CSV format
Each file contains only the numeric matrix, with no header or index column.
0 = free cell; 1 = obstacle cell. Coordinates use one-based (row, column)
indices. The start is (1, 1); the goal is (n, n).

Orientation
The CSVs retain the optimization-grid row/column order. In the paper's
Cartesian plot, a cell center is at x = column - 0.5, y = row - 0.5;
row 1 is at the bottom. Reverse the rows when rendering with an image
viewer whose first row is displayed at the top. map_metadata.json records
the dimensions, endpoints and figure correspondence for every grid.

Provenance and scope
The matrices were exported from the saved numerical data used to prepare
the manuscript's final path-planning figures. No map cells were edited.
This folder contains input maps, rather than algorithm source code or
path-planning run outputs.
