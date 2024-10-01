#phil1440 
## Tautologies
A sentence of TFL is a Tautology when it has the value 'T' in all rows of its truth table

| A   | A$\lor$$\neg$A |
| --- | -------------- |
| T   | T              |
| F   | T              |
(A$\lor|$$\neg$A) is a tautology, is not a sentence of TFL, it is a sentence of English
### Double Turnstile 
A, (A$\implies$B) $\vdash$ B
Means that 'B' follows deductively from the premmises 'A' and '(A$\implies$B)
$\models$(A$\lor$$\neg$A)
The statement follows deductively from zero premises.
## Contradiction 
Something is a contradiction when the conclusion is all F

| A   | (A$\land$$\neg$A) |
| --- | ----------------- |
| T   | F                 |
| F   | F                 |
(A$\land$$\neg$A)$\models$ 
'No Row of the truth table where the statement is true'
## (Joint) Consistency 
A$\land$B, $\neg$A, $\neg$B
Jointly inconsistent
A$\land$B, $\neg$A, $\neg$B $\models$
## Contingency 

Object language (TFL), metalanguage -> English (Whatever language we use to talk about the language)
'A' and '(A$\implies$B)' entail 'B'
((A$\land$(A$\implies$B))$\implies$B) - Statement in object language 

## "Meta Variable"
Say we want to say "If two formulas entail a third, then the conditional formula whose antecedent is the conjunction of he first and second formulas and whose consequent is the third is a Tautology"

If _A_, _B_ $\models$_C_ then $\models$(_A_$\land$_B_) $\implies$ _C_
### Deduction theorem
_A_, ...... , _A<sub>N</sub>_$\models$B
F("_A_, ........, _A<sub>N</sub>_" )$\implies$ B

EXAMPLES Determine whether ($\neg$B$\lor$B) is a tautology

| B   | ($\neg$B$\lor$B) |
| --- | ---------------- |
| T   | T                |
| F   | T                |
Yes because we get 'T ' in every ROW
EXAMPLE 2: Determine whether (A$\lor$B), $\neg$A, $\neg$B, are Jointly consistent

| A   | B   | A$\lor$B | $\neg$A | $\neg$B |
| --- | --- | -------- | ------- | ------- |
| T   | T   | T        | F       | F       |
| T   | F   | T        | F       | T       |
| F   | T   | T        | T       | F       |
| F   | F   | F        | T       | T       |
> Not jointly consistent as there is not one row where all three are true

Example 3: Suppose _A_, _B_ are logically equivalent, what can we say about (_A_$\iff$_B_)

| _A_ | _B_ | _A_$\iff$_B_ |
| --- | --- | ------------ |
| T   | T   | T            |
| F   | F   | T            |
_A_$\models$B, _B_$\models$_A_
(A$\iff$B) is a tautology