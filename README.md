All pairs whose sum is equal to given number in C
Here, in this page we will discuss the program to find all pairs whose sum is equal to given number in C . We are given with an array and a value sum and we need to return the count of all the pairs whose sum is equal to given value of the sum.

All pairs on integer array whose sum is equal to given number in C
Algorithm:
A simple solution is to traverse each element and check if there’s another number in the array which can be added to it to give sum. 

Declare a variable say count = 0, that will count the required pairs.
Now, run a lop from i=0 to i=n-1, and check inside that loop whether there is a number which add up with the i-th number to give the value sum, if it is so then increment the value of count by 1.
After the complete of iteration print the value of the count.
Time and Space Complexities :
Time complexity : O(n^2)
Space Complexity : O(1)
Code in C
Run
#include<stdio.h> 

int getPairsCount(int arr[], int n, int sum)
{
  int count = 0; 

  // Consider all possible pairs and check their sums
  for (int i = 0; i < n; i++){
     for (int j = i + 1; j < n; j++){
        if (arr[i] + arr[j] == sum)
          count++;
     }
  }
  return count;
}

// Driver function to test the above function
int main()
{ 
   int arr[] ={10, 12, 10, 15, -1, 7, 6, 5, 4, 2, 1, 1, 1};
   int n = sizeof(arr)/sizeof(arr[0]);
   int sum=11;
   
   printf("Count of pairs is %d",getPairsCount(arr, n, sum));
   return 0;
}
Output :
Count of pairs is 9
