
### Problem: 33. Search in Rotated Sorted Array

🏷 Topic: Search

🤖 LLM Feedback:
Feedback:
Your solution correctly identifies the rotated index in the rotated sorted array. However, it's not efficient for larger arrays.

💻 Your Code:
```cpp
class Solution {
public:
    int search(vector<int>& nums, int target) {
        for(int i =0;i<nums.size();i++){
            if(target ==nums[i]){
                return i;
            }
        }

        return -1;
        
    }
};
```
