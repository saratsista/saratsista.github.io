---
layout: post
title:  "Sorting Primitive Data Type Arrays in Java"
date:   2020-01-10 12:32:28 PST
categories: algorithms
---

### `Arrays#sort()` method in Java
In Java, primitive arrays can be sorted using `Arrays#sort()` method. Internally, this method uses Quick Sort to sort the arrays with primitive data types while it uses Merge Sort to sort the arrays with reference data types.

In competitive programming, we frequently need to sort the arrays with primitive data types. But one needs to be careful if they're using Java because Quick Sort is O(N^2) in the worst case and most online judges will have a test case to test this scenario.

The solution to overcome this problem is to **_shuffle the array randomly_** before using Quick Sort  

### Randomly Shuffling the Array
In Java, one can use `Random.java` to initialize and generate random numbers. But a simpler, more concise and probably faster way to achieve this is to use `Math#random()` method.

`Math#random()` returns a random `double` between `0.0` and `1.0`. In order to use this to generate a random value within a given range, we can do the following:

```java
/**
 * Let 'lo' and 'hi' represent the range.
**/
int range = (hi - lo) + 1;
int randomNumberInRange = ((int)Math.random() * range) + lo;
```
 
### Example

Problem - [Queries about less or equal elements](https://codeforces.com/contest/600/problem/B)

Implementation - [QueriesLessOrEqual.java](https://github.com/saratsista/competitive-programming/blob/master/src/codeforces/R600/QueriesLessOrEqual.java)
