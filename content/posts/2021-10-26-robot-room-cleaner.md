---
author: "volyx"
title:  "489. Robot Room Cleaner"
date: "2021-10-26"
# description: "Sample article showcasing basic Markdown syntax and formatting for HTML elements."
tags:  ["leetcode", "hard", "dfs", "backtracking"]
categories: ["leetcode"]
# series: ["Themes Guide"]
# aliases: ["migrate-from-jekyl"]
# ShowToc: true
# TocOpen: true
# weight: 2
---

![489. Robot Room Cleaner](https://leetcode.com/problems/robot-room-cleaner/)

You are controlling a robot that is located somewhere in a room. The room is modeled as an m x n binary grid where 0 represents a wall and 1 represents an empty slot.

The robot starts at an unknown location in the root that is guaranteed to be empty, and you do not have access to the grid, but you can move the robot using the given API Robot.

You are tasked to use the robot to clean the entire room (i.e., clean every empty cell in the room). The robot with the four given APIs can move forward, turn left, or turn right. Each turn is 90 degrees.

When the robot tries to move into a wall cell, its bumper sensor detects the obstacle, and it stays on the current cell.

Design an algorithm to clean the entire room using the following APIs:

```java
interface Robot {
  // returns true if next cell is open and robot moves into the cell.
  // returns false if next cell is obstacle and robot stays on the current cell.
  boolean move();

  // Robot will stay on the same cell after calling turnLeft/turnRight.
  // Each turn will be 90 degrees.
  void turnLeft();
  void turnRight();

  // Clean the current cell.
  void clean();
}
```

Note that the initial direction of the robot will be facing up. You can assume all four edges of the grid are all surrounded by a wall.

Custom testing:

The input is only given to initialize the room and the robot's position internally. You must solve this problem "blindfolded". In other words, you must control the robot using only the four mentioned APIs without knowing the room layout and the initial robot's position.

```txt
Example 1:

Input: room = [[1,1,1,1,1,0,1,1],[1,1,1,1,1,0,1,1],[1,0,1,1,1,1,1,1],[0,0,0,1,0,0,0,0],[1,1,1,1,1,1,1,1]], row = 1, col = 3
Output: Robot cleaned all rooms.
Explanation: All grids in the room are marked by either 0 or 1.
0 means the cell is blocked, while 1 means the cell is accessible.
The robot initially starts at the position of row=1, col=3.
From the top left corner, its position is one row below and three columns right.
```

![ex1](/images/2021-10-26-robot-ex1.jpg)

```txt
Example 2:

Input: room = [[1]], row = 0, col = 0
Output: Robot cleaned all rooms.
```

Constraints:

- m == room.length
- n == room[i].length
- 1 <= m <= 100
- 1 <= n <= 200
- room[i][j] is either 0 or 1.
- 0 <= row < m
- 0 <= col < n
- room[row][col] == 1
- All the empty cells can be visited from the starting position.

## Solution

```java
/**
 * // This is the robot's control interface.
 * // You should not implement it, or speculate about its implementation
 * interface Robot {
 *     // Returns true if the cell in front is open and robot moves into the cell.
 *     // Returns false if the cell in front is blocked and robot stays in the current cell.
 *     public boolean move();
 *
 *     // Robot will stay in the same cell after calling turnLeft/turnRight.
 *     // Each turn will be 90 degrees.
 *     public void turnLeft();
 *     public void turnRight();
 *
 *     // Clean the current cell.
 *     public void clean();
 * }
 */


/*

0000
0000
00^0
0000

^>^>
^v^v
^v^v
<<<v

*/
class Solution {
    Set<String> visited = new HashSet<>();
    public void cleanRoom(Robot robot) {
        dfs(1, 0, 0, robot);
    }
    
    /*
    [
    [1,1,1,1,1,0,1,1],
    [1,1,1,1,1,0,1,1],
    [1,0,1,1,1,1,1,1],
    [0,0,0,1,0,0,0,0],
    [1,1,1,1,1,1,1,1]
    ]
    
    111
    111
    111
        
    11   
    11
    
    */
    void dfs(int d, int i, int j, Robot robot) {
        String key = i + "." + j;
        if (visited.contains(key)) {
            return;
        }
        
        // System.out.println(visited);
        
        visited.add(key);
        
        robot.clean();
            
        for (int dir = 0; dir < 4; dir++) {
            if (robot.move()) {
                int newDir = (dir + d) % 4;
                int x = getNext(newDir, i, j)[0];
                int y = getNext(newDir, i, j)[1];
                dfs(newDir, x, y, robot);
                goBack(robot);
            }
            robot.turnRight();
        } 
    }
    
    public void goBack(Robot robot) {
        robot.turnRight();
        robot.turnRight();
        robot.move();
        robot.turnRight();
        robot.turnRight();
    }
    
    int[] getNext(int dir, int x, int y) {
        if (dir == 0) {
            return new int[] {x + 1, y};
        } else if (dir == 1) {
            return new int[] {x, y + 1};
        } else if (dir == 2) {
             return new int[] {x - 1, y};
        } else if (dir == 3) {
            return new int[] {x, y - 1};
        }
        throw new IllegalStateException();
    }
}
 ```
