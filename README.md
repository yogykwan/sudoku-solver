# sudoku-ai
AI agent that could solve the Diagonal Sudoku game with DFS and constraints propagation (elimination, only choice and naked twin).

## Code

* `solution.py` - Diagonal sudoku solution with DFS and constraints propagation (elimination, only choice and naked twin).
* `solution_test.py` - Unittest for naked twins and diagonal sudoku.
* `PySudoku.py` - Visualize solution process in PyGame.
* `visualize.py` -  Filter assignments of boxes for each step.


## Deploy

```
conda env create -f environment.yaml
```

## Run
```
python solution.py
python solution_test.py
```

## Q&A

### Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: In each unit, find two same boxes and length of each pending value is 2. Then we could eliminate these 2 digits from other boxes in this unit. Thus, this will introduces new constraints for other parts.

### Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: Construct two more units based on two diagonals. For every box in each diagonal, update its variables units and peers. Then, each time we will also do elimination, only choice and naked twins on diagonals. Thus, more constraints are introduced.

