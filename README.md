# cooding-ninja-problem-

#include<bits/stdc++.h>
using namespace std;
 
// Function to check if the number
// is pair-sum of sum of first X
// natural numbers
void checkSumOfNatural(int n)
{
    int i = 1;
    bool flag = false;
     
    // Check if the given number
    // is sum of pair of special numbers
    while (i * (i + 1) < n * 2)
    {
         
        // X is the sum of first
        // i natural numbers
        int X = i * (i + 1);
         
        // t = 2 * Y
        int t = n * 2 - X;
        int k = sqrt(t);
         
        // Condition to check if
        // Y is a special number
        if (k * (k + 1) == t)
        {
            flag = true;
            break;
        }
        i += 1;
    }
     
    if (flag)
        cout << "YES";
    else
        cout << "NO";
}
 
// Driver Code
int main()
{
    int n;
    cin >> n;
    checkSumOfNatural(n);
 
    return 0;
}
