# Leetcode-2894.-Divisible-and-Non-divisible-Sums-Difference
To find  Divisible and Non-divisible Sums Difference
# Description :
You are given positive integers n and m.

Define two integers as follows:

num1: The sum of all integers in the range [1, n] (both inclusive) that are not divisible by m.
num2: The sum of all integers in the range [1, n] (both inclusive) that are divisible by m.
Return the integer num1 - num2.

# Solution
Divisible numbers are those which if divided by some number will give the answer as 0 i.e : 4 % 2 ==0
Non Divisible numbers are those which if divided by some number will not give the answer as 0 i.e : 5 % 2 is not 0

We have 2 integers given as n and m .

Eg : if n=5 and m=1
Range =[1 to 5]
1%1 ==0
2%1 == 0
3%1 == 0
4%1 == 0
5%1 == 0

Divisible numbers = [1,2,3,4,5]
Non Divisible numbers = [0]
# Code
 C++
 class Solution {
public:
    int differenceOfSums(int n, int m) {
        int divisible=0;
        int nondivisible=0;
        for(int i=1;i<=n;i++){
            if(i%m==0){
                divisible+=i;
            }
            else{
                nondivisible+=i;
            }
        
        }
        return nondivisible-divisible;
    }
};

1. In this question we have to find all the numbers from range 1 to n which should be divided by m  .
2. Add all these numbers into a variable called divisible .
3. The numbers which are not divisible by m will be added into a separate variable named nondivisible.
4. After the loop ends subtract nondivisible and divisible .
5. Return the difference. 

