# Introductory Project: Diagonal Sudoku Solver
For this project, I will implement 2 extensions to the Sudoku algorithm developed in the lectures:
* The first extension will be an implementation of the `naked twins` technique. 
* The second will be a modification of the algorithm to solve a `diagonal sudoku`.

## Questions:
### Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: "Naked Twins" is an additional strategy equivalent to "only_choise" or "eliminate" in order to reduce search space. For this purpouse in the code we iterate over all units (3x3 block, column, row or diagonal), in each unit we are looking for a pair of boxes such that each box contain exactly the same pair of digits, if such group exists we eliminate digits from the pair from all other boxes in a unit.

### Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: In diagonal sudoku problem we have two more constraints comparing to plain sudoku: numbers on main diagonal (from left top to right bottom) and secondary diagonal (from top right to bottom left) can appear only once. In order to solve this we only had to create two additional units that represent these diagonals and including them in the process of applying strategies (only_choise, elimination and naked_twins). However in the program just represents update the code where list of different units is computed and a dictionary of neighbour boxes is computed.



## Environment & code

### Environment
I have followed IAND instructions for setting up my conda environment. In this project I used **Python 3**, [Anaconda](https://www.continuum.io/downloads) that uses the environment provided in the Anaconda lesson of the Nanodegree. I installed pygame to see my visualization.  To visualize my solution, I only assign values to the values_dict using the ```assign_values``` function provided in solution.py.


### Code of this repository
* `solutions.py` - You'll fill this in as part of your solution.
* `solution_test.py` - Do not modify this. You can test your solution by running `python solution_test.py`.
* `PySudoku.py` - Do not modify this. This is code for visualizing your solution.
* `visualize.py` - Do not modify this. This is code for visualizing your solution.
* `solution.ipynb` - Contains the notebook version that helped me to create the final solution (use jupiter notebook)
This code can be tested as follows:
```
$ source activate aind
(aind) $ git clone https://github.com/JordiTorresUdacity/AIND-Sudoku.git
(aind) $ cd AIND-Sudoku/
(aind) $ python solution_test.py
(aind) $ python solution.py

```
 
