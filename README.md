 Committing to the #TeachersDay Challenge — a part of #MissionDrGViswanathan

🔹 Problem-solving consistency
🔹 Video explanations for better understanding
🔹 Interview-style practice

Every line of code takes me one step closer to the dream.

### DAY 1
YOUTUBE LINK : https://youtu.be/Uwggx3YVTo0

✅ Problem 1: Two Sum (Find indices of two numbers that add up to target):

Loop through the array with two nested for loops.

For every pair of indices i and j, check if nums[i] + nums[j] == target.

If a pair is found, return their indices in an array: return new int[] {i, j}.

If no such pair is found, return an empty array.

Time complexity is O(n²) — brute-force but works correctly.
BEGINNER : <img width="1919" height="873" alt="Screenshot 2025-07-25 212736" src="https://github.com/user-attachments/assets/4bf068ba-c4c7-4262-9bf2-bb4d21347af3" />


✅ Problem 2: Count Numbers with Even Number of Digits:

Loop through each number in the input array.

Count how many digits the number has using either Math.log10(num) + 1 or by converting to a string.

If the digit count is even (i.e., divisible by 2), increment the counter.

After the loop, return the count of numbers that had even digits.

Time complexity is O(n) — efficient and simple.
ADVANCED : <img width="1919" height="871" alt="Screenshot 2025-07-25 212748" src="https://github.com/user-attachments/assets/894a45ea-ad7d-4103-94f1-9ea0400f0f85" />

DAY 02 :
1. FizzBuzz
   <img width="1919" height="870" alt="Screenshot 2025-07-26 210436" src="https://github.com/user-attachments/assets/281d0abf-f55f-414a-979c-4c4b71873fa2" />

This is a classic number substitution problem:

It loops from 1 to n.

If the number is divisible by both 3 and 5, it adds "FizzBuzz" to the result list.

If divisible only by 3, it adds "Fizz".

If divisible only by 5, it adds "Buzz".

Otherwise, it just adds the number itself as a string.

The results are stored in a list and returned.

2. Check if Two Binary Trees are Same
   <img width="1919" height="862" alt="Screenshot 2025-07-26 222301" src="https://github.com/user-attachments/assets/ab0696c7-4e2d-451a-9613-a90628c3695f" />

This function compares two binary trees recursively:

If both current nodes are null, it returns true (identical at this point).

If only one is null or their values don’t match, it returns false.

It then recursively checks the left and right child nodes of both trees.

If all corresponding nodes match, the trees are considered the same.

3. Group Anagrams (Without HashMap)
   <img width="1919" height="870" alt="Screenshot 2025-07-26 222029" src="https://github.com/user-attachments/assets/2481399e-c217-474d-80e8-c2c78c58a2c9" />

This groups strings that are anagrams:

Each word is sorted alphabetically to form a key pattern.

A list seen stores these sorted patterns.

For each word, it checks if its sorted pattern already exists in seen.

If it does, the word is added to the existing group in the result list.

If not, a new group is started and added to the result.

This avoids using HashMaps and keeps the logic simple for beginners.

4. Remove Elements from Linked List
<img width="1919" height="873" alt="image" src="https://github.com/user-attachments/assets/891575d9-8739-4764-8b1c-9247bcc45e78" />

This removes all nodes with a specific value from a linked list:

A dummy node is created at the beginning to simplify edge cases like deleting the head.

A pointer cur traverses the list.

If the next node's value matches the given value, it's skipped (cur.next = cur.next.next).

If not, it moves forward.

Finally, it returns dummy.next which points to the possibly new head of the list.

###DAY 03
1. Valid Palindrome
Problem:
Check if a given string is a palindrome, considering only alphanumeric characters and ignoring cases.

Approach:

Use two pointers (start from beginning and last from end).

Skip non-alphanumeric characters.

Compare lowercase versions of characters.

If at any point they differ, return false.

If loop completes, return true.

Why it works:
Efficient two-pointer technique that avoids extra space and handles edge cases like symbols and spaces.

2. Invert Binary Tree
Problem:
Invert (mirror) a binary tree by swapping left and right child nodes recursively.

Approach:

Base case: if the root is null, return null.

Swap left and right children of the current node.

Recursively call the same function on left and right children.

Return the modified root.

Why it works:
Simple and elegant recursive approach that traverses the tree top-down and inverts each subtree.

3. Top K Frequent Elements
Problem:
Given an integer array, return the k most frequent elements.

Approach:

Count the frequency of each number using a dictionary hs.

Use another dictionary frq to map frequency to a list of elements with that frequency.

Loop from highest possible frequency down to 1.

Collect elements in order until k elements are gathered.

Why it works:
This approach groups elements by frequency and then picks from highest to lowest — efficiently bypasses the need for sorting the entire array.

### DAY 04
1. Min Stack
Problem:
Design a stack that supports push, pop, top, and retrieving the minimum element in constant time.

Approach:

Instead of storing only values, store a pair: (value, current_min).

push(x): push (x, min(x, current_min)).

pop(): remove top element.

top(): return the top value.

getMin(): return the second item of the top pair.

Why it works:
By storing the minimum value along with every element, you can access the min in O(1) time — no need to traverse.

2. Best Time to Buy and Sell Stock
Problem:
Find the maximum profit from a list of stock prices — buy once and sell once.

Approach:

Use two pointers: left (buy) and right (sell).

If selling price is greater, calculate profit and update max_profit.

If not, move the left pointer to the right (start new buy).

Repeat until the end.

Why it works:
You check the lowest buying point and highest selling point in one pass, with O(n) time.

3. Two Sum
Problem:
Find two indices in the array whose elements add up to the target.

Approach:

Use a nested loop to try all combinations of two elements.

If any pair adds up to the target, return their indices.

Why it works:
Brute-force approach, simple to understand for beginners. Though it has O(n²) time, it’s clear and easy to debug.

### DAY 05
1. Roman to Integer
   
Explanation:

Roman numerals follow subtraction rules when a smaller numeral appears before a larger one (e.g., IV = 4).

We iterate through the string:

If a smaller numeral precedes a larger one, subtract it.

Otherwise, add the value.

This allows proper handling of both additive and subtractive cases in a single pass.

2. 56. Merge Intervals

Explanation:

First, sort all intervals by their starting point.

Iterate through them:

If the current interval overlaps with the last one in out, merge them.

If not, append the current interval as is.

This is efficient and ensures all overlapping intervals are combined into one.

3. 104. Maximum Depth of Binary Tree

Explanation:

We perform a Depth-First Search (DFS), tracking the depth as we go down each branch.

The base case returns the current depth if the node is null.

For each node, we compute the max depth of its left and right children recursively.

The final answer is the maximum depth encountered from root to leaf.

### DAY 06:
1. Valid Parentheses
   This algorithm checks if a string of brackets is valid by using a stack data structure.
It works by pushing opening brackets onto the stack, and for each closing bracket, it checks if the top of the stack has a corresponding opening bracket.
If at any point there's a mismatch or the stack is empty when a closing bracket appears, the string is invalid.
At the end, the stack should be empty for the string to be considered valid, meaning all opened brackets were properly closed in order.
2. Maximum Subarray (Kadane's Algorithm)
   Explanation:
This solution uses Kadane’s algorithm to find the subarray with the largest sum.
It iterates through the list and updates each element by adding the previous value if it’s positive, meaning it's beneficial to extend the current subarray.
This way, nums[i] holds the maximum sum subarray ending at index i.
Finally, the maximum of all such subarrays is returned, ensuring the global maximum is captured.
3. Reverse Linked List
   Explanation:
This function reverses a singly linked list using an iterative approach.
It maintains a prev pointer initialized to None and iteratively moves through the list, reversing the direction of each node's next pointer to point to the previous node.
At the end of the loop, the prev pointer will be at the new head of the reversed list.
This approach runs in O(n) time with O(1) space, making it efficient and in-place.
