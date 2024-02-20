## Syntax Directed Translation and Definition. GPT + Research

- **Syntax-directed translation** fundamentally works by adding actions to the productions in a context-free grammar, resulting in a Syntax-Directed Definition (SDD).
- Actions are steps or procedures that will be carried out when that production is used in a derivation.
- These actions serve to imbue the grammar with semantic meaning, allowing for the generation of intermediate code or transformation of input code into target code.


- A **Syntax-Directed Definition (SDD)** couples a context-free grammar with semantic rules or actions. 
- These semantic rules define attributes or computations associated with the production rules of the grammar. 
- Types of attributes:
	1. **Inherited attributes**: These are attributes of non-terminal symbols that can be inherited from their parent nodes during parsing. For example, for the non-terminal E, we can define an inherited attribute `type`, which represents the type of the expression.
	2. **Synthesized attributes**: These are attributes whose values are computed during parsing and are not passed to parent nodes. For instance, for non-terminal E, we can define a synthesized attribute `value`, which holds the computed value of the expression.

For instance, consider a simple arithmetic expression grammar:

`E -> E + T | T `
`T -> T * F | F `
`F -> ( E ) | id`

We can augment this grammar with semantic rules to compute the value of expressions:

`E -> E1 + T { E.value = E1.value + T.value; }    | T { E.value = T.value; } `

`T -> T1 * F { T.value = T1.value * F.value; }    | F { T.value = F.value; }`

`F -> ( E ) { F.value = E.value; }    | id { F.value = id.value; }`

In this augmented grammar, the `{}` brackets contain semantic actions associated with each production rule. These actions compute and assign values to attributes such as `value`, which represents the value of an expression or subexpression. For example, the action `E.value = E1.value + T.value;` computes the value of an addition expression as the sum of the values of its left and right operands.



