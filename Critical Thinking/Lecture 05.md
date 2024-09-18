#phil1440 
## More on formalization 
| Not        | And           | Or            | If, then      | If and only if     |
| ---------- | ------------- | ------------- | ------------- | ------------------ |
| ^(Left)    | ^(Right)      | v             | ->            | <->                |
| 'Negation' | 'Conjunction' | 'Disjunction' | 'Implication' | 'Bi-implicational' |
|            |               |               |               |                    |
- How to formalize a sentence/argument
- What we can''t formalize in truth-functional logic (TFL)
- 'only if', 'unless', 'if'
A v B: A or B
A ^ B: A and B
A->B: if A then B
A<->B: A if and only if B

EXAMPLE:
```
If it rains or snows, Aliice will be upset.
```
> Connectives: in the sentence (If/Then)
> A: it rains
> B: it snows
> C: Alice will be upset
> Atomic sentences: sentences that cannot be reduced further(With provided methods)
> (A v B)->C
> Only truth functional

- What makes something truth functional? 
	- 'Because' can't be properly formalized
		- 'A' because 'b'
			- You cannot calculate this value
			- Because packs in more words than just because. There is too much information that we cannot capture with just truth functional words
EXAMPLE:
```
Alice thinks the moon is made of cheese
```
> No available connectives in the sentence therefore it is not a truth functional sentence 
```
Alice will be upset unless it snows
```
> Connectives: Unless. Unless is similar to or 
> Either Alice will be upset or it snows
> (A v B) 
> A = Alice will be upset
> B = It snows