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