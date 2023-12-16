# LeetCode Challenge D2

## [](https://github.com/ashi-bandara/LeetCode-Problem657-Robot_Return_to_Origin#overview)Overview

Welcome to my LeetCode solution repository! This project addresses the coding challenge presented by  [610. Triangle Judgement](https://leetcode.com/problems/triangle-judgement/description/). Below, you'll find details about the problem, my approach to solving it, and the implemented solution.

## [](https://github.com/ashi-bandara/LeetCode-Problem657-Robot_Return_to_Origin#problem-statement)Problem Statement

The "Triangle" table has columns `x`, `y`, and `z`, representing line segment lengths. For each set of segments, the goal was determine if they form a valid triangle. The result table should include the original segments along with a column indicating validity with a simple `Yes` or `No`.

**Example**

> **Input:** 
Triangle table:

| x  | y  | z  |
|----|----|----|
| 13 | 15 | 30 |
| 10 | 20 | 15 |

> **Output:**

| x  | y  | z  | triangle |
|----|----|----|----------|
| 13 | 15 | 30 | No       |
| 10 | 20 | 15 | Yes      |

>  **Explanation**:
> 
>  The SQL query utilizes the triangle inequality theorem by checking if the sum of any two sides of a triangle is greater than the length of the third side. For example, in the first row, `13` + `15` is less than `30`, indicating that the given lengths cannot form a valid triangle. On the other hand, in the second row, `10` + `20` is greater than `15`, `10` + `15` is greater than `20`, and `20` + `15` is greater than `10`, satisfying the conditions for a valid triangle, hence marked as `Yes` in the `triangle` column.

**Language Used**
> 
> MySQL

**Difficulty**

> Easy

## Solution Overview

The SQL solution employs a `CASE` statement to determine the validity of triangles based on the triangle inequality theorem. By checking if the sum of any two sides is greater than the length of the third side, the query populates the `triangle` column with `Yes` for valid triangles and `No` for invalid ones. This ensures that each row accurately reflects whether the provided line segment lengths can form a triangle or not.
