## Truth-Tables and the Conditional
>A$\lor$B
>$\neg$ A
>Therefore B

| A   | B   | A$\lor$B | $\neg$A | B   |
| --- | --- | -------- | ------- | --- |
| T   | T   | T        | F       | T   |
| T   | F   | T        | F       | F   |
| F   | T   | T        | T       | T   |
| F   | F   | F        | T       | F   |
### Conditional (Material Conditional)

| A   | B   | A$\implies$B |
| --- | --- | ------------ |
| T   | T   | T            |
| T   | F   | F            |
| F   | T   | T            |
| F   | F   | T            |
```
If it is raining, Alice is upset
Alice is upset
So it is raining
```
> Logical fallacy, 'Affirming the consequent'
> Formalizing the argument
> A$\implies$B
> B
> A

| A   | B   | A$\implies$B |     |
| --- | --- | ------------ | --- |
| T   | T   | T            |     |
| T   | F   | F            |     |
| F   | T   | T            |     |
| F   | F   | T            |     |
> Row 3 is our 'Falsifying row'

```
P. If its raining then alice is upset
C. If Alice is not upset it is not raining
```
> A$\implies$B
> ($\neg$A) $\implies$($\neg$B)

| A   | B   | A$\implies$B | ($\neg$B) $\implies$ ($\neg$A) |
| --- | --- | ------------ | ------------------------------ |
| T   | T   | T            | F        T        F            |
| T   | F   | F            | T        F        F            |
| F   | T   | T            | F        T        T            |
| F   | F   | T            | T        T        T            |
>Valid because no row where the premise is all true and the conclusion is false. 
> Two sentences of TFL are logically equivalent when each follows deductively from the other -> They have the same truth tables

#### (A$\iff$B) is logically equivalent to (A$\implies$B)  $\land$ (B$\implies$A)
do a and b have the same truth value?

| A   | B   | A$\iff$B |
| --- | --- | -------- |
| T   | T   | T        |
| T   | F   | F        |
| F   | T   | F        |
| F   | F   | T        |
```
Alice is upset if and only if its raining
it is raining 
Alice is upset
```
> A$\iff$B
> B
> A

### Truth tables with 3 arguments
>A$\implies$B
>B$\implies$C
>A$\implies$C

| A   | B   | C   | A$\implies$B | B$\implies$C | A$\implies$C |
| --- | --- | --- | ------------ | ------------ | ------------ |
| T   | T   | T   | T            | T            | T            |
| T   | T   | F   | T            | F            | F            |
| T   | F   | T   | F            | T            | T            |
| T   | F   | F   | F            | T            | F            |
| F   | T   | T   | T            | T            | T            |
| F   | T   | F   | T            | F            | T            |
| F   | F   | T   | T            | T            | T            |
| F   | F   | F   | T            | T            | T            |
>No falsifying rows. 

Study: How to construct a truth table, 