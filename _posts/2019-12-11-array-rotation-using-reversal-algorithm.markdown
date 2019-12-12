### Input
Given an input array and the start index (l) and end index (r) within the array, we would want to rotate the subarray [l..r] by K rotations.

### Algorithm

{% highlight git %}

Lets assume that K divides the subarray [l..r] into two parts A[l..K-1] and B[K..r]. 
Perform the following steps in order as given:

1. Reverse the subarray [l..r]
2. Reverse the B part of the subarray [l+K..r]
3. Reverse the A part of the subarray [l, l+K-1];

{% endhighlight %}

The above 3 steps, when performed in order, yields the subarray that's rotated K times.

### Example

Problem - [Queries On String](https://codeforces.com/contest/598/problem/B)

Implementation - [QueriesOnString.java](https://github.com/saratsista/competitive-programming/blob/master/src/codeforces/QueriesOnString.java)