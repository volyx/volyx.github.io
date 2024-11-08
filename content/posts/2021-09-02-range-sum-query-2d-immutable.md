---
author: "volyx"
title:  "304. Range Sum Query 2D - Immutable"
date: "2021-09-02"
# description: "Sample article showcasing basic Markdown syntax and formatting for HTML elements."
tags:  ["leetcode", "medium", "matrix"]
categories: ["leetcode"]
# series: ["Themes Guide"]
# aliases: ["migrate-from-jekyl"]
# ShowToc: true
# TocOpen: true
# weight: 2
---

[304. Range Sum Query 2D - Immutable](https://leetcode.com/problems/range-sum-query-2d-immutable/)

Given a 2D matrix matrix, handle multiple queries of the following type:

- Calculate the sum of the elements of matrix inside the rectangle defined by its upper left corner (row1, col1) and lower right corner (row2, col2).

Implement the NumMatrix class:

- NumMatrix(int[][] matrix) Initializes the object with the integer matrix matrix.
- int sumRegion(int row1, int col1, int row2, int col2) Returns the sum of the elements of matrix inside the rectangle defined by its upper left corner (row1, col1) and lower right corner (row2, col2).

```txt
Example 1:

Input
["NumMatrix", "sumRegion", "sumRegion", "sumRegion"]
[[[[3, 0, 1, 4, 2], [5, 6, 3, 2, 1], [1, 2, 0, 1, 5], [4, 1, 0, 1, 7], [1, 0, 3, 0, 5]]], [2, 1, 4, 3], [1, 1, 2, 2], [1, 2, 2, 4]]
Output
[null, 8, 11, 12]

Explanation
NumMatrix numMatrix = new NumMatrix([[3, 0, 1, 4, 2], [5, 6, 3, 2, 1], [1, 2, 0, 1, 5], [4, 1, 0, 1, 7], [1, 0, 3, 0, 5]]);
numMatrix.sumRegion(2, 1, 4, 3); // return 8 (i.e sum of the red rectangle)
numMatrix.sumRegion(1, 1, 2, 2); // return 11 (i.e sum of the green rectangle)
numMatrix.sumRegion(1, 2, 2, 4); // return 12 (i.e sum of the blue rectangle)
```

![ex1](/images/2021-09-01-matrix-ex1.jpg)

Constraints:

- m == matrix.length
- n == matrix[i].length
- 1 <= m, n <= 200
- -10^5 <= matrix[i][j] <= 10^5
- 0 <= row1 <= row2 < m
- 0 <= col1 <= col2 < n
- At most 10^4 calls will be made to sumRegion.

## Solution

```java
class NumMatrix {
    
    int[][] prefix;
    int n;
    int m;

    public NumMatrix(int[][] matrix) {
       this.n = matrix.length;
       this.m = matrix[0].length; 
       this.prefix = new int[n][m];
       
       for (int i = 0; i < n; i++) {
           for (int j = 0; j < m; j++) {
               int sum = 0;
               if (i > 0 && j > 0) {
                   sum += matrix[i][j];
                   sum += prefix[i - 1][j];
                   sum += prefix[i][j - 1];
                   sum -= prefix[i - 1][j - 1];
               } else if (i > 0) {
                   sum += matrix[i][j];
                   sum += prefix[i - 1][j];
               } else if (j > 0) {
                   sum += matrix[i][j];
                   sum += prefix[i][j - 1];
               } else {
                   sum = matrix[i][j];
               }
               prefix[i][j] = sum;
           }
       }  
    }
    
    public int sumRegion(int row1, int col1, int row2, int col2) {
        int big = prefix[row2][col2];
        
        if (row1 > 0) {
            big -= prefix[row1 - 1][col2];
        } 
        if (col1 > 0) {
            big -= prefix[row2][col1 - 1];
        } 
        
        if (row1 > 0 && col1 > 0) {
            big += prefix[row1 - 1][col1 - 1];
        }
        return big;
    }
}

/**
 * Your NumMatrix object will be instantiated and called as such:
 * NumMatrix obj = new NumMatrix(matrix);
 * int param_1 = obj.sumRegion(row1,col1,row2,col2);
 */
```
