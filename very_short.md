# Operations Research Short Answer Questions

## Unit-1: Linear Programming Problem (LPP)

1. **What is Linear Programming?**  
   Linear Programming is a mathematical optimization technique used to find the best outcome in a mathematical model with linear relationships.

2. **Define Basic Solution in LPP.**  
   A basic solution is a solution where the number of non-zero variables equals the number of constraints.

3. **What is a Feasible Solution?**  
   A feasible solution is a set of values for the decision variables that satisfies all the constraints of the LPP.

4. **Define Basic Feasible Solution.**  
   A basic feasible solution is a basic solution that satisfies all the constraints and non-negativity conditions.

5. **What is an Optimal Solution?**  
   An optimal solution is a feasible solution that achieves the best possible value of the objective function (maximum or minimum).

6. **What is a Degenerate Solution?**  
   A degenerate solution is a basic feasible solution where one or more basic variables have a value of zero.

7. **Define Unbounded Solution in LPP.**  
   An unbounded solution occurs when the objective function can be improved indefinitely without violating any constraints.

8. **What is a Multiple Optimal Solution?**  
   Multiple optimal solutions exist when there are two or more distinct feasible solutions that achieve the same optimal value of the objective function.

9. **What is Infeasibility in LPP?**  
   Infeasibility occurs when there is no solution that satisfies all the constraints of the LPP.

10. **What is the purpose of the Simplex Method?**  
    The Simplex Method is an algorithm used to find the optimal solution of a linear programming problem by moving from one basic feasible solution to another.

11. **Define Slack Variable.**  
    A slack variable is added to a less-than-or-equal-to constraint ($\leq$) to convert it into an equality constraint.

12. **What is a Surplus Variable?**  
    A surplus variable is subtracted from a greater-than-or-equal-to constraint ($\geq$) to convert it into an equality constraint.

13. **What is an Artificial Variable?**  
    An artificial variable is a non-negative variable added to equality constraints or greater-than-or-equal-to constraints to obtain an initial basic feasible solution.

14. **What is the objective function in LPP?**  
    The objective function is the linear function that is to be maximized or minimized in a linear programming problem.

15. **What is the difference between Graphical and Simplex Methods?**  
    The Graphical Method is limited to problems with only two variables and uses geometric representation, while the Simplex Method can handle multiple variables and uses algebraic iterations.

16. **What is the use of the Big-M Method?**  
    The Big-M Method is used to handle artificial variables in the simplex method by adding a large penalty coefficient (M) to artificial variables in the objective function.

17. **Define Convex Combination in LPP.**  
    A convex combination is a linear combination of points where all coefficients are non-negative and sum to 1.

18. **What is the significance of the Optimality Condition?**  
    The optimality condition determines whether the current basic feasible solution is optimal by checking if all reduced costs are non-negative (for maximization) or non-positive (for minimization).

19. **Define the term "Feasible Region."**  
    The feasible region is the set of all feasible solutions, represented by the area that satisfies all constraints in the LPP.

20. **What does the Simplex Tableau represent?**  
    The Simplex Tableau is a matrix representation of the linear programming problem that facilitates the systematic execution of the simplex algorithm.

## Unit-2: Transportation and Assignment Problems

21. **What is a Transportation Problem?**  
    A transportation problem is a special linear programming problem that deals with the distribution of goods from multiple sources to multiple destinations with the objective of minimizing total transportation cost.

22. **Define Balanced Transportation Problem.**  
    A balanced transportation problem is one where the total supply equals the total demand.

23. **What is an Unbalanced Transportation Problem?**  
    An unbalanced transportation problem is one where the total supply is not equal to the total demand.

24. **What is the N.W. Corner Rule?**  
    The North-West Corner Rule is a method to find an initial basic feasible solution for a transportation problem by starting from the upper-left corner and allocating maximum possible amount.

25. **What is the Least Cost Method?**  
    The Least Cost Method is a technique to find an initial basic feasible solution for a transportation problem by allocating maximum possible amount to the cell with the lowest cost.

26. **Define Vogel's Approximation Method (VAM).**  
    VAM is a method to find an initial basic feasible solution for a transportation problem by considering the penalty costs, which are the differences between the two lowest costs in each row and column.

27. **What is an Assignment Problem?**  
    An assignment problem is a special case of transportation problem where n jobs are to be assigned to n machines with the objective of minimizing the total cost or maximizing the total profit.

28. **Explain the concept of the Hungarian Method.**  
    The Hungarian Method is an algorithm used to solve assignment problems by systematically reducing the cost matrix until an optimal assignment can be made.

29. **What is the Initial Basic Feasible Solution?**  
    An initial basic feasible solution is a starting feasible solution for transportation problems, obtained using methods like N.W. Corner Rule, Least Cost Method, or VAM.

30. **Define Optimality Condition in Transportation Problem.**  
    The optimality condition in a transportation problem is met when all opportunity costs (or evaluation indices) are non-negative for minimization problems or non-positive for maximization problems.

31. **What is the objective of solving an Assignment Problem?**  
    The objective of solving an assignment problem is to find the optimal assignment of jobs to machines that minimizes the total cost or maximizes the total profit.

32. **What is the difference between Transportation and Assignment Problems?**  
    In a transportation problem, multiple units can be shipped from a source to a destination, while in an assignment problem, exactly one job is assigned to one machine.

33. **Define Degeneracy in Transportation Problem.**  
    Degeneracy in a transportation problem occurs when the number of allocated cells is less than m+n-1, where m is the number of sources and n is the number of destinations.

34. **What is the role of the Cost Matrix in Assignment Problems?**  
    The Cost Matrix in assignment problems represents the costs associated with assigning each job to each machine, forming the basis for finding the optimal assignment.

35. **What does the Modifying Distribution (MODI) Method do?**  
    The MODI Method tests the optimality of the current basic feasible solution in a transportation problem and helps in finding the next improved solution.

36. **What is the significance of the Dummy Row/Column in T.P?**  
    A dummy row or column is added to balance an unbalanced transportation problem by introducing an artificial source or destination with zero supply/demand and zero costs.

37. **What is a Feasible Solution in Transportation Problem?**  
    A feasible solution in a transportation problem is an allocation pattern that satisfies all supply and demand constraints.

38. **What is Total Transportation Cost?**  
    Total Transportation Cost is the sum of the products of the unit transportation costs and the corresponding amounts transported across all routes.

39. **Define Minimization Problem in Transportation.**  
    A minimization problem in transportation aims to find the transportation plan that minimizes the total transportation cost while satisfying all supply and demand constraints.

40. **What is the advantage of the Hungarian Method?**  
    The advantage of the Hungarian Method is that it guarantees an optimal solution to the assignment problem in polynomial time complexity.

## Unit-3: Network Analysis

41. **What is Network Analysis?**  
    Network Analysis is a technique used to plan, schedule, and control complex projects by modeling them as networks of activities and events.

42. **Define Critical Path.**  
    The Critical Path is the longest path through a network diagram, representing the shortest possible time to complete the project.

43. **What is a Network Diagram?**  
    A Network Diagram is a graphical representation of project activities showing their sequence, dependencies, and durations.

44. **What is CPM?**  
    Critical Path Method (CPM) is a project management technique used to determine the critical path and the minimum time required to complete a project.

45. **Define PERT.**  
    Program Evaluation and Review Technique (PERT) is a method that uses probabilistic time estimates for activities to analyze the time required to complete a project.

46. **What is Float in CPM?**  
    Float is the amount of time an activity can be delayed without affecting the project completion time.

47. **What is Slack?**  
    Slack is the time difference between the earliest and latest start or finish times of an activity.

48. **What is Total Float?**  
    Total Float is the maximum amount of time an activity can be delayed without delaying the project completion time.

49. **Define Free Float.**  
    Free Float is the amount of time an activity can be delayed without affecting the earliest start time of its successor activities.

50. **What is Independent Float?**  
    Independent Float is the amount of time an activity can be delayed without affecting the latest finish time of its predecessor activities or the earliest start time of its successor activities.

51. **What is an Activity in Network Analysis?**  
    An Activity in network analysis is a task or job that consumes time and resources and has a definite beginning and end.

52. **What is an Event in Network Analysis?**  
    An Event in network analysis is a point in time marking the start or completion of one or more activities.

53. **What is the significance of the Critical Path?**  
    The Critical Path identifies the sequence of activities that must be completed on time to ensure the entire project is completed on schedule.

54. **Define Earliest Start Time.**  
    Earliest Start Time (EST) is the earliest time at which an activity can begin, considering all predecessor activities.

55. **What is Latest Finish Time?**  
    Latest Finish Time (LFT) is the latest time by which an activity must be completed without delaying the project.

56. **What is the importance of Float Analysis?**  
    Float Analysis helps in identifying the flexibility in scheduling activities and in allocating resources efficiently.

57. **What is the purpose of PERT in project management?**  
    The purpose of PERT is to handle uncertainty in project scheduling by using probabilistic time estimates for activities.

58. **What is a Dummy Activity?**  
    A Dummy Activity is a zero-duration activity used in network diagrams to show logical relationships between activities without consuming time or resources.

59. **What is a Predecessor Activity?**  
    A Predecessor Activity is an activity that must be completed before another activity can start.

60. **What is the difference between CPM and PERT?**  
    CPM uses deterministic time estimates for activities, while PERT uses probabilistic time estimates (optimistic, most likely, and pessimistic).

## Unit-4: Sequencing Problems and Game Theory

61. **What is a Sequencing Problem?**  
    A Sequencing Problem deals with determining the optimal order in which a set of jobs should be processed through a given set of machines.

62. **Define No Passing Rule.**  
    The No Passing Rule stipulates that jobs must follow the same sequence on all machines, meaning no job can pass another job in the sequence.

63. **What is a Saddle Point in Game Theory?**  
    A Saddle Point is a position in a payoff matrix where the minimum value in its row is equal to the maximum value in its column.

64. **What is a Zero-Sum Game?**  
    A Zero-Sum Game is a game where the total of the payoffs to all players is zero for each possible outcome.

65. **What is a Two-Person Zero-Sum Game?**  
    A Two-Person Zero-Sum Game is a game with two players where one player's gain is exactly balanced by the other player's loss.

66. **What is a Pure Strategy?**  
    A Pure Strategy is a decision rule that specifies a single action to be taken for each possible situation in a game.

67. **Define Mixed Strategy.**  
    A Mixed Strategy is a probability distribution over the possible pure strategies, allowing a player to randomly choose among different actions.

68. **What is a Payoff Matrix?**  
    A Payoff Matrix is a table that shows the outcomes (payoffs) for each possible combination of strategies chosen by the players.

69. **What is a Game Tree?**  
    A Game Tree is a graphical representation of a sequential game, showing the possible moves and countermoves of each player.

70. **What are Optimal Strategies?**  
    Optimal Strategies are the strategies that maximize a player's minimum payoff or minimize the maximum loss.

71. **What is a Saddle Point Theorem?**  
    The Saddle Point Theorem states that if a game has a saddle point, then the corresponding pure strategies form an optimal solution to the game.

72. **What is the Principle of Dominance?**  
    The Principle of Dominance states that a strategy is dominated if there exists another strategy that always gives a better payoff regardless of the opponent's choice.

73. **Define Minimax Criterion.**  
    The Minimax Criterion is a decision rule where a player chooses the strategy that minimizes the maximum possible loss.

74. **What is Maximin Criterion?**  
    The Maximin Criterion is a decision rule where a player chooses the strategy that maximizes the minimum possible gain.

75. **What is the significance of Sequencing in Operations Research?**  
    Sequencing in Operations Research helps in optimizing the order of jobs or tasks to minimize the total completion time, idle time, or waiting time.

76. **What are the types of Games in Game Theory?**  
    Types of Games include Zero-Sum Games, Non-Zero-Sum Games, Cooperative Games, Non-Cooperative Games, Simultaneous Games, and Sequential Games.

77. **What is a 2×2 Game?**  
    A 2×2 Game is a two-person game where each player has exactly two possible strategies.

78. **What does the term "Strategy" mean in Game Theory?**  
    In Game Theory, a Strategy is a complete plan of action that specifies what a player will do in every possible situation in a game.

79. **What is the significance of Sequencing Rules?**  
    Sequencing Rules provide guidelines for determining the order in which jobs should be processed to optimize specific performance criteria.

80. **Define Independent Float in Game Theory.**  
    Independent Float in Game Theory refers to the flexibility in timing that a player has for making decisions without affecting the optimal decisions of other players.
