Que. Given an array arr[] denoting heights of N towers and a positive integer K, you have to modify the height of each tower either by increasing or decreasing them by K only once. After modifying, height should be a non-negative integer. 
Find out what could be the possible minimum difference of the height of shortest and longest towers after you have modified each tower.

Example 1:

Input:
K = 2, N = 4
Arr[] = {1, 5, 8, 10}
Output: 5
Explanation: The array can be modified as 
{3, 3, 6, 8}. The difference between 
the largest and the smallest is 8-3 = 5.

Example 2:

Input:
K = 3, N = 5
Arr[] = {3, 9, 12, 16, 20}
Output: 11
Explanation: The array can be modified as
{6, 12, 9, 13, 17}. The difference between 
the largest and the smallest is 17-6 = 11. 

Algorithm: 

	1. Sort the given array.
	2. Set the ans to the difference between the least element of the array and the first element of an array.
	3. Set minimum to the first element of array + k and maximum to last element - k of the array.
	4. Traverse the array from i=1 to i<n-1(one less than the length of the array).
	  1. Set diff to arr[i]-k.
	  2. Set sum to arr[i]+k.
	  3. Check if the diff is greater than equal to minimum or sum is less than or equal to maximum.
		1. If true, then continue and skip this traversal.
	  4. Check if maximum-diff is less than or equal to sum-minimum.
		1. If true, then update minimum to diff.
	  5. Else set the maximum to sum.
	5. Return the minimum between the ans and maximum-minimum.
