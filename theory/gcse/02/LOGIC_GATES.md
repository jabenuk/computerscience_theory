# 2.7 Logic gates

**Q, in all logic gates, represents the final output.**

## 2.7.1 Types of logic gates

### AND gates

An AND gate checks if both of the given booleans are true. The shape is flat on the input side and circular on the output side.

<img src="/resources/logic-gates-and.png">

The notation of an AND gate can be any of the following:
```
A AND B
A /\ B
A.B
```

### OR gates

An OR gate checks if either of the given booleans are true. The shape is reminiscent of a rounded arrow head, the point on the output side.

<img src="/resources/logic-gates-or.png">

The notation of an OR gate can be any of the following:
```
A OR B
A \/ B
A+B
```

### NOT gates

A NOT gate inverses the given boolean. The shape is a simple isoceles triangle with a small circle on the point of the output side.

<img src="/resources/logic-gates-not.png">

The notation of a NOT gate can be any of the following:
```
NOT A
¬ A
~A
```

## 2.7.2 Combining logic gates

The following equations are all the same; they combine two AND gates. The result (Q) is true only if all three inputs A, B, and C are true. 
```
Q = (A AND B) AND C
Q = (A /\ B) /\ C
Q = (A.B).C
```

Again, the following equations are all the same; this time, they combine an OR gate and a NOT gate. The result (Q) is true if both inputs A and B are false.
```
Q = NOT (A OR B)
Q = ¬ (A+B)
Q = ~(A+B)
etc ...
```
This is a **NOR** gate. To create a **NAND** gate, replicate this combination, replacing all instances of *OR* (or notational equivalents) with *AND* (or notational equivalents).

## References

### Sections
 - [2.7.1 Types of logic gates](https://www.bbc.co.uk/bitesize/guides/zkkkw6f/revision/2)
 - [2.7.2 Combining logic gates](https://www.bbc.co.uk/bitesize/guides/zjw8jty/revision/5)
