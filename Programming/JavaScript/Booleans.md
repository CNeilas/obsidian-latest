
Only making this not for a few things. 
First, the order of javascript evaluating these is !, && and only then ||,
if you write a ! in front of parentheses it will convert the evaluation result from true to false or vice versa.

De Morgan's Law:

`!(A || B)` is equivalent to `!A && !B`
`!(A && B)` is equivalent to `!A || !B`

