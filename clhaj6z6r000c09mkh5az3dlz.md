---
title: "Basics of R"
datePublished: Fri May 05 2023 12:27:25 GMT+0000 (Coordinated Universal Time)
cuid: clhaj6z6r000c09mkh5az3dlz
slug: basics-of-r
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1683289609005/e3504c9c-b88e-4bfe-979a-efd9ed248c0c.png
tags: r

---

R is an interpreted programming language. It also allows you to carry out modular programming with the help of functions. It is widely used to analyze statistical information as well as graphical representation.

## Hello World

Let's try to create your first R program. We will try to create a simple `Hello, World` Program.

A Hello World program is a simple program that simply prints a `"Hello World!"` message on the screen. It's generally used to introduce a new language to learners.

Consider the program below.

```r
message <-"Hello World!"
print(message)
```

Here, we have created a simple variable called message. We have initialized this variable with a simple message string called "Hello World!". On execution, this program prints the message stored inside the variable.

Every output in R is preceded by a number (say n) in square brackets. This number means that the displayed value is the nth element printed.

**Output:**

```r
[1] "Hello World!"
```

## Comments in R

Comments are portions of a computer program that are used to describe a piece of code. For example,

```r
# declare variable
age = 24

# print variable
print(age)
```

Here, #declare variable and #print variable are two comments used in the code.

Comments have nothing to do with code logic. They do not get interpreted or compiled and are completely ignored during the execution of the program.

### Types of Comments in R

In general, all programming languages have the following types of comments:

* single-line comments
    
* multi-line comments
    

However, in R programming, there is no functionality for multi-line comments. Thus, you can only write single-line comments in R.

You use the `#` symbol to create single-line comments in R. For example,

```r
# this code prints Hello World
print("Hello World")
```

**Output**

```r
[1] "Hello World"
```

In the above example, we have printed the text `Hello World` to the screen. Here, just before the print statement, we have included a single-line comment using the `#` symbol.

**Note**: You can also include a single-line comment in the same line after the code. For example,

```r
print("Hello World") # this code prints Hello World
```

As already mentioned, R does not have any syntax to create multi-line comments.

However, you can use consecutive single-line comments to create a multi-line comment in R. For example,

```r
# this is a print statement
# it prints Hello World

print("Hello World")
```

**Output**

```r
[1] "Hello World"
```

In the above code, we have used multiple consecutive single-line comments to create a multi-line comment just before the print statement.

## Variables in R

In computer programming, a variable is a named memory location where data is stored. For example,

```r
x = 13.8
```

Here, x is the variable where the data **13.8** is stored. Now, whenever we use x in our program, we will get **13.8**.

```r
x = 13.8

# print variable
print(x)
```

**Output**

```r
[1] 13.8
```

As you can see, when we print x we get 13.8 as output.

### Rules of Declaring Variables

As per our requirements, we can use any name for our variables. However, certain rules need to be followed while creating a variable:

* A variable name in R can be created using letters, digits, periods, and underscores.
    
* You can start a variable name with a letter or a period, but not with digits.
    
* If a variable name starts with a dot, you can't follow it with digits.
    
* R is case-sensitive. This means that age and Age are treated as different variables.
    
* We have some reserved words that cannot be used as variable names.
    

### Logical Variables

It stores single-bit data which is either `TRUE` or `FALSE`. Here, `TRUE` means yes and `FALSE` means no. For example,

```r
a = TRUE

print(a)
print(class(a))
```

**Output**

```r
[1] TRUE
[1] "logical"
```

Here, we have declared the boolean variable a with the value `TRUE`. Logical variables belong to the logical class so `class(a)` returns `"logical"`.

### Integer Variables

It stores numeric data without any decimal values. For example,

```r
A = 14L

print(A)
print(class(A))
```

**Output**

```r
[1] 14
[1] "integer"
```

Here, `L` represents an integer value. In R, integer variables belong to the integer class so, `class(a)` returns `"integer"`.

### Numeric Variables

It stores numeric data with decimal values. For example,

```r
x = 13.4

print(x)
print(class(x))
```

**Output**

```r
[1] 13.4
[1] "numeric"
```

Here, we have created a floating point variable named x. You can see that the floating point variable belongs to the `numeric` class.

### Character Variables

It stores single-character data. For example,

```r
alphabet = "a"

print(alphabet)
print(class(alphabet))
```

**Output**

```r
[1] "a"
[1] "character"
```

Here, we have created a character variable named alphabet. Since character variables belong to the character class, `class(alphabet)` returns `"character"`.

### String Variables

It stores data that is composed of more than one character. We use double quotes to represent string data. For example,

```r
message = "Welcome to Binary Bits!"

print(message)
print(class(message))
```

**Output**

```r
[1] "Welcome to Binary Bits!"
[1] "character"
```

Here, we have created a string variable named message. You can see that the string variable also belongs to the `character` class.

### Complex Variables

A complex variable is data that contains a real and an imaginary part (denoted by the suffix `i`). For example,

```r
y <- 3.2e-1i
print(y)
print(typeof(y))
```

**Output**

```r
[1] 0+0.32i
[1] "complex"
```

### Special Constants in R

R programming also provides 4 special types of constants.

* `NULL` - to declare an empty R object. For example,
    
    ```r
    x <- NULL
    print(x)  # NULL
    print(typeof(x))  # "NULL"
    ```
    
* `Inf/-Inf` - represents positive and negative infinity. For example,
    
    ```r
    # result is too big so it represents positive infinity
    a <- 2^2020
    print(a)   # Inf
    
    # result is too big
    # represents negative infinity
    b <- -2^2020
    print(b)    # -Inf
    ```
    
* `NaN` (Not a Number) - represents an undefined numerical value. For example,
    
    ```r
    print(0/0)      # NaN
    print(Inf/Inf)  # NaN
    ```
    
* `NA` - represents a value which is not available. For example,
    
    ```r
    print(NA + 20) # NA
    ```
    

### Raw Datatype

A `raw` data type specifies values as raw bytes. You can use the following methods to convert character data types to raw data types and vice-versa:

* `charToRaw()` - converts character data to raw data
    
* `rawToChar()` - converts raw data to character data
    

For example,

```r
# convert character to raw
raw_variable <- charToRaw("Welcome to Binary Bits")

print(raw_variable)
print(class(raw_variable))

# convert raw to character
char_variable <- rawToChar(raw_variable)

print(char_variable)
print(class(char_variable))
```

**Output**

```r
[1] 57 65 6c 63 6f 6d 65 20 74 6f 20 50 72 6f 67 72 61 6d 69 7a
[1] "raw"
[1] "Welcome to Binary Bits"
[1] "character"
```

In this program,

* We first used the `charToRaw()` function to convert the string `"Welcome to Binary Bits"` to raw bytes.
    
    This is why we get `"raw"` as output when we print the class of raw\_variable.
    
* Then, we used the `rawToChar()` function to convert the data in raw\_variable back to character form.
    
    This is why we get `"character"` as output when we print the class of char\_variable.
    

## print( ) function

In R, we use the `print()` function to print values and variables. For example,

```r
# print values
print("R is fun")

# print variables
x <- "Welcome to Binary Bits"
print(x)
```

**Output**

```r
[1] "R is fun"
[1] "Welcome to Binary Bits"
```

In the above example, we have used the `print()` function to print a string and a variable. When we use a variable inside `print()`, it prints the value stored inside the variable.

## paste( ) function

You can also print a string and variable together using the `print()` function. For this, you have to use the `paste()` function inside `print()`. For example,

```r
company <- "Binary Bits"

# print string and variable together
print(paste("Welcome to", company))
```

**Output**

```r
Welcome to Binary Bits
```

Notice the use of the `paste()` function inside `print()`. The `paste()` function takes two arguments:

* **string** - "Welcome to"
    
* **variable** - company
    

By default, you can see there is a space between string `Welcome to` and the value `Binary Bits`.

If you don't want any default separator between the string and variable, you can use another variant of `paste()` called `paste0()`. For example,

```r
company <- "Binary Bits"

# using paste0() instead of paste()
print(paste0("Welcome to", company))
```

**Output**

```r
[1] "Welcome toBinary Bits"
```

Now, you can see there is no space between the string and the variable.

## cat( ) function

R programming also provides the `cat()` function to print variables. However, unlike `print()`, the `cat()` function is only used with basic types like logical, integer, character, etc.

```r
# print using Cat
cat("R Tutorials\n")

# print a variable using Cat
message <- "Binary Bits"
cat("Welcome to ", message)
```

**Output**

```r
R Tutorials
Welcome to  Binary Bits
```

In the example above, we have used the `cat()` function to display a string along with a variable. The `\n` is used as a newline character.

This was all about the basics of R. Thanks for reading :).