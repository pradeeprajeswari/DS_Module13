# Ex2 Conversion of the infix expression into postfix expression
## DATE:20\02\2025
## AIM:
To write a C program to convert the infix expression into postfix form using stack by following the operator precedence and associative rule.

## Algorithm
1. Scan left to right:If operand → print.
2. If '(' → push to stack.
3. If ')' → pop and print until '('.
4. If operator → Pop and print operators of higher/equal priority, then push current operator.
5. After scanning → pop and print all stack elements.

## Program:
```
/*
Program to convert the infix expression into postfix expression
Developed by: PRADEEP E
RegisterNumber:  212223230149
*/
```
```
#include<stdio.h>
#include<ctype.h>

char stack[100];
int top = -1;

void push(char x)
{
   stack[++top]=x;
}

char pop()
{
    if(top==-1)
   return -1;
   else
   return stack[top--];
}
int priority(char x)
{
    if(x=='(') return 0;
    if(x=='&' || x=='|') return 1;
    if(x=='+' || x=='-') return 2;
    if(x=='*' || x=='/' || x=='%') return 3;
    if(x=='^') return 4;
    return 0;
} 
char IntoPost(char *exp)
{
    
    char *e,x;
    e=exp;
    while(*e != '\0'){
        if(isalnum(*e)){
            printf("%c ",*e);
        }
        else if(*e=='('){
            push(*e);
        }
        else if(*e==')'){
            while((x=pop()) != '('){
                printf("%c ",x);
            }
        }
        else{
            while(priority(stack[top]) >= priority(*e))
                printf("%c ",pop());
            push(*e);
        }
        e++;
    }
    while(top != -1)
    {
       printf("%c ",pop());
    }return 0;
}


int main()
{
    char exp[100]="3%2+4*(A&B)";
    IntoPost(exp);
    return 1;
}


```

## Output:

![Screenshot 2025-04-28 102252](https://github.com/user-attachments/assets/f469196c-c3cb-49b8-a286-ed8061622617)


## Result:
Thus, the C program to convert the infix expression into postfix form using stack by following the operator precedence and associative rule is implemented successfully.
