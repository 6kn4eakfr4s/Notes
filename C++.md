Create a pair for map:
```C++
pair<int, int>(a, b);
```
Find values in map:
```C++
auto it = map.find(key);
```
Find value from itrator:
```C++
a = it->second;
```
Using [] to access map:
```C++
int a = map[key];
//It will insert a new element with a default value if the key doesn't exist
```
Increase a value in map:
```C++
map[key] += value;
```
Create a vector from values:
```C++
{a, b};
```
Swap two variables:
```C++
swap(a, b);
```
Swaping using XOR:
```C++
int x = 10, y = 20;
x ^= y;  // x = 10 ^ 20
y ^= x;  // y = 20 ^ (10 ^ 20) = 10
x ^= y;  // x = (10 ^ 20) ^ 10 = 20
// Now x=20, y=10
```
Removing a character in string:
```C++
string.erase(start, num)
//Removes the next num characters starting at index start
```
Reversing a string:
```C++
reverse(str.begin(), str.end());
```