---
title: "Regular Expressions and Regular Languages"
datePublished: Mon Oct 23 2023 12:33:14 GMT+0000 (Coordinated Universal Time)
cuid: clo2vp4gk001j09li5p90h29m
slug: regular-expressions-and-regular-languages
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1698064359945/2c340f92-da2d-4803-b56c-fb8babe20c09.png
tags: theory-of-computation

---

Regular Expressions are the expressions that describe the language accepted by Finite Automata. It is the most efficient way to represent any language. 

The languages accepted by some regular expressions are referred to as **Regular languages**.

Regular expressions are used to check and match character combinations in strings. The string-searching algorithm uses this pattern to find the operations on a string.

Let **Σ** be an alphabet that denotes the input set.

The regular expression over Σ can be defined as follows:-

1.) Φ is a regular expression that denotes the empty set.

2.) ε is a regular expression and denotes the set {ε}, called a null string.

3.) For each ‘x’ in Σ ‘x’ is a regular expression and denotes the set {x}.

4.) If ‘a’ and ‘b’ are the regular expressions that denote the language L1 and L2, respectively, then:-

     a.) a+b is equal to L1 U L2 union.

     b.) ab is equal to the L1L2 concatenation.

     c.) a\* is equal to L1\* closure.

In a regular expression, **a\*** means zero or more occurrences of a. It can generate {ε, a, aa, aaa, aaaa, aaaaa, .....}.

In a regular expression, **a<sup>+</sup>** means one or more occurrences of a. It can generate {a, aa, aaa, aaaa, aaaaa, .....}.

---

The various operations in the regular language are:

#### **1) Union** 

If R and S are two regular languages, their union R U S is also a Regular Language.

R U S = {a | a is in R or a is in S} 

##### **2) Intersection** 

If R and S are two regular languages, their intersection is also a Regular Language.

L ⋂ M = {ab | a is in R and b is in S} 

##### **3) Kleene closure** 

If R is a regular language, its Kleene closure R1\* will also be a Regular Language.

R\* = Zero or more occurrences of language R.

Let us look at some examples of Regular Expressions

```plaintext
Question 1: Write the regular expression for the language accepting all the string which are starting with 1 and ending with 0, over ∑ = {0, 1}.
```

In a regular expression, the first symbol should be 1, and the last symbol should be 0. The r.e. is as follows:

R = 1 (0+1)\* 0  

```plaintext
Question 2: Write the regular expression for the language starting and ending with a and having any having any combination of b's in between.
```

The regular expression will be:

R = a b\* b  

```plaintext
Question 3: Write the regular expression for the language starting with a but not having consecutive b's.
```

The regular expression has to be built for the language:

L = {a, aba, aab, aba, aaa, abab, .....}  

The regular expression for the above language is:

R = {a + ab}\*  

```plaintext
Question 4: Write the regular expression for the language accepting all the string in which any number of a's is followed by any number of b's is followed by any number of c's.
```

As we know, any number of a's means a\* any number of b's means b\*, any number of c's means c\*. Since as given in problem statement, b's appear after a's and c's appear after b's. So the regular expression could be:

R = a\* b\* c\*  

```plaintext
Question 5: Write the regular expression for the language L over ∑ = {0, 1} such that all the string do not contain the substring 01.
```

The Language is as follows:

L = {ε, 0, 1, 00, 11, 10, 100, .....}  

The regular expression for the above language is as follows:

R = (1\* 0\*)  

Before we wrap up Regular Expressions, we must know that finite automata and regular expressions are closely related concepts in the theory of computation. 

![Relationship between Finite Automata and Regular Expression](https://files.codingninjas.in/article_images/regular-expression-and-finite-automata-2-1688306139.jpg align="center")

The relationship between Finite Automata (FA) and Regular Expressions (RE) can be described in several steps:

1. Using epsilon moves, regular expressions can be transformed into Non-deterministic Finite Automata (NFA). Without an input symbol, epsilon moves lets you jump from one state to another.
    
2. The NFA with epsilon moves can be transformed into an equivalent NFA without epsilon moves. This process involves eliminating the epsilon transitions by performing the epsilon closure operation and creating new transitions.
    
3. The NFA can be further transformed into a Deterministic Finite Automata (DFA) without epsilon stages. For this conversion, a new state must be created for each subset of the NFA states, and transitions are chosen based on the possible inputs for each state.
    
4. Additionally, a DFA can be converted back into a Regular Expression. This kind of data conversion is possible using methods like state elimination, in which unnecessary states are gradually eliminated until a regular expression representation is produced.
    

This was all about Regular Expressions and Regular Languages in the field of computational theory.