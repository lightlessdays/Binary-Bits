---
title: "Finite Automata"
datePublished: Mon Oct 23 2023 11:37:21 GMT+0000 (Coordinated Universal Time)
cuid: clo2tp93m000i09kzh4zzbghu
slug: finite-automata
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1698061015334/0c72342d-71ac-4c5d-9e4d-2df8c789863e.png
tags: theory-of-computation

---

Finite automata are used to recognize patterns. It takes the string of symbols as input and changes its state accordingly. When the desired symbol is found, then the transition occurs. At the time of transition, the automata can either move to the next state or stay in the same state. Finite automata have two states, Accept state or **Reject state**. When the input string is processed successfully, and the automata reaches its final state, then it will accept.

Let us now formally define Finite Automata.

A finite automaton is a collection of 5-tuple (Q, ∑, δ, q0, F), where:

1. Q: a finite set of states
    
2. ∑: a finite set of the input symbol
    
3. q0: initial state
    
4. F: final state
    
5. δ: Transition function
    

Finite automata can be represented by input tape and finite control.

**Input tape:** It is a linear tape having some number of cells. Each input symbol is placed in each cell.

**Finite control:** The finite control decides the next state on receiving particular input from the input tape. The tape reader reads the cells one by one from left to right, and at a time only one input symbol is read.

![Finite Automata](https://static.javatpoint.com/tutorial/automata/images/finite-automata.png align="center")

There are two types of finite automata:

1. DFA(deterministic finite automata)
    
2. NFA(non-deterministic finite automata)
    

### Transition Diagram

A transition diagram or state transition diagram is a directed graph which can be constructed as follows:

* There is a node for each state in Q, which is represented by the circle.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697952825678/bfd482f4-2911-45e5-a491-7ea8a3a40518.png align="center")
    
* There is a directed edge from node q to node p labeled a if δ(q, a) = p.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697952861983/67b6c72c-d67e-4b14-ae93-7d0f158d9175.png align="center")
    
* In the start state, there is an arrow with no source.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697952882784/e96766a9-312b-4fd3-8202-e4db82754dd6.png align="center")
    
* Accepting states or final states are indicated by a double circle.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697952895658/ccdf7810-59c1-4dc9-8060-f8d1f5e20d35.png align="center")
    

### Deterministic Finite Automata

* DFA refers to deterministic finite automata. Deterministic refers to the uniqueness of the computation. The finite automata are called deterministic finite automata if the machine reads an input string one symbol at a time.
    
* In DFA, there is only one path for specific input from the current state to the next state.
    
* DFA does not accept the null move, i.e., the DFA cannot change state without any input character.
    
* DFA can contain multiple final states. It is used in Lexical Analysis in Compiler.
    

In the following diagram, we can see that from state q0 for input a, there is only one path that is going to q1. Similarly, from q0, there is only one path for input b going to q2.

![Deterministic finite automata](https://static.javatpoint.com/tutorial/automata/images/dfa.png align="center")

Formally, we can define DFA as follows:

A DFA is a collection of 5-tuples same as we described in the definition of FA.

1. Q: a finite set of states
    
2. ∑: a finite set of the input symbol
    
3. q0: initial state
    
4. F: **final** state
    
5. δ: Transition function
    

The transition function can be defined as:

δ: Q x ∑→Q

Graphically, we can define DFA as follows:

A DFA can be represented by digraphs called state diagrams. In which:

1. The state is represented by vertices.
    
2. The arc labeled with an input character shows the transitions.
    
3. The initial state is marked with an arrow.
    
4. The final state is denoted by a double circle.
    

This is how a DFA operates:

1. In DFA, the input to the automata can be any string. Now, put a pointer to the start state q read the input string w from left to right, and move the pointer according to the transition function, δ. We can read one symbol at a time. If the next symbol of string w is a and the pointer is on state p, move the pointer to δ(p, a). When the end of the input string w is encountered, then the pointer is on some state F.
    
2. The string w is said to be accepted by the DFA if r ∈ F which means the input string w is processed successfully and the automata reached its final state. The string is said to be rejected by DFA if r ∉ F.
    

Let us look at a question now.

```plaintext
Question 1: DFA with ∑ = {0, 1} accepts all strings starting with 1.
```

![Transition Diagram](https://static.javatpoint.com/tutorial/automata/images/transition-diagram2.png align="center")

The finite automata can be represented using a transition graph. In the above diagram, the machine initially is in start state q0 then on receiving input 1 the machine changes its state to q1. From q0 on receiving 0, the machine changes its state to q2, which is the dead state. From q1 on receiving input 0, 1 the machine changes its state to q1, which is the final state. The possible input strings that can be generated are 10, 11, 110, 101, 111......., that means all string starts with 1.

```plaintext
Question 2: DFA for
Q = {q0, q1, q2}  
∑ = {0, 1}  
q0 = {q0}  
F = {q2}
```

![Deterministic finite automata](https://static.javatpoint.com/tutorial/automata/images/dfa2.png align="center")

```plaintext
Question 3: DFA with ∑ = {0, 1} accepts all starting with 0.
```

![Deterministic finite automata](https://static.javatpoint.com/tutorial/automata/images/dfa3.png align="center")

In the above diagram, we can see that on given 0 as input to DFA in state q0 the DFA changes state to q1 and always go to final state q1 on starting input 0. It can accept 00, 01, 000, 001....etc. It can't accept any string that starts with 1, because it will never go to the final state on a string starting with 1.

```plaintext
Question 4: DFA with ∑ = {0, 1} accepts all ending with 0.
```

![Deterministic finite automata](https://static.javatpoint.com/tutorial/automata/images/dfa4.png align="center")

In the above diagram, we can see that on given 0 as input to DFA in state q0, the DFA changes state to q1. It can accept any string which ends with 0 like 00, 10, 110, 100....etc. It can't accept any string which ends with 1, because it will never go to the final state q1 on 1 input, so the string ending with 1, will not be accepted or will be rejected.

```plaintext
Question 5: Design a FA with ∑ = {0, 1} accepts those string which starts with 1 and ends with 0.
```

![Examples of Deterministic finite automata](https://static.javatpoint.com/tutorial/automata/images/examples-of-dfa.png align="center")

In state q1, if we read 1, we will be in state q1, but if we read 0 at state q1, we will reach state q2 which is the final state. In state q2, if we read either 0 or 1, we will go to q2 state or q1 state respectively. Note that if the input ends with 0, it will be in the final state.

```plaintext
Question 6: Design a FA with ∑ = {0, 1} accepts the only input 101.
```

![Examples of Deterministic finite automata](https://static.javatpoint.com/tutorial/automata/images/examples-of-dfa2.png align="center")

In the given solution, we can see that only input 101 will be accepted. Hence, for input 101, there is no other path shown for other input.

```plaintext
Question 7: Design FA with ∑ = {0, 1} accepts even number of 0's and even number of 1's.
```

![Examples of Deterministic finite automata](https://static.javatpoint.com/tutorial/automata/images/examples-of-dfa3.png align="center")

Here q0 is a start state and the final state also. Note carefully that a symmetry of 0's and 1's is maintained. We can associate meanings to each state as:

q0: state of even number of 0's and even number of 1's.  
q1: state of odd number of 0's and even number of 1's.  
q2: state of odd number of 0's and odd number of 1's.  
q3: state of even number of 0's and odd number of 1's.

```plaintext
Question 8: Design FA with ∑ = {0, 1} accepts the set of all strings with three consecutive 0's.
```

The strings that will be generated for this particular languages are 000, 0001, 1000, 10001, .... in which 0 always appears in a clump of 3. The transition graph is as follows:

![Examples of Deterministic finite automata](https://static.javatpoint.com/tutorial/automata/images/examples-of-dfa4.png align="center")

```plaintext
Question 9: Design a FA with ∑ = {0, 1} accepts the strings with an even number of 0's followed by single 1.
```

![Examples of Deterministic finite automata](https://static.javatpoint.com/tutorial/automata/images/examples-of-dfa7.png align="center")

### Non Deterministic Finite Automata

NFA stands for non-deterministic finite automata. It is easier to construct an NFA than a DFA for a given regular language. The finite automata are called NFA when there exist many paths for specific input from the current state to the next state. Every NFA is not DFA, but each NFA can be translated into DFA. NFA is defined in the same way as DFA but with the following two exceptions, it contains multiple next states, and it contains ε transition.

In the following image, we can see that from state q0 for input a, there are two next states q1 and q2, similarly, from q0 for input b, the next states are q0 and q1. Thus it is not fixed or determined with a particular input where to go next. Hence this FA is called non-deterministic finite automata.

![Non-Deterministic finite automata](https://static.javatpoint.com/tutorial/automata/images/nfa.png align="center")

Formally, we can define NFA as follows:

NFA also has five states same as DFA, but with different transition function, as shown follows:

δ: Q x ∑ →2Q  
where,

1. Q: finite set of states  
    
2. ∑: finite set of the input symbol  
    
3. q0: initial state   
    
4. F: **final** state  
    
5. δ: Transition function  
    

Graphically, NFA can be defined as follows:

An NFA can be represented by digraphs called state diagram. In which:

1. The state is represented by vertices.
    
2. The arc labeled with an input character show the transitions.
    
3. The initial state is marked with an arrow.
    
4. The final state is denoted by the double circle.
    

Let us look at some questions to understand NFA in more detail.

```plaintext
Question 10: NFA with ∑ = {0, 1} accepts all strings with 01.
```

![Non-Deterministic finite automata](https://static.javatpoint.com/tutorial/automata/images/nfa3.png align="center")

```plaintext
Question 11: NFA with ∑ = {0, 1} and accept all string of length atleast 2.
```

![Non-Deterministic finite automata](https://static.javatpoint.com/tutorial/automata/images/nfa4.png align="center")

```plaintext
Question 12: Design an NFA with ∑ = {0, 1} accepts all string ending with 01.
```

We can write this diagrammatically as:

![Examples of NFA](https://static.javatpoint.com/tutorial/automata/images/examples-of-nfa2.png align="center")

Hence, NFA would be:

![Examples of NFA](https://static.javatpoint.com/tutorial/automata/images/examples-of-nfa3.png align="center")

```plaintext
Question 13: Design an NFA with ∑ = {0, 1} in which double '1' is followed by double '0'.
OR
Question 13: Design an NFA in which all the string contain a substring 1100.
```

The FA with double 1 is as follows:

![Examples of NFA](https://static.javatpoint.com/tutorial/automata/images/examples-of-nfa4.png align="center")

It should be immediately followed by double 0. Then,

![Examples of NFA](https://static.javatpoint.com/tutorial/automata/images/examples-of-nfa5.png align="center")

Now before double 1, there can be any string of 0 and 1. Similarly, after double 0, there can be any string of 0 and 1. Hence the NFA becomes:

![Examples of NFA](https://static.javatpoint.com/tutorial/automata/images/examples-of-nfa6.png align="center")

```plaintext
Question 14: Design an NFA with ∑ = {0, 1} accepts all string in which the third symbol from the right end is always 0.
```

![Examples of NFA](https://static.javatpoint.com/tutorial/automata/images/examples-of-nfa9.png align="center")

Thus we get the third symbol from the right end as '0' always. The NFA can be:

![Examples of NFA](https://static.javatpoint.com/tutorial/automata/images/examples-of-nfa10.png align="center")

This was all about Finite Automata and the two types of Finite Automata in Computational Theory.