#include <iomanip>
#include "windows.h"
#include <iostream>
using namespace std;

int main()
{
    int k=5;
    const int n = 5;
    int A[n] = { 1,4,8,-23,6 };
    
    for (int i = 0; i < n; i++)
        cin >> A[i];
    for (int i = 0; i < n; i++)
        cout << setw(5) << A[i];
    int min = 0;
    for (int i = 1; i < n; i++)
        if (A[i] <A[min]) min = i;
    cout << endl << "min=" <<setw(1)<<A[min] <<";"<< "index = "<<min;
    int max = 0;
    for (int i = 1; i < n; i++)
        if (A[i] > A[max]) max = i;
    cout << endl << "max=" << setw(1) << A[max] << ";" << "index = " << max;
    int sum = 0;
    for (int i = 0; i < n; i++)
        if ((A[i] % k)==0) {
            sum += A[i] ;
        }
    cout << "\nSum=" << sum;
}