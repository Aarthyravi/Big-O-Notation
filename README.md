# Big-O-Notation

## O(1) - Constant Time Examples:

    Algorithm 1:
Algorithm 1 prints hello once and it doesn't depend on n, so it will always run in constant time, so it is O(1).

print "hello";
Algorithm 2:
Algorithm 2 prints hello 3 times, however it does not depend on an input size. Even as n grows, this algorithm will always only print hello 3 times. That being said 3, is a constant, so this algorithm is also O(1).

print "hello";
print "hello";
print "hello";
O(log(n)) - Logarithmic Examples:

Algorithm 3 - This acts like "log_2"
Algorithm 3 demonstrates an algorithm that runs in log_2(n). Notice the post operation of the for loop multiples the current value of i by 2, so i goes from 1 to 2 to 4 to 8 to 16 to 32 ...

for(int i = 1; i <= n; i = i * 2)
  print "hello";
Algorithm 4 - This acts like "log_3"
Algorithm 4 demonstrates log_3. Notice i goes from 1 to 3 to 9 to 27...

for(int i = 1; i <= n; i = i * 3)
  print "hello";
Algorithm 5 - This acts like "log_1.02"
Algorithm 5 is important, as it helps show that as long as the number is greater than 1 and the result is repeatedly multiplied against itself, that you are looking at a logarithmic algorithm.

for(double i = 1; i < n; i = i * 1.02)
  print "hello";
O(n) - Linear Time Examples:

Algorithm 6
This algorithm is simple, which prints hello n times.

for(int i = 0; i < n; i++)
  print "hello";
Algorithm 7
This algorithm shows a variation, where it will print hello n/2 times. n/2 = 1/2 * n. We ignore the 1/2 constant and see that this algorithm is O(n).

for(int i = 0; i < n; i = i + 2)
  print "hello";
O(n*log(n)) - nlog(n) Examples:

Algorithm 8
Think of this as a combination of O(log(n)) and O(n). The nesting of the for loops help us obtain the O(n*log(n))

for(int i = 0; i < n; i++)
  for(int j = 1; j < n; j = j * 2)
    print "hello";
Algorithm 9
Algorithm 9 is like algorithm 8, but each of the loops has allowed variations, which still result in the final result being O(n*log(n))

for(int i = 0; i < n; i = i + 2)
  for(int j = 1; j < n; j = j * 3)
    print "hello";
O(n^2) - n squared Examples:

Algorithm 10
O(n^2) is obtained easily by nesting standard for loops.

for(int i = 0; i < n; i++)
  for(int j = 0; j < n; j++)
    print "hello";
Algorithm 11
Like algorithm 10, but with some variations.

for(int i = 0; i < n; i++)
  for(int j = 0; j < n; j = j + 2)
    print "hello";
O(n^3) - n cubed Examples:

Algorithm 12
This is like algorithm 10, but with 3 loops instead of 2.

for(int i = 0; i < n; i++)
  for(int j = 0; j < n; j++)
    for(int k = 0; k < n; k++)
      print "hello";
Algorithm 13
Like algorithm 12, but with some variations that still yield O(n^3).

for(int i = 0; i < n; i++)
  for(int j = 0; j < n + 5; j = j + 2)
    for(int k = 0; k < n; k = k + 3)
      print "hello";
