# Travelling-Salesman-Problem-using-Genetic-Algorithm

Here's the Genetic Algorithm for the Traveling Salesman Problem (TSP) expressed in mathematical notation:

1. **Objective**: Minimize the total distance of a route that visits each city exactly once and returns to the starting city.

```math
\text{Minimize } D(\text{route}) = \sum_{i=1}^{N} \text{dist}(\text{route}_i, \text{route}_{i+1}) + \text{dist}(\text{route}_N, \text{route}_1)
```

where:
- \(D(\text{route})\) is the total distance of the route.
- \(N\) is the number of cities.
- \(\text{dist}(A, B)\) represents the distance between cities \(A\) and \(B\).

2. **Initialize Population**: Generate an initial population of random routes:
```math
P(0) = \{\text{route}_1, \text{route}_2, \dots, \text{route}_{\text{population\_size}}\}
```

3. **Fitness Calculation**: For each generation \(g\), calculate the fitness of each route \(R\) in the population:
```math
\text{fitness}(R) = \frac{1}{D(R)}
```

4. **Selection**: Select \(k\) routes with the highest fitness values from the current population \(P(g)\) using a selection method such as Roulette Wheel Selection.

5. **Crossover**: Generate offspring by combining pairs of selected parents to produce a new population. Given parent routes \(A\) and \(B\):
```math
\text{offspring} = \text{crossover}(A, B)
```

6. **Mutation**: Introduce mutations with probability \(p\) by randomly swapping cities within routes to maintain diversity:
```math
\text{mutate}(R) = R' \text{ with probability } p
```

7. **Next Generation**: Replace the current population \(P(g)\) with the offspring population to form \(P(g+1)\).

8. **Termination**: After a set number of generations, select the route with the minimum total distance as the optimal solution:
```math
\text{Best Route} = \arg\min_{R \in P} D(R)
```

where \(P\) is the set of best routes across all generations.
