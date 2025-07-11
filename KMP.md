# How to Calculate Next
Next[i] means the index after the longest common prefix and affix of the first i numbers.
It means where to look after a mismatch happens.

To calculate the next array, use two indexes, i and j.   
I represents the index of the last character of the affix.   
J represents the index of the last character of the prefix.   
Initially, i = 1, j = 0, next[0] = 0.   
In each for loop, i increases by one.
We compare the new i with j to see if they match.
Note that j is increased for the next cycle in the previous cycle, so we don't need to increase j.
If they match, we increase j by 1 and set next[i] = j because j is always the index to compare when a mismatch happens, so it is the character after the common prefix and affix.
If they don't match, we want to know if there is a common prefix and affix from 0 to i - 1. If there is, we can utilize that to try to find a new common prefix and affix:
```C++
while (j > 0 && needle[i] != needle[j]) {
    j = next[j - 1];
}
```
Note that we can directly use next[j - 1] because it already represents the character after the common prefix and affix, so we can compare it directly with the new character needle[i].
# How to use next to find needle in haystack
No need to back in haystack, only use next array to back in needle.
```C++
for (int i = 0; i < haystack.size(); i++) {
    while(j > 0 && haystack[i] != needle[j]) {
        j = next[j - 1];
    }
    if (haystack[i] == needle[j]) {
        j++;
    }
    if (j == needle.size() ) {
        return (i - needle.size() + 1);
    }
}
```