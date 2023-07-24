---
title: "Loops in R"
datePublished: Fri May 05 2023 17:17:54 GMT+0000 (Coordinated Universal Time)
cuid: clhatkiyl000i09mg92368hdd
slug: loops-in-r
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1683307049616/7ff7d202-3bb3-49aa-bf85-3f19a595da71.png
tags: r

---

In R programming, we require a control structure to run a block of code multiple times. Loops come in the class of the most fundamental and vital programming concepts. A circle is a control statement that allows multiple executions of a statement or a set of statements. The word ‘looping’ means cycling or iterating. 

A loop asks a query, in the loop structure. If the answer to that query requires an action, it will be executed. The same query is asked again and again until further action is taken. Any time the query is asked in the loop, it is known as an iteration of the loop. There are two components of a loop, the control statement, and the loop body.  The control statement controls the execution of statements depending on the condition and the loop body consists of the set of statements to be executed.

In order to execute identical lines of code numerous times in a program, a programmer can simply use a loop. 

There are three types of loops in R programming: 

1. for loop
    
2. while loop
    
3. repeat loop
    

## for loop

It is a type of control statement that enables one to easily construct a loop that has to run statements or a set of statements multiple times. For loop is commonly used to iterate over items of a sequence. It is an entry-controlled loop, in this loop, the test condition is tested first, and then the body of the loop is executed, the loop body would not be executed if the test condition is false. 

```r
for (value in sequence)
{
  statement
}
```

Let us take an example of a program to display numbers from 1 to 5 using for loop in R. 

```r
# R program to demonstrate the use of for loop

# using for loop
for (val in 1: 5)
{
	# statement
	print(val)
}
```

**Output:** 

```r
[1] 1
[1] 2
[1] 3
[1] 4
[1] 5
```

Here, for loop is iterated over a sequence having numbers from 1 to 5. In each iteration, each item of the sequence is displayed. 

## while loop

It is a type of control statement which will run a statement or a set of statements repeatedly unless the given condition becomes false. It is also an entry-controlled loop, in this loop, the test condition is tested first, and then the body of the loop is executed, the loop body would not be executed if the test condition is false. 

```r
while ( condition ) 
{
  statement
}
```

Below are some programs to illustrate the use of the while loop in R programming. Let us take an example of a program to display numbers from 1 to 5 using a while loop in R. 

```r
# R program to demonstrate the use of while loop

val = 1

# using while loop
while (val <= 5)
{
	# statements
	print(val)
	val = val + 1
}
```

**Output:** 

```r
[1] 1
[1] 2
[1] 3
[1] 4
[1] 5
```

Initially, the variable value is initialized to 1. In each iteration of the while loop, the condition is checked and the value of value is displayed then it is incremented until it becomes 5 and the condition becomes false, the loop is terminated. 

## repeat loop

It is a simple loop that will run the same statement or a group of statements repeatedly until the stop condition has been encountered. Repeat loop does not have any condition to terminate the loop, a programmer must specifically place a condition within the loop’s body and use the declaration of a break statement to terminate this loop. If no condition is present in the body of the repeat loop then it will iterate infinitely.

```r
repeat 
{ 
   statement
 
   if( condition ) 
   {
      break
   }
}
```

To terminate the repeat loop, we use a jump statement that is the break keyword. Let us take an example of a program to display numbers from 1 to 5 using a repeat loop in R. 

```r
# R program to demonstrate the use of repeat loop

val = 1

# using repeat loop
repeat
{
	# statements
	print(val)
	val = val + 1

	# checking stop condition
	if(val > 5)
	{
		# using break statement
		# to terminate the loop
		break
	}
}
```

**Output:** 

```r
[1] 1
[1] 2
[1] 3
[1] 4
[1] 5
```

In the above program, the variable val is initialized to 1, then in each iteration of the repeat loop the value of val is displayed and then it is incremented until it becomes greater than 5. If the value of val becomes greater than 5 then break statement is used to terminate the loop.

## jump statements

We use a jump statement in loops to terminate the loop at a particular iteration or to skip a particular iteration in the loop. The two most commonly used jump statements in loops are: 

* **Break Statement:** The break keyword is a jump statement that is used to terminate the loop at a particular iteration.
    

**Example:**

```r
# R program to illustrate
# the use of break statement

# using for loop
# to iterate over a sequence
for (val in 1: 5)
{
	# checking condition
	if (val == 3)
	{
		# using break keyword
		break
	}

	# displaying items in the sequence
	print(val)
}
```

**Output:** 

```r
[1] 1
[1] 2
```

In the above program, if the value of val becomes 3 then the break statement will be executed and the loop will terminate.

* **Next Statement:** The next keyword is a jump statement which is used to skip a particular iteration in the loop.
    

**Example:** 

```r
# R program to illustrate
# the use of next statement

# using for loop
# to iterate over the sequence
for (val in 1: 5)
{
	# checking condition
	if (val == 3)
	{
		# using next keyword
		next
	}

	# displaying items in the sequence
	print(val)
}
```

**Output:** 

```r
[1] 1
[1] 2
[1] 4
[1] 5
```

In the above program, if the value of Val becomes 3 then the next statement will be executed hence the current iteration of the loop will be skipped. So 3 is not displayed in the output.c