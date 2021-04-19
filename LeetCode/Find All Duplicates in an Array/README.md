# 328. Odd Even Linked List

Given an array of integers, 1 ≤ a[i] ≤ n (n = size of array), some elements appear twice and others appear once.

Find all the elements that appear twice in this array.

Could you do it without extra space and in O(n) runtime?

## Example:

```
Input:
[4,3,2,7,8,2,3,1]

Output:
[2,3]
```
const findDupes = (nums) => {
    const res = [];
 
    for(let i = 0; i < nums.length; i ++) {
        for (var j = i + 1; j < nums.length; j++) {
         if (nums[i] == nums[j]) {
             res.push(nums[i]);
             res.push(nums[j]);
         }
        }
     }
     return res;
 };
