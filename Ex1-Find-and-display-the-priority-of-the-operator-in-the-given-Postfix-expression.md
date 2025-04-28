# EX 1 Display operator precedence in the infix expression.
## DATE:24/02/2025
## AIM:
To write a C program to find and display the priority of the operator in the given Postfix expression

## Algorithm
1. Start and define a function pri(x) to return a priority number based on the operator (&, |, +, -, *, /, %, ^).

2. Initialize the expression exp = "K%L-M*N+(O^P)" and set counters i, j.

3. Loop through each character of exp:

4. If priority (j) is not -1:

5. Print the operator and its corresponding priority description (Lowest, Second Lowest, Second Highest, Highest) using a switch case. 

## Program:
```
/*
Program to find and display the priority of the operator in the given Postfix expression
Developed by: PRADEEP E
RegisterNumber:  212223230149

#include <stdio.h>
#include <string.h>
int pri(char x){
    if (x=='&' || x=='|')
        return 1;
    else if(x=='+' || x=='-')
        return 2;
    else  if(x=='*' || x=='/' || x=='%')
        return 3;
    else if(x=='^')
        return 4;
    else
        return -1;
}
int main(){
    char exp[]="K%L-M*N+(O^P)";
    int i,j;
    for(i=0;exp[i]!= '\0';i++){
        j=pri(exp[i]);
        if(j!=-1)
            printf("%c  ---->", exp[i]);
        switch(j){
            case 1: printf(" Lowest Priority\n");break;
            case 2: printf(" Second Lowest Priority\n");break;
            case 3: printf(" Second Highest Priority\n");break;
            case 4: printf(" Highest Priority");break;
        }
    }
}
*/
```

## Output:

![Screenshot 2025-04-28 101125](https://github.com/user-attachments/assets/f7fea4f9-6f4c-411e-97a1-188847d43a8a)


## Result:
Thus the C program to find and display the priority of the operator in the given Postfix expression is implemented successfully
