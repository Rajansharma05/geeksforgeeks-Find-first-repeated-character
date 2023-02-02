# geeksforgeeks-Find-first-repeated-character
**Given a string S. The task is to find the first repeated character in it. We need to find the character that occurs more than once and whose index of second occurrence is smallest. S contains only lowercase letters.**



class Solution 
{ 
    String firstRepChar(String s) 
    { 
         int[] hash = new int[26];
    for (int i = 0; i < s.length(); i++) {
        if (hash[s.charAt(i) - 'a'] == 1) {
            return Character.toString(s.charAt(i));
        }
        hash[s.charAt(i) - 'a']++;
    }
    return "-1";
    }
} 


________________________________________________________________________________________________________________________________________________________________________

**PYTHON**
def firstRepChar(s):
    hash = [0] * 26
    for i in range(len(s)):
        if hash[ord(s[i]) - ord('a')] == 1:
            return s[i]
        hash[ord(s[i]) - ord('a')] += 1
    return "-1"
