
### Problem: 13. Roman to Integer

🏷 Topic: DP

🤖 LLM Feedback:
Your solution to "Roman to Integer" correctly converts Roman numerals to integers. It uses a greedy approach by iterating from left to right through the roman numeral string, and it maintains a dictionary to map Roman numerals to their corresponding integer values. However, it has room for improvement in terms of efficiency.

The current solution has a time complexity of O(n), where n is the length of the Roman numeral string. This is because it needs to iterate through the string once to convert it to an integer. This is the most efficient time complexity possible for this problem, as it needs to examine each character in the input at least once.

One possible improvement is to sort the Roman numeral string before processing it. This could potentially reduce the time complexity to O(1), but it would also increase the space complexity to O(n), as it would need a new sorted string. However, since the space complexity is already O(n) in the current solution (due to the use of a dictionary), this improvement would not significantly reduce the overall complexity.

💻 Your Code:
```cpp
class Solution {
public:
    int romanToInt(string s) {
       
         unordered_map<char, int> value = {
            {'I', 1}, {'V', 5}, {'X', 10}, {'L', 50},
            {'C', 100}, {'D', 500}, {'M', 1000}
        };

        int result  =0 ;


        int n = s.size();

        for(int i  =0;i<n;i++){
            if( i < n-1 && value[s[i]] < value[s[i+1]]){ 
                result = result - value[s[i]];



            }else{

            result = result +value[s[i]];
        }
        }



return result;
        
    }
};
```
