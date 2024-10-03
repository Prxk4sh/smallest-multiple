# smallest-multiple
 is the smallest number that can be divided by each of the numbers from  to  without any remainder.
What is the smallest positive number that is evenly divisible(divisible with no remainder) by all of the numbers from  to ?

Input Format

First line contains  that denotes the number of test cases. This is followed by  lines, each containing an integer, .

Constraints

Output Format

Print the required answer for each test case.

Sample Input 0

2
3
10
Sample Output 0

6
2520
Explanation 0

You can check  is divisible by each of , giving quotient of  respectively.
You can check  is divisible by each of  giving quotient of  respectively.
------------------------------------------------------------------------------------
import math
import functools


def gcd(*numbers):
    """ greatest common divisor """
    return functools.reduce(math.gcd, numbers)


def lcm(*numbers):
    """ least common multiple """
    return functools.reduce(lambda a, b: (a * b) // gcd(a, b), numbers, 1)

for _ in range(int(input())):
    n = int(input())
    print(lcm(*range(1, n + 1)))
