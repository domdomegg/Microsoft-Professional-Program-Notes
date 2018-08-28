# Logic and Computational Thinking (DEV262x)

## Module 1: Logic and Computer Science

### Introduction

Logic deals with the structure of our thinking. Logic is the study of the rules of properly ordered thinking.

Like mathematics, logic was discovered. Logicians examine relationships between ideas and create rules for which relationships work. These rules are the system of formal logic.

The first formal logician is widely considered to be Aristotle (322-384 BC).

### Arguments

An argument consists of 3 parts:

1. Premises, reasons or evidence for a claim
2. A conclusion, the claim the argument is making
3. A logical relation, the connection between the premises and conclusion

### Statements and Propositions

A statement is a sentence that could be possibly true. A simple statement is one which declares a single truth. A compound statment is one which declares multiple truths.

A proposition is the underlying meaning behind a statement. Statements are the lingustic form of expressing propositions.

Propositions have a truth value at a given time, that is whether they are true or false.

### Logical Operators

| Name        	| Symbol          	| Example                                                            	|
|-------------	|-----------------	|--------------------------------------------------------------------	|
| Negation    	| `¬`, `!` or `~` 	| `¬A` means `It is not the case that A`                             	|
| Conjunction 	| `∧`, `&` or `·` 	| `A ∧ B` means `A and B`                                            	|
| Disjunction 	| `∨`, `∥` or `+` 	| `A ∨ B` means `A or B`                                             	|
| Conditional 	| `⇒`, `→` or `⊃` 	| `A ⇒ B` means `If A then B`. A is the antecedent, B the consequent 	|

## Module 2: Deductive and Inductive Arguments

### Deductive arguments

Deductive arguments prove their conclusion with absolute certainty.

#### Validity

Deductive arguments are valid iff all the premises being true means the conclusion must necessarily be true.

Deductive arguments are sound iff they are valid and all their premises are true.

#### Syllogisms

A syllogism is an argument which has two linked premises

Modus ponens

> 1. If `A` then `B`
> 2. `A`
> 3. Therefore, `B`

Modus tollens

> 1. If `A` then `B`
> 2. It is not the case that `B`
> 3. Therefore, it is not the case that `A`

Hypothetical Syllogism

> 1. If `A` then `B`
> 2. If `B` then `C`
> 3. Therefore, if `A` then `C`

Disjunctive Syllogism

> 1. `A` or `B`
> 2. It is not the case that `A`
> 3. Therefore, `B`

Fallacy: Affirming the consequent

> 1. If `A` then `B`
> 2. `B`
> 3. Therefore, `A`

Fallacy: Denying the antecedent

> 1. If `A` then `B`
> 2. It is not the case that `A`
> 3. Therefore, it is not the case that `B`

### Inductive arguements

Inductive arguemnts just show their conclusion is likely.

#### Strength

An inductive argument is strong if in the case the premises are true the conclusion is likely. An inductive argument is stronger the more likely the conclusion is.

Strength increases as the data sample size increases and as the conclusion becomes less extreme or specific.

## Module 3: Categorical Logic

To be in standard form, categories must be nouns and not adjectives.
> Example: "cute" is not a category, but "cute things" is.

### Categorical statements

Categorical logic uses three quantifiers to establish relationships between categories. They are:

* All
* Some (meaning "at least one")
* None (or no)

A categorical sentence contains four parts: the quantifier, the subject term, the copula and the predicate term.

| Quantifier 	| subject 	| copula 	| predicate   	|
|------------	|---------	|--------	|-------------	|
| All        	| cats    	| are    	| cute things 	|

Categorical statements can be classified into 4 groups:
* Universal affirmative: `All A are B`
* Universal negative: `No A are B`
* Particular affirmative: `Some A are B`
* Particular negative: `Some A are not B`

### Categorical syllogisms

Categorical syllogisms are syllogisms composed only of categorical statements.

> Example:
> 1. All `B` are `C`
> 2. All `A` are `B`
> 3. Therefore, All `A` are `C`

The term not in the conclusion is the middle term (example: `B`). The subject term of the conclusion is the minor term (example: `A`). The predicate term of the conclusion is the major term (example: `C`).

### Venn diagrams

We shade an area if it is empty. We place an X in an area to say that an area contains at least one thing (if something exists in some area but we do not know which one, the X is placed on the boundary of the possible regions).

Particular statements result in X's, and universal statements result in areas being shaded.

To test for validity, put the information in the premises on the diagram. Iff the conclusion is already represented by the diagram the argument is valid.