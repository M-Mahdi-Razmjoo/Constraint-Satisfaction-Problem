# Constraint Satisfaction Problem (CSP) Solver
This project provides an implementation of a Constraint Satisfaction Problem (CSP) solver. CSPs are mathematical problems defined by a set of variables that must be assigned values while satisfying a series of constraints. This approach is commonly used in artificial intelligence, particularly in fields requiring decision-making under constraints, such as scheduling, planning, and resource allocation.

## Project Overview
A ***CSP*** is formulated as:

**Variables:** A set of variables, each representing an element in the problem. For example, in a scheduling problem, each task could be a variable.
**Domains:** Each variable has a domain of possible values it can take. For example, a task's domain might be a list of possible time slots.
**Constraints:** A set of restrictions that define the valid combinations of variable assignments. For example, certain tasks cannot occur at the same time.

## CSP Example: Sudoku Puzzle
In a Sudoku puzzle, each cell is a variable, the possible numbers (1-9) are the domain, and the constraints ensure that each number appears only once per row, column, and 3x3 sub-grid.

## Key Components

**Constraint Propagation:** Techniques like forward checking and arc-consistency are used to reduce the search space by enforcing constraints as early as possible.

**Backtracking Search:** This classic search technique tries different variable assignments, backtracking whenever a conflict (constraint violation) arises. While it is simple, it is also efficient when combined with constraint propagation.

**Heuristics:** The solver can be improved by incorporating heuristics like:
1-Minimum Remaining Values (MRV): Selects the variable with the fewest remaining values in its domain, which often leads to quicker solutions.
2-Degree Heuristic: Selects the variable with the highest number of constraints on other variables.
3-Least Constraining Value (LCV): Chooses the value that leaves the most options open for other variables.

## Algorithm Steps

**Define the Variables and Domains:** Initialize each variable and define its set of possible values.

**Apply Constraints:** Constraints between variables are defined to ensure only valid solutions are considered.

**Search with Constraint Propagation:**
1-Use backtracking to explore different assignments.
2-Apply constraint propagation techniques to reduce the domain size and prune paths that cannot lead to solutions.

**Check for Solution:** If all variables are assigned valid values without constraint violations, a solution is found.

## Applications

**Scheduling Problems:** Assigning tasks to time slots without conflicts, such as in meeting or class scheduling.

**Puzzle Solving:** Solving puzzles like Sudoku, where each cell must satisfy row, column, and sub-grid constraints.

**Resource Allocation:** Assigning resources to tasks in a way that meets specific constraints (e.g., project management, manufacturing).

**Assignment Problems:** Problems like map coloring or the N-Queens problem, where constraints guide the valid placement of elements.

## Limitations and Extensions

**Time Complexity:** CSP algorithms, especially those with backtracking, can be computationally expensive for large problems. The efficiency depends on the number of variables, domain size, and constraints.

**Constraint Propagation Enhancements:** Techniques like Arc-Consistency (AC-3) and Constraint Learning (Dynamic CSPs) can be added to improve efficiency by further reducing the search space.
















