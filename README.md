# AI Sudoku Solver

## Synopsis

This project extends the Sudoku-solving agent developed in the Udacity AI classroom lectures to solve _diagonal_ Sudoku puzzles and implement a new constraint strategy called "naked twins" (see the pseudocode [here](https://github.com/udacity/artificial-intelligence/blob/master/Projects/1_Sudoku/pseudocode.md). A diagonal Sudoku puzzle is identical to traditional Sudoku puzzles with the added constraint that the boxes on the two main diagonals of the board must also contain the digits 1-9 in each cell (just like the rows, columns, and 3x3 blocks). The naked twins strategy says that if you have two or more unallocated boxes in a unit and there are only two digits that can go in those two boxes, then those two digits can be eliminated from the possible assignments of all other boxes in the same unit.


## Quickstart Guide

1. Follow the instructions in the classroom lesson to install and configure the `aind` [Anaconda](https://www.continuum.io/downloads) environment which includes several important packages that are used for the project. OS X or Unix/Linux users can activate the aind environment by running the following (Windows users simply run `activate aind`):
    
    `$ source activate aind`

2. Run a small set of test cases using the local test suite. 

    `(aind)$ python -m unittest -v`

5. You can run the code with visualization (see the last section of the readme for more information)

    `(aind)$ python solution.py`


## Visualization

**Note:** The `pygame` library is required to visualize the solution -- however, the `pygame` module can be troublesome to install and configure. It should be installed by default with the AIND conda environment, but it is not reliable across all operating systems or versions. Please refer to the pygame documentation [here](http://www.pygame.org/download.shtml), or discuss among your peers in the slack group if you need help.

Running `python solution.py` will automatically attempt to visualize your solution, but you must use the provided `assign_value` function (defined in `utils.py`) to track the puzzle solution progress for reconstruction during visuzalization.
