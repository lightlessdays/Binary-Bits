---
title: "Data Structures in R"
datePublished: Sat May 06 2023 08:48:16 GMT+0000 (Coordinated Universal Time)
cuid: clhbqt01q000809mf0bvq597v
slug: data-structures-in-r
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1683361242457/5a34df76-08f3-4f59-b451-3e774c818cdb.png
tags: r

---

A data structure is essentially a way to organize data in a system to facilitate effective usage of the same. The whole idea is to reduce the complexities of space and time in various tasks.

While using a programming language, different variables are essential to store different data. These variables are reserved in a memory location for storing values. Once a variable is created, some area in the memory is reserved.

Data structures are objects that are manipulated regularly in R. They are used to store data in an organized fashion to make data manipulation and other data operations more efficient. R has many data structures. The following section will discuss them in detail.

## Vectors

Vector is one of the basic data structures in R. It is homogenous, which means that it only contains elements of the same data type. Data types can be numeric, integer, character, complex, or logical.

Vectors are created by using the c() function. Coercion takes place in a vector, from bottom to top, if the elements passed are of different data types, from logical to integer to double to the character.

The typeof() function is used to check the data type of the vector, and the class() function is used to check the class of the vector.

```r
Vec1 <- c(44, 25, 64, 96, 30)
Vec2 <- c(1, FALSE, 9.8, "hello world")
typeof(Vec1)
typeof(Vec2)
```

**Output:**

```r
[1] "double"
[1] "character"
```

To delete a vector, you simply have to do the following:

```r
Vec1 <- NULL
Vec2 <- NULL
```

Vectors can be accessed in the following ways:

* Elements of a vector can be accessed by using their respective indexes. \[ \] brackets are used to specify indexes of the elements to be accessed.
    

**For example:**

```r
x <- c("Jan","Feb","March","Apr","May","June","July")
y <- x[c(3,2,7)]
print(y)
```

**Output:**

```r
[1] "March" "Feb"   "July"
```

* Logical indexing, negative indexing, and 0/1 can also be used to access the elements of a vector.
    

**For example:**

```r
x <- c("Jan","Feb","March","Apr","May","June","July")
y <- x[c(TRUE,FALSE,TRUE,FALSE,FALSE,TRUE,TRUE)]z <- x[c(-3,-7)]c <- x[c(0,0,0,1,0,0,1)]
print(y)
print(z)
print(c)
```

**Output:**

```r
[1] "Jan"   "March" "June" "July"(All TRUE values are printed)
[1] "Jan" "Feb" "Apr" "May" "June"(All corresponding values for negative indexes are dropped)
[1] "Jan" "Jan"(All corresponding values are printed)
```

You can perform addition, subtraction, multiplication, and division on vectors having the same number of elements in the following ways:

```r
v1 <- c(4,6,7,31,45)
v2 <- c(54,1,10,86,14,57)
add.v <- v1+v2
print(add.v)
sub.v <- v1-v2
print(sub.v)
multi.v <- v1*v2
print(multi.v)
divi.v <- v1/v2
print(divi.v)
```

**Output:**

```r
[1]  58   7  17 117  59  66
[1] -50   5  -3 -55  31 -48
[1]  216    6   70 2666  630  513
[1] 0.07407407 6.00000000 0.70000000 0.36046512 3.21428571 0.15789474
```

If arithmetic operations are performed on vectors having unequal lengths, then a vector’s elements, which are shorter in number as compared to the elements of other vectors, are recycled. For example:

```r
v1 <- c(8,7,6,5,0,1)
v2 <- c(7,15)                               
add.v <- v1+v2                                     
(v2 becomes c(7,15,7,15,7,15))
print(add.v)
sub.v <- v1-v2
print(sub.v)
```

**Output:**

```r
[1] 15 22 13 20  7 16
[1]   1  -8  -1 -10  -7 -14
```

You can sort the elements of a vector by using the sort() function in the following way:

```r
v <- c(4,78,-45,6,89,678)
sort.v <- sort(v)
print(sort.v)

#Sort the elements in the reverse order
revsort.v <- sort(v, decreasing = TRUE)
print(revsort.v) 
#Sorting character vectors
v <- c("Jan","Feb","March","April")
sort.v <- sort(v)
print(sort.v) 
#Sorting character vectors in reverse order
revsort.v <- sort(v, decreasing = TRUE)
print(revsort.v)
```

**Output:**

```r
[1] -45   4   6 78 89 678
[1] 678 89 78   6   4 -45
[1] "April" "Feb" "Jan"   "March"
[1] "March" "Jan"   "Feb"   "April"
```

## Lists

A list is a non-homogeneous data structure, which implies that it can contain elements of different data types. It accepts numbers, characters, lists, and even matrices and functions inside it. It is created by using the list() function.

**For example:**

```r
list1<- list("Sam", "Green", c(8,2,67), TRUE, 51.99, 11.78,FALSE)
print(list1)
```

**Output:**

```r
[[1]]
[1] "Sam"
[[2]]
[1] "Green"
[[3]]
[1]  8  2 67
[[4]]
[1] TRUE
[[5]]
[1] 51.99
[[6]]
[1] 11.78
[7]]
[1] FALSE
```

The elements of a list can be accessed by using the indices of those elements.

For example:

```r
list2 <- list(matrix(c(3,9,5,1,-2,8), nrow = 2), c("Jan","Feb","Mar"), list(3,4,5))
print(list2[1])
print(list2[2])
print(list2[3])
```

**Output:**

```r
[[1]]
[,1] [,2] [,3]          (First element of the list)
[1,]    3    5   -2
[2,]    9    1    8
[[1]]
[1] "Jan" "Feb" "Mar"        (Second element of the list)
[1,]    3    5   -2
[[1]]
[[1]][[1]]
[1] 3
[[1]][[2]]                      (Third element of the list)
[1] 4
[[1]][[3]]
[1] 5
```

You can add and delete elements only at the end of a list.

**For example:**

```r
list2 <- list(matrix(c(3,9,5,1,-2,8), nrow = 2), c("Jan","Feb","Mar"), list(3,4,5))
list2[4] <- “HELLO”
print(list2[4])
```

**Output:**

```r
[[1]]
[1] "Hello"
```

**Similarly,**

```r
list2[4] <- NULL
print(list2[4])
```

**Output:**

```r
[[1]]
NULL
```

To update a value in a list, use the following syntax:

```r
list2[3] <- "Element Updated"
print(list2[3])
```

**Output:**

```r
[[1]]
[1] "Element Updated"
```

## Matrices

Matrix is a two-dimensional data structure that is homogenous, meaning that it only accepts elements of the same data type. Coercion takes place if elements of different data types are passed. It is created by using the matrix() function.

The basic syntax to create a matrix is given below:

```r
matrix(data, nrow, ncol, byrow, dimnames)
where,
data = the input element of a matrix given as a vector.
nrow = the number of rows to be created.
ncol = the number of columns to be created.
byrow = the row-wise arrangement of the elements instead of column-wise
dimnames = the names of columns or rows to be created.
```

**For example:**

```r
M1 <- matrix(c(1:9), nrow = 3, ncol =3, byrow= TRUE)
print(M1)
```

**Output:**

```r
[,1] [,2] [,3]
[1,]    1    2    3
[2,]    4    5    6
[3,]    7    8    9
M2 <-  matrix(c(1:9), nrow = 3, ncol =3, byrow= FALSE)
print(M2)
```

**Output:**

```r
[,1] [,2] [,3]
[1,]    1    4    7
[2,]    2    5    8
[3,]    3    6    9
```

By using row and column names, a matrix can be created as follows:

```r
rownames = c("row1", "row2", "row3")
colnames = c("col1", "col2", "col3")
M3 <- matrix(c(1:9), nrow = 3, byrow = TRUE, dimnames = list(rownames, colnames))
print(M3)
```

**Output:**

```r
col1 col2 col3
row1    1    2    3
row2    4    5    6
row3    7    8    9
```

To access the elements of a matrix, row and column indices are used in the following ways:  
For accessing the elements of the matrix M3 created above, use the following syntax:

```r
print(M3[1,1])
print(M3[3,3])
print(M3[2,3])
```

**Output:**

```r
[1] 1 (Element at first row and first column)
[1] 9 (Element at third row and third column)
[1] 6 (Element at second row and third column)
```

## Factors

Factors are used in data analysis for statistical modelling. They are used to categorize unique values in columns, such as “Male”, “Female”, “TRUE”, “FALSE”, etc., and store them as levels. They can store both strings and integers. They are useful in columns that have a limited number of unique values.

Factors can be created using the **factor()** function and they take vectors as inputs.  
**For example**:

```r
data <- c("Male","Female","Male","Child","Child","Male","Female","Female")
print(data)
factor.data <- factor(data)
print(factor.data)
```

**Output:**

```r
[1] Male   Female Male   Child  Child  Male   Female Female
Levels: Child Female Male
```

For any data frame, R treats the text column as categorical data and creates factors on it.

## Dataframes

A data frame is a two-dimensional array-like structure that also resembles a table, in which each column contains values of one variable and each row contains one set of values from each column.

A data frame has the following characteristics:

* The column names of a data frame should not be empty.
    
* The row names of a data frame should be unique.
    
* The data stored in a data frame can be a numeric, factor, or character type.
    
* Each column should contain the same number of data items.
    

You can use the following syntax for creating a data frame in R programming:

```r
empid <- c(1:4)
empname <- c("Aditya","Shubham","Shankar","Vivek")
empdept <- c("Cryptography","5G","DevOps","Quantum Computing")
empdata <- data.frame(empid,empname,empdept)
print(emp.data)
```

**Output:**

| empid | empname | empdept |
| --- | --- | --- |
| 1 | Aditya | Cryptography |
| 2 | Shubham | 5G |
| 3 | Shankar | DevOps |
| 4 | Vivek | Quantum Computing |

To extract a specific column from a data frame, use the following syntax:

```r
result <- data.frame(empdata$empname,empdata$empdept)
print(result)
```

**Output:**

| empname | empdept |
| --- | --- |
| Aditya | Cryptography |
| Shubham | 5G |
| Shankar | DevOps |
| Vivek | Quantum Computing |

To extract specific rows from a data frame, use the following syntax:

```r
result <- empdata[1:2,]
print(result)
```

**Output:**

| empid | empdept |
| --- | --- |
| Aditya | Cryptography |
| Shubham | 5G |

The following code extracts the first and third rows with second and third columns respectively.

```r
result <- empdata[c(1,2),c(2,3)]
print(result)
```

**Output:**

| empname | empdept |
| --- | --- |
| Aditya | Cryptography |
| Shankar | DevOps |

To add a salary column to the above data frame, you can use the following syntax:

```r
empdata$salary <- c(20000,30000,40000,27000)
n <- empdata
print(n)
```

**Output:**

| empid | empname | empdept | salary |
| --- | --- | --- | --- |
| 1 | Aditya | Cryptography | 20000 |
| 2 | Shubham | 5G | 30000 |
| 3 | Shankar | DevOps | 40000 |
| 4 | Vivek | Quantum Computing | 27000 |

To add a new row(s) to an existing data frame, you need to create a new data frame that contains the new row(s), and then merge it with the existing data frame using the rbind() function.

**Creating a New Data Frame**

```r
empnewdata <-   data.frame(
empid = c(5:7),
empname = c("Shivank","Wafi","Dhruv"),
empdept = c("DevOps","AI/ML","AR/VR"),
salary = c(32000,51000,60000)
)
```

**Merging the New Data Frame with the Existing Data Frame**

```r
empfinaldata <- rbind(empdata,empnewdata)
print(empfinaldata)
```

**Output:**

| empid | empname | empdept | salary |
| --- | --- | --- | --- |
| 1 | Aditya | Cryptography | 20000 |
| 2 | Shubham | 5G | 30000 |
| 3 | Shankar | DevOps | 40000 |
| 4 | Vivek | Quantum Computing | 27000 |
| 5 | Shivank | DevOps | 32000 |
| 6 | Wafi | AI/ML | 51000 |
| 7 | Dhruv | AR/VR | 60000 |

## Arrays

Arrays refer to the type of data structure that is used to store multiple items of a similar type together. This leads to a collection of items that are stored at contiguous memory locations. This memory location is denoted by the array name. The position of an element can be calculated simply by adding an offset to its base value.

An array consists of the following:

**Array Index:** The array index identifies the location of the element. The array index starts with 0.

**Array Element:** Array elements are items that are stored in the array.

**Array Length:** The array length is determined by the number of elements that can be stored by the array.

There are two types of arrays:

* One-dimensional Arrays
    
* Multi-dimensional Arrays
    

One- or single-dimensional arrays are the types of arrays that have array elements stored in a sequence and can be accessed in the same order. Multi-dimensional arrays are arrays that have elements stored in more than one dimension. They can be two- or three-dimensional arrays and can consist of row and column indexes.

An array is created using the array() function. It takes vectors as input and uses the values in the dim parameter to create an array.

The following example creates an array of two 3x3 matrices each with 3 rows and 3 columns.

```r
# Create two vectors of different lengths.
vector1 <- c(5,9,3)
vector2 <- c(10,11,12,13,14,15)

# Take these vectors as input to the array.
result <- array(c(vector1,vector2),dim = c(3,3,2))
print(result)
```

**Output:**

```r
, , 1

     [,1] [,2] [,3]
[1,]    5   10   13
[2,]    9   11   14
[3,]    3   12   15

, , 2

     [,1] [,2] [,3]
[1,]    5   10   13
[2,]    9   11   14
[3,]    3   12   15
```

You can access the array elements by referring to the index position. You can use the `[]` brackets to access the desired elements from an array:

For example:

```r
thisarray <- c(1:24)
multiarray <- array(thisarray, dim = c(4, 3, 2))

multiarray[2, 3, 2]
```

**Output:**

```r
[1] 22
```

To find out if a specified item is present in an array, use the `%in%` operator:

```r
thisarray <- c(1:24)
multiarray <- array(thisarray, dim = c(4, 3, 2))

2 %in% multiarray
```

**Output:**

```r
[1] TRUE
```

Use the `dim()` function to find the amount of rows and columns in an array:

```r
thisarray <- c(1:24)
multiarray <- array(thisarray, dim = c(4, 3, 2))

dim(multiarray)
```

**Output:**

```r
[1] 4 3 2
```

Use the `length()` function to find the dimension of an array:

```r
thisarray <- c(1:24)
multiarray <- array(thisarray, dim = c(4, 3, 2))

length(multiarray)
```

**Output:**

```r
[1] 24
```

You can loop through the array items by using a `for` loop:

```r
thisarray <- c(1:24)
multiarray <- array(thisarray, dim = c(4, 3, 2))

for(x in multiarray){
  print(x)
}
```

**Output:**

```r
[1] 1
[1] 2
[1] 3
[1] 4
[1] 5
[1] 6
[1] 7
[1] 8
[1] 9
[1] 10
[1] 11
[1] 12
[1] 13
[1] 14
[1] 15
[1] 16
[1] 17
[1] 18
[1] 19
[1] 20
[1] 21
[1] 22
[1] 23
[1] 24
```

Thanks for reading :)