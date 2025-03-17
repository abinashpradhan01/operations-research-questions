## Unit 1: Linear Programming Problems

### Q1: Explain the concept of Linear Programming with an example.

Linear Programming (LP) is a mathematical optimization technique used to find the best outcome in a mathematical model whose requirements are represented by linear relationships. It involves maximizing or minimizing a linear objective function subject to linear constraints.

**Example:**
A furniture manufacturer produces tables and chairs. Each table requires 4 hours of carpentry and 2 hours of finishing. Each chair requires 3 hours of carpentry and 1 hour of finishing. The workshop has 240 hours of carpentry time and 100 hours of finishing time available each week. If the profit is $70 per table and $50 per chair, determine the production mix that maximizes profit.

**Mathematical formulation:**
Let x = number of tables, y = number of chairs

Maximize: Z = 70x + 50y (Profit function)
Subject to:
- 4x + 3y ≤ 240 (Carpentry constraint)
- 2x + y ≤ 100 (Finishing constraint)
- x ≥ 0, y ≥ 0 (Non-negativity constraints)

### Q2: Describe the Graphical Method of solving LPP.

The Graphical Method is used to solve linear programming problems with two decision variables:

1. Plot the constraints on a coordinate plane.
2. Identify the feasible region (area satisfying all constraints).
3. Find the coordinates of all corner points of the feasible region.
4. Evaluate the objective function at each corner point.
5. Select the point that gives the optimal value of the objective function.

For maximization problems, the optimal solution is the corner point with the highest objective function value; for minimization, it's the lowest.

### Q3: What are the advantages and limitations of the Simplex Method?

**Advantages:**
1. Can solve problems with many variables and constraints, unlike the graphical method.
2. Systematically moves from one basic feasible solution to another with improved objective function value.
3. Provides sensitivity analysis information.
4. Computationally efficient for most practical problems.
5. Can handle both maximization and minimization problems.

**Limitations:**
1. Requires problems to be in standard form, often necessitating variable transformations.
2. May require many iterations for large problems.
3. Can be computationally expensive for very large problems.
4. Susceptible to degeneracy, which can cause cycling in rare cases.
5. Not suitable for non-linear programming problems.

### Q4: Explain the Big-M Method with an example.

The Big-M Method is used to solve linear programming problems with greater-than-or-equal-to (≥) constraints or equality constraints by introducing artificial variables with large penalty costs.

**Steps:**
1. Convert all constraints to standard form.
2. Add artificial variables to ≥ constraints and equality constraints.
3. Modify the objective function by subtracting M times the sum of artificial variables (for maximization) or adding M times the sum (for minimization), where M is a very large positive number.
4. Solve using the simplex method.
5. In the optimal solution, all artificial variables must be zero.

**Example:**
Minimize: Z = 3x + 2y
Subject to:
- x + y ≥ 5
- x + 2y ≤ 10
- x, y ≥ 0

Convert to standard form:
- x + y - s₁ + a₁ = 5 (adding slack s₁ and artificial a₁)
- x + 2y + s₂ = 10 (adding slack s₂)
- x, y, s₁, s₂, a₁ ≥ 0

Modified objective: Z = 3x + 2y + Ma₁

The Big-M method penalizes any solution with a₁ > 0, forcing the simplex algorithm to find a solution where a₁ = 0.

### Q5: How do you identify a Degenerate Solution in LPP?

A degenerate solution in linear programming occurs when one or more basic variables equal zero in a basic feasible solution. Mathematically, in a problem with m constraints and n variables, a basic solution involves m basic variables. If any of these basic variables is zero, the solution is degenerate.

**Identification:**
1. In the simplex tableau, if any basic variable has a value of zero, the solution is degenerate.
2. In the context of the graphical method, degeneracy occurs when more than two constraints intersect at a single point.

Degeneracy can cause computational difficulties as it may lead to cycling in the simplex algorithm, where the algorithm moves between the same set of basic feasible solutions without improving the objective function.

### Q6: Explain the concept of Multiple Optimal Solutions.

Multiple optimal solutions exist when a linear programming problem has more than one feasible solution that yields the same optimal value of the objective function.

**Characteristics:**
1. Occurs when the objective function is parallel to one of the constraint lines or planes.
2. Any point on the line segment connecting two optimal corner points is also optimal.
3. All points on this line segment have the same objective function value.

**Identification:**
- In the simplex method, multiple optimal solutions are indicated when, in the final tableau, at least one non-basic variable has a zero coefficient in the objective row.
- Graphically, multiple optimal solutions occur when the objective function line is parallel to a constraint that forms part of the boundary of the feasible region.

### Q7: How can you determine an Unbounded Solution?

An unbounded solution in linear programming occurs when the objective function can be improved indefinitely without violating any constraints.

**Identification:**
1. In the simplex method, an unbounded solution is indicated when:
   - A positive entry exists in the objective row (for maximization) or a negative entry (for minimization).
   - All entries in the column corresponding to this entry in the constraint rows are negative or zero.
   
2. Graphically, an unbounded solution occurs when:
   - The feasible region extends infinitely in the direction of improving the objective function.
   - The feasible region is not closed in the direction of optimization.

An unbounded solution typically indicates a modeling error, as most real-world problems have natural bounds.

### Q8: Explain the role of Slack and Surplus Variables in LPP.

**Slack Variables:**
- Added to less-than-or-equal-to (≤) constraints to convert them to equalities.
- Represent unused resources or capacity.
- Example: If constraint is x + y ≤ 10, it becomes x + y + s = 10, where s ≥ 0 is the slack variable.

**Surplus Variables:**
- Added to greater-than-or-equal-to (≥) constraints to convert them to equalities.
- Represent excess over the minimum requirement.
- Example: If constraint is x + y ≥ 5, it becomes x + y - s = 5, where s ≥ 0 is the surplus variable.

**Roles:**
1. Convert inequality constraints to equality constraints for the simplex method.
2. Provide economic interpretation (unused resources or excess production).
3. Help identify the basic feasible solutions.
4. Facilitate the implementation of the simplex algorithm.

### Q9: How does the Simplex Method work?

The Simplex Method is an iterative algorithm that moves from one basic feasible solution to another, improving the objective function value until reaching the optimal solution.

**Steps:**
1. **Initialization:**
   - Convert the problem to standard form using slack, surplus, and artificial variables.
   - Create an initial feasible solution (usually with slack/artificial variables as basic variables).

2. **Iteration:**
   - **Entering Variable Selection:** Choose a non-basic variable with the most negative coefficient in the objective row (for maximization) to enter the basis.
   - **Departing Variable Selection:** Use the minimum ratio test to determine which basic variable leaves the basis.
   - **Pivot:** Perform row operations to update the tableau.

3. **Optimality Check:**
   - For maximization: If all coefficients in the objective row are non-negative, the current solution is optimal.
   - For minimization: If all coefficients are non-positive, the current solution is optimal.

4. **Extract Solution:**
   - Basic variables and their values form the optimal solution.
   - The value of the objective function is in the right-hand corner of the tableau.

### Q10: Discuss the significance of the Feasible Region in LPP.

The feasible region in linear programming is the set of all possible solutions that satisfy all constraints of the problem. It represents the decision space within which the optimal solution must lie.

**Significance:**
1. **Boundary of Search:** Defines the limits within which the optimal solution must be found.
2. **Corner Point Property:** The optimal solution to a linear programming problem (if it exists) will occur at a corner point of the feasible region.
3. **Feasibility Analysis:** Helps determine if a problem has a solution. If the feasible region is empty, the problem has no solution.
4. **Sensitivity Analysis:** Changes in constraints affect the shape and size of the feasible region, which impacts the optimal solution.
5. **Geometric Interpretation:** Provides visual understanding of the problem in two or three dimensions.
6. **Constraint Binding:** Identifies which constraints are binding (active) at the optimal solution.

## Unit 2: Transportation and Assignment Problems

### Q1: Explain the N.W. Corner Rule with an example.

The Northwest Corner Rule is a method for finding an initial basic feasible solution to a transportation problem. It starts from the northwest (top-left) corner of the transportation table and allocates maximum possible units based on supply and demand constraints.

**Steps:**
1. Start from the northwest corner (top-left cell).
2. Allocate the maximum possible amount based on supply and demand constraints.
3. Cross out the row or column that is satisfied (supply exhausted or demand met).
4. Move to the next available cell (right if column is satisfied, down if row is satisfied).
5. Repeat until all supplies and demands are satisfied.

**Example:**
Consider a transportation problem with 3 sources (S₁, S₂, S₃) and 3 destinations (D₁, D₂, D₃) with the following supply and demand:
- Supply: S₁ = 50, S₂ = 40, S₃ = 60
- Demand: D₁ = 30, D₂ = 50, D₃ = 70

**Solution using NW Corner Rule:**
1. Start at cell (S₁, D₁): Allocate 30 units (D₁'s demand is satisfied)
2. Move to (S₁, D₂): Allocate 20 units (S₁'s supply is exhausted)
3. Move to (S₂, D₂): Allocate 30 units (D₂'s demand is satisfied)
4. Move to (S₂, D₃): Allocate 10 units (S₂'s supply is exhausted)
5. Move to (S₃, D₃): Allocate 60 units (S₃'s supply is exhausted and D₃'s demand is satisfied)

Total allocation: 30 + 20 + 30 + 10 + 60 = 150 units

### Q2: What are the merits and demerits of the Least Cost Method?

The Least Cost Method is an approach for finding an initial basic feasible solution to a transportation problem by allocating units based on the lowest transportation costs.

**Merits:**
1. Generally produces a better initial solution than the Northwest Corner Rule.
2. Considers the cost aspect, which is economically more rational.
3. Reduces the number of iterations required to reach the optimal solution.
4. More efficient for problems with widely varying transportation costs.
5. Often provides a solution closer to the optimal solution.

**Demerits:**
1. More complex and time-consuming than the Northwest Corner Rule.
2. Requires repeated scanning of the entire cost matrix to find the lowest cost cell.
3. May not always provide the optimal solution (still just an initial solution).
4. May result in degeneracy if not implemented carefully.
5. Less intuitive than the Northwest Corner Rule.

### Q3: Describe the steps involved in Vogel's Approximation Method.

Vogel's Approximation Method (VAM) is an improved method for finding an initial basic feasible solution to transportation problems that often provides a near-optimal solution.

**Steps:**
1. **Calculate Penalty:**
   - For each row, find the difference between the two lowest costs (penalty).
   - For each column, find the difference between the two lowest costs (penalty).

2. **Select Highest Penalty:**
   - Identify the row or column with the highest penalty.
   - If there's a tie, choose arbitrarily or use a secondary criterion.

3. **Allocate:**
   - In the selected row or column, find the cell with the lowest cost.
   - Allocate the maximum possible amount to this cell based on supply and demand constraints.
   - Cross out the satisfied row or column (where supply or demand becomes zero).

4. **Recalculate:**
   - Recalculate penalties for the remaining rows and columns.
   - If a row or column has only one cell left, its penalty is the cost of that cell.

5. **Repeat:**
   - Repeat steps 2-4 until all supplies and demands are satisfied.

6. **Complete:**
   - Calculate the total transportation cost based on the allocations.

### Q4: What is the Hungarian Method, and how does it solve Assignment Problems?

The Hungarian Method is an algorithm for solving assignment problems optimally. It finds the optimal assignment of n workers to n jobs to minimize the total cost or maximize the total profit.

**Steps:**
1. **Row Reduction:**
   - Subtract the smallest element in each row from all elements in that row.

2. **Column Reduction:**
   - Subtract the smallest element in each column from all elements in that column.

3. **Cover Zero Elements:**
   - Draw minimum number of lines (horizontal and vertical) to cover all zeros in the matrix.
   - If the number of lines equals n (matrix size), an optimal assignment is possible.
   - If not, proceed to the next step.

4. **Create Additional Zeros:**
   - Find the smallest uncovered element.
   - Subtract it from all uncovered elements.
   - Add it to elements at the intersection of covering lines.
   - Return to step 3.

5. **Make Optimal Assignment:**
   - Make assignments in the reduced matrix, selecting one zero in each row and column.
   - Convert back to the original problem to determine the optimal assignment.

The Hungarian Method guarantees an optimal solution in O(n³) time complexity.

### Q5: Explain Balanced vs Unbalanced Transportation Problems.

**Balanced Transportation Problem:**
- Total supply equals total demand: ∑S₍ᵢ₎ = ∑D₍ⱼ₎
- Every unit of supply can be transported to meet demand.
- The transportation table forms a closed system.
- Standard methods can be applied directly.

**Unbalanced Transportation Problem:**
- Total supply does not equal total demand: ∑S₍ᵢ₎ ≠ ∑D₍ⱼ₎
- Two possible scenarios:
  1. Supply exceeds demand (∑S₍ᵢ₎ > ∑D₍ⱼ₎): Introduce a dummy destination with demand equal to excess supply.
  2. Demand exceeds supply (∑S₍ᵢ₎ < ∑D₍ⱼ₎): Introduce a dummy source with supply equal to excess demand.
- Dummy cells typically have zero transportation cost.
- After balancing, standard methods can be applied.

An unbalanced problem indicates either excess capacity or unfulfilled demand in the system.

