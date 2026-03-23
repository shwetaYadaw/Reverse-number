# Number Reversal Program

## Overview
This C++ program reverses a given integer. 
It takes a number as input and outputs the number with its digits in reverse order.

## How It Works
- The program reads an integer `n`.
- It initializes a variable `rev` to store the reversed number.
- A loop runs until `n` becomes 0.
- In each iteration:
  - The last digit is extracted using `n % 10`.
  - This digit is added to the reversed number (`rev = rev * 10 + d`).
  - The last digit is removed from `n` using `n = n / 10`.
- Finally, the reversed number is printed.

## Input
- A single integer value.

## Output
- The reversed integer.

## Example

Input:
1234

Output:
4321

## Code

```cpp
#include<bits/stdc++.h>
using namespace std;

int main(){
    int n;
    cin >> n;

    int rev = 0;

    while(n){
        int d = n % 10;
        rev = rev * 10 + d;
        n /= 10;
    }

    cout << rev;
}
