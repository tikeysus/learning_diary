
# Switch Statements in C

## Purpose 

A switch statement transfers control to an operation within its body based on the value of an expression. This expression or variable must have an assigned and unambiguous at the time of compilation. 

## Keywords

* Case 
	- Used to compare the value of the expression to the conditional within the case body. 
	- Analogous to an "if" in basic conditional branches. 

* Default 
	- If no cases match the value of the expression, the default statement is executed. 
	- Can be placed anywhere in the body of the switch statement, considered good practice to write it at the end. 
	- Analogous to an "else" statement in conditional branching. 

* Break 
	- Important keyword to control execution. Must be written after each individual case. 
	- Without a break statement at the end of each case, follow through will happen and every single case after the matching one will execute. 

## Example 

```
switch( i )
{
    case -1:
        n++;
        break;
    case 0 :
        z++;
        break;
    case 1 :
        p++;
        break;
}

```

The following code block will execute case -1, case 0, or case 1 based on the value of the variable i. Because break statements are included, no follow through will occur and only the matching case will be executed. 
