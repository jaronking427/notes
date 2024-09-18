#phil1440 
## Truth Tables
EXAMPLE:
> AvB
> ^A 
> B

| A   | ^ A |
| --- | --- |
| T   | F   |
| F   | T   |

--- 

### Disjuction (Or) ( Inclusive)

| A   | B   | A$\lor$B |
| --- | --- | -------- |
| T   | T   | T        |
| T   | F   | T        |
| F   | T   | T        |
| F   | F   | F        |

---
### Conjunction 
| A   | B   | A$\land$B |
| --- | --- | --------- |
| T   | T   | T         |
| T   | F   | F         |
| F   | T   | F         |
| F   | F   | F         |

--- 

| A   | B   | A$\lor$B | ^ A | ^ B |
| --- | --- | -------- | --- | --- |
| T   | T   | T        | F   | F   |
| T   | F   | T        | F   | T   |
| F   | T   | T        | T   | F   |
| F   | F   | F        | T   | T   |

---
### Not valid

| A   | B   | A v B | A   | ^ B |
| --- | --- | ----- | --- | --- |
| T   | T   | T     | T   | F   |
| T   | F   | T     | T   | T   |
| F   | T   | T     | F   | F   |
| F   | F   | F     | F   | T   |
Row 3 is a counterexample or a falsifying row

--- 

A
^A 
therefore B

| A   | B   | $\neg$A |
| --- | --- | ------- |
| T   | T   | F       |
| T   | F   | F       |
| F   | T   | T       |
| F   | F   | T       |
This is a valid argument, not a good argument but a valid one 

---
$.$ B
$...$A$\lor$$\neg$A
Valid argument, no way for the conclusion to be false

| A   | A$\lor$$\neg$A |
| --- | -------------- |
| T   | T              |
| F   | T              |

---
## Implication $\implies$
| A   | B   | A$\implies$B |
| --- | --- | ------------ |
| T   | T   | T            |
| T   | F   | F            |
| F   | T   | T            |
| F   | F   | T            |
Arrow is loose approximation of 'if'
Material conditional(Truth functional, loose approximation of if )

| A   | B   | A$\iff$B |
| --- | --- | -------- |
| T   | T   | F        |
| T   | F   | F        |
| F   | T   | F        |
| F   | F   | T        |
