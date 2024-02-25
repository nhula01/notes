---
title = "Query Gate"
---

The computational model is usually built as

input -&gt; computation -&gt; output

For query model, the input is not provided to the computation.
The input is a function that the computation acceses by making queries.
(random access to the input)

input

|  |
|--|
|  |

computation ---&gt; output

Since the input is hidden (oracle/blackbox), only by asking the information of
the input could be revealed.

For a funcion \\(f: \sum^n-> \sum^m\\).
When the query \\(x\in \sum^n\\) is made by a computation, a value \\(f(x) \in \sum^m\\)
is made available.

Efficiency of query algorithms: the number of queries made.

Examples:


## OR {#or}

\\(f: \sum^n -> \sum\\)

Output 1 if there exists string \\(x\in\sum^n\\) for which \\(f(x)=1\\)
Output 0 if there is no string like that/


## Parity {#parity}

\\(f: \sum^n -> \sum\\)
The goal is to determine if it is even or odd
0 if the set \\(\\{x \in \sum^n: f(x)=1\\}\\) has an even number of elements
1 otherwise


## Minimum {#minimum}

\\(f: \sum^n -> \sum^m\\)
compute the minimum of the intergers

Sometimes, we also have a promise on the input (some types of guarantee)
For example

unique Search:
we guarante that there is only one for which \\(f(x)=1\\)
