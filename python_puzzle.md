## Python puzzle notes

### set
set() has unique values (no duplicates allowed).

set() elements cannot be accessed using index, but only with loop.

set() elements are arranged in random order (unordered).

set() can have elements of different types


### list
list() can have duplicates

list() can be accessed using index and also with loop

list() has elements in order



## Trick 1

get missing number from a list(1..100)

***Technique***: convert list() to set() as subtraction of set is possible and is much easier to perform, which can give the missing number

e.g. 50 is removed from the list. list now has 1..98 only (#98 elements)

```
lst = list(range(1,100))   # 1..99  means index 0 .. 98
lst.remove(50)             # 98 elements remain


set A = set(lst)  # 1....99 without 50 means index 0..97

# lst[len(lst) - 1] = lst[98-1] = lst[97] = 99

set B = set(range(1, lst[len(lst)- 1]))   # 1...98  contains 50 with index 0..97


Now perform set B - set A will give an element in set B which is not present in set A which is the missing number
```



