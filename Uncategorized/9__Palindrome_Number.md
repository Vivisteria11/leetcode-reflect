
### Problem: 9. Palindrome Number

ðŸ· Topic: Uncategorized

ðŸ¤– GPT Feedback:
Feedback:
This solution is mostly correct. However, there is a corner case where the input number is 0, and it's not handled correctly. When the input is 0, the function will return true, but a non-palindromic number (0) is considered a palindrome. This issue should be addressed.

ðŸ’» Your Code:
```cpp
class Solution {
public:
    bool isPalindrome(int x) {

        
        if(x < 0){
            return false;
        }

         long  orig =x;

        long val = 0;
        while(x!=0){
            long res = x % 10;
            val = val * 10 + res;
            x = x/10;


        }
        

       
        
        return orig == val;
    }
};
```
