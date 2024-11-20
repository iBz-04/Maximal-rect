Problem Description
Given a binary matrix (matrix), find the area of the largest rectangle formed by 1s. The matrix consists of '0's and '1's.

Solution Approach
The solution uses a dynamic programming approach along with a helper function (largestRectangleArea) that computes the largest rectangle area in a histogram.

Helper Function (largestRectangleArea):

This function treats each row of the matrix as a histogram.
It uses a stack-based method to calculate the maximum area of a rectangle that can be formed with the heights of the histogram bars.


Main Function (maximalRectangle):

It initializes a result variable to store the maximum area found.
It processes each row of the matrix:
Converts the row into a histogram (count) representing the heights of bars made of consecutive 1s.
Calls largestRectangleArea with this histogram to get the largest rectangle area for that row.
Updates result with the maximum of the current result and the area obtained from largestRectangleArea.


Time Complexity
The time complexity of the maximalRectangle function is O(m * n), where m is the number of rows and n is the number of columns in the matrix. This complexity arises from the nested loops iterating through each element of the matrix and then computing the largest rectangle area using largestRectangleArea.
