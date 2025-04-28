# EX3 Implementation of Tower of Hanoi
## DATE:24/02/2025
## AIM:
To write a C program to implement Tower of Hanoi

## Algorithm
1. If n > 0,
2. Move n-1 disks from source x to auxiliary z using destination y.
3. Move the largest disk (nth disk) from source x to destination y.
4. Move n-1 disks from auxiliary z to destination y using source x.

## Program:
```
/*
Program to implement Tower of Hanoi
Developed by: PRADEEP E 
RegisterNumber:  212223230149
*/
```
```
#include<stdio.h>
void TOH(int n,char x,char y,char z)
{
   if(n>0){
       TOH(n-1,x,z,y);
       printf("%c to %c\n",x,y);
       TOH(n-1,z,y,x);
   }
}

```

## Output:

![Screenshot 2025-04-28 102734](https://github.com/user-attachments/assets/32b493a7-566c-4466-8ec8-34c105adc34a)


## Result:
Thus, the C program to implement Tower of Hanoi using recursion is implemented successfully.
