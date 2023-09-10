# Find-the-Largest-Element-in-an-Array-using-Recursion-in-C

Find the Largest Element in an Array using Recursion in C
Given the length of the array “n” and the array itself “A”, Find the Largest Element in an Array using Recursion in C Language.

For instance,

Input: A = [1, 4, 3, -5, -4, 8, 6]
Output: 8
Largest Element in an Array using Recursion
Find the Largest Element in an Array using Recursion 
the objective of the program is to recursively traverse through the string while comparing the elements. If the element is larger than the previous one. update the largest variable until no other element is larger than it. To do so we can use either recursion or iteration. We’ll use iteration on this page, the link to solutions with other approaches is given at the end of the page. 

Lets try and understand using an example. an Array A = [ 10, 324, 45 ].  Declare a function with the base case as when n==1 we return the first character of the array. The recursive function returns the maximum of the last element of the array passed as an argument and the returned value from the recursion. The recursion process is shown in the image adjacent. When in the last block the base case is satisfied, first element of the array is returned. The output for the above example is 324. For the Example in the image, the output is 4.

Find the Largest Element in an Array using Recursion in C
Related Pages
Finding Number of times x digit occurs in a given input
 
Finding number of integers which has exactly x divisors
 
Smallest element in an array

Power of a Number

Prime Number

While loop in C
C Code
Run
#include <stdio.h>

int max(int a, int b)
{
    return a>b?a:b ;
}

int findMaxRec(int A[], int n)
{
    if (n == 1)
        return A[0];
    return max(A[n-1], findMaxRec(A, n-1));
}
int main()
{
    int arr[] = {10, 324, 45, 90, 9808};
    int n = sizeof(arr)/sizeof(arr[0]);
    printf("Largest in given array is %d", findMaxRec(arr, n));
    return 0;
}
Output
Largest in given array is 9808
Explanation

The objective of the code is to recursively parse through the array input while checking for the largest element in the array. To do so we call recursively and break down the string into tiny strings. 

The algorithm for the above C code is as follows,

 Include the Required Library.
Define max function which takes two integer variables and return the largest among the two.
Declare findMaxRec() function that takes the array and it’s length as arguments.
Set base case as n==1, if true return the first element of the array A.
else return the maximum value of the last element of the array A and the value returned by the recursive call of the function using max() function.
In the int main() function declare and initialize the variables and call the findMaxRec() function. 
Print the reult using printf() function.
The output for the above code is the largest element in the Array input i.e 9808.

Prime Course Trailer

Related Banners
Get PrepInsta Prime & get Access to all 200+ courses offered by PrepInsta in One Subscription

Get Prime
